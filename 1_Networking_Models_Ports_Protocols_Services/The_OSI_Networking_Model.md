# Open Systems Interconnection Networking Model (OSI Model)

- Conceptual model which describes a network architecture that enables data to be passed between different systems

- Consists of seven layers, each with specific functions and protocols:
    7. Application Layer: provides access to the network for applications
        - Takes user input and display output
        - Provides network services to applications
        - Protocols: HTTP, FTP, SMTP, DNS, Telnet

    6. Presentation Layer: convert data formats and encryption
        - Data translation, encryption, and compression
        - Protocols: Secure Sockets Layer (SSL), Transport Layer Security (TLS), Hypertext Transfer Protocol Secure (HTTPS)

    5. Session Layer: synchronization of data between applications on different devices
        - Establishes, manages, and terminates connections
        - Protocols: NetBIOS, Network File System (NFS), Server Message Block (SMB)

    4. Transport Layer: transport data between network devices
        - Error detection and correction
        - Service address translation
        - Segmentation and reassembly
        - Data flow control (buffering/windowing)
        - Protocols: TCP, UDP

    3. Network Layer: routing and forwarding statically/dynamically
        - Internet Protocol (IP)
        - Routing protocols (e.g., OSPF, BGP)

    2. Data Link Layer: getting data to the physical layer
        - Media Access Control (MAC): hardware identification and addressing
        - Logical Link Control (LLC): error detection and correction

    1. Physical Layer: networks physical characteristics
        - Hardware specifications
        - Network Topology
        - Electrical signals 

- Mapping Network Devices to the OSI Model:

    | Device        | Device Type                    | Layer # |
    |---------------|--------------------------------|---------|
    | Proxy Server  | Application Layer              | 7       |
    | Load Balancer | Transport or Application Layer | 4/7     |
    | IDS/IPS       | Network Layer                  | 3       |
    | Firewall      | Network or Transport Layer     | 3/4     |
    | Router        | Network Layer                  | 3       |
    | Switch        | Data Link or Network Layer     | 2/3     |
    | Bridge        | Data Link Layer                | 2       |
    | Access Point  | Data Link Layer                | 2       |
    | NIC           | Data Link Layer                | 2       |
    | Repeater      | Physical Layer                 | 1       |
    | Hub           | Physical Layer                 | 1       |


- Developed by the International Organization for Standardization (ISO) in 1984

- Can be used as a bottom-to-top troubleshooting tool

# Four-Layer TCP/IP Model
- A more practical version of the OSI model, consisting of four layers:

    | Layer       | OSI Equivalent                     |
    |-------------|------------------------------------|
    | Application | Application, Presentation, Session |
    | Transport   | Transport                          |
    | Internet    | Network                            |
    | Link        | Data Link, Physical                |

# Data Encapsulation/Decapsulation and OSI Model
- Encapsulation: adding protocol information to data as it passes through layers

- Decapsulation: removing protocol information from data as it passes through layers

- OSI model encapsulation/decapsulation

    | Layer        | Encapsulation/Decapsulation Function     | Representation                        |
    |--------------|------------------------------------------|---------------------------------------|
    | Application  | v data is created in the application     | DATA                                  |
    | Presentation | v and passed to/from the transport layer | DATA                                  |
    | Session      | -                                        | DATA                                  |
    | Transport    | - segment header is added/removed        | SEGMENT HEADER / DATA                 |
    | Network      | - packet header is added/removed         | PACKET HEADER / SEGMENT HEADER / DATA |
    | Data Link    | - frame header/trailer is added/removed  | FRAME HEADER / PACKET HEADER / SEGMENT HEADER / DATA / FRAME TRAILER                             |