
# OSI & TCP/IP Models

## 1. OSI Model (Open Systems Interconnection)

The OSI Model is a 7-layer conceptual framework used to standardize network communication functions.

### Layers & Protocols

| Layer | Description | Protocols & Examples |
|-------|-------------|----------------------|
| 7 - Application | Provides services for end users, like web browsing & email. | HTTP, HTTPS, FTP, SMTP, IMAP, POP3, SNMP |
| 6 - Presentation | Translates data formats, encryption, and compression. | SSL/TLS, JPEG, ASCII, GIF |
| 5 - Session | Manages session establishment, maintenance, and termination. | NetBIOS, PPTP, RPC, SIP |
| 4 - Transport | Handles end-to-end communication and data flow control. | TCP, UDP |
| 3 - Network | Routes packets between different networks. | IP, ICMP, ARP, RIP, OSPF, BGP |
| 2 - Data Link | Ensures error-free transmission between adjacent nodes. | Ethernet, MAC, PPP, Frame Relay, ATM |
| 1 - Physical | Defines hardware and transmission mediums. | Cables, Fiber, Hubs, NICs, RF, Bluetooth |

---

## 2. TCP/IP Model (Transmission Control Protocol/Internet Protocol)

The TCP/IP Model is a 4-layer model used in real-world networking.

### Layers & Protocols

| Layer | Description | OSI Equivalent | Protocols & Examples |
|-------|-------------|----------------|----------------------|
| 4 - Application | Handles end-user applications & data representation. | Application, Presentation, Session | HTTP, HTTPS, FTP, SSH, DNS, SNMP |
| 3 - Transport | Manages host-to-host communication, reliability, and flow control. | Transport | TCP, UDP |
| 2 - Internet | Handles logical addressing, routing, and packet forwarding. | Network | IP, ICMP, ARP, RIP, OSPF, BGP |
| 1 - Network Access | Defines how data is physically transmitted. | Data Link, Physical | Ethernet, MAC, Wi-Fi, Bluetooth |

---

## 3. Key Differences Between OSI & TCP/IP Models

| Feature | OSI Model | TCP/IP Model |
|---------|-----------|--------------|
| Layers | 7 | 4 |
| Developed By | ISO (International Organization for Standardization) | U.S. Department of Defense |
| Usage | Conceptual model, not strictly implemented | Practical, widely used in modern networks |
| Transport Protocols | TCP, UDP | TCP, UDP |
| Focus | Defines complete network communication process | Standardizes internet-based communication |

---

## 4. Common Protocols & Their Layers

| Protocol | OSI Layer | TCP/IP Layer |
|----------|-----------|--------------|
| HTTP/HTTPS | Application | Application |
| FTP | Application | Application |
| DNS | Application | Application |
| TCP | Transport | Transport |
| UDP | Transport | Transport |
| IP | Network | Internet |
| ICMP | Network | Internet |
| Ethernet | Data Link | Network Access |

---

## 5. Summary

- The OSI Model is a theoretical framework with 7 layers.
- The TCP/IP Model is a real-world implementation with 4 layers.
- Both models help standardize network communication.
- Each layer serves a specific role, ensuring seamless data transmission.

---

## 6. How a Packet Travels Through the OSI Model

### Encapsulation & Decapsulation Data Units

| Layer | Data Unit | Description |
|-------|-----------|-------------|
| 7 - Application | Data | Raw user-generated information (e.g., HTTP request). |
| 6 - Presentation | Data | Data formatting, encryption, compression. |
| 5 - Session | Data | Maintains and manages communication sessions. |
| 4 - Transport | Segment (TCP) / Datagram (UDP) | TCP ensures reliable communication; UDP is connectionless. |
| 3 - Network | Packet | Contains source and destination IP addresses for routing. |
| 2 - Data Link | Frame | Adds MAC addresses for local delivery. |
| 1 - Physical | Bits | Converts frames into signals (electrical, optical, radio). |

### Expanded Process of Encapsulation & Decapsulation

**Encapsulation (Sending Data):**
- Application data is formatted, encrypted, compressed (Presentation Layer).
- Session is initiated and maintained (Session Layer).
- Data is divided into TCP segments or UDP datagrams (Transport Layer).
- Segments are encapsulated into IP packets with logical addressing (Network Layer).
- Packets are converted into frames with MAC addresses (Data Link Layer).
- Frames are transmitted as bits via the physical medium (Physical Layer).

**Decapsulation (Receiving Data):**
- Bits are converted back into frames at the Physical Layer.
- Frames are stripped of MAC headers and turned into packets (Data Link Layer).
- Packets are processed for IP routing and forwarded accordingly (Network Layer).
- TCP/UDP segments are reassembled for proper sequencing (Transport Layer).
- Data is decompressed, decrypted, and formatted (Presentation Layer).
- The application receives readable data (Application Layer).

---

## 7. How a Packet Travels Through the TCP/IP Model

### Encapsulation & Decapsulation Data Units

| Layer | Data Unit | Description |
|-------|-----------|-------------|
| 4 - Application | Data | Raw application data generated (e.g., HTTP request, email). |
| 3 - Transport | Segment (TCP) / Datagram (UDP) | Ensures reliable or fast transmission. |
| 2 - Internet | Packet | Adds source and destination IP addresses. |
| 1 - Network Access | Frame | Encapsulates the packet with MAC addresses for local delivery. |

### Expanded Process of Encapsulation & Decapsulation

**Encapsulation:**
- Application layer generates data (e.g., HTTP request, email).
- Transport layer encapsulates data into TCP segments or UDP datagrams.
- Internet layer adds source and destination IP addresses to create packets.
- Network access layer converts packets into frames with MAC addresses and transmits them.

**Decapsulation:**
- Network access layer extracts packets from received frames.
- Internet layer processes IP headers, verifies addresses, and routes packets.
- Transport layer ensures reliability, reordering, and error correction (for TCP).
- Application layer receives fully reconstructed data for end-user processing.

---

