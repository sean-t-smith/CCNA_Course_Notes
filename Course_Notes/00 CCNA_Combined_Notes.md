# 1. NETWORKING DEVICES

## What is a network?

A computer network is a digital telecommunications network allows NODES to share RESOURCES.

A CLIENT is a device that accesses a service made available by a SERVER.

A SERVER is a device that provides functions or services for CLIENTS.

- Note : The same device can be a CLIENT in some situations and a SERVER in other situations. Ex: A Peer-to-Peer network.

SWITCHES (Level 2):

- provide connectivity to hosts within the same LAN (Local Area Network)
- Have many network interfaces/ports for End Hosts to connect to.
- DO NOT provide connectivity between LANs/over the Internet.

ROUTERS (Level 3):

- have fewer network interfaces than switches.
- are used to provide connectivity BETWEEN LANs.
- are used to send data over the Internet.

FIREWALL (Can be Level 3,4, and 7):

- Firewalls are specialty hardware network security devices that control network traffic entering/exiting your network.
- Can be places "inside" or "outside" the network.
- Monitor and control network traffic based on configured rules.
- Are known as "Next-Generation Firewalls" when they include more modern and advanced filtering capabilities.
- Host-based firewalls are software applications that filter traffic entering and exiting a host machine, like a PC.

# 2. INTERFACES AND CABLES

SWITCHES provide many PORTS for connectivity (usually 24)

These PORTS tend to be RJ-45 (Registered Jack) ports.

---

WHAT IS ETHERNET?

- Ethernet is a collection of network protocols/standards.

Why do we need network protocols and standards?

- provide common communication standards over networks.
- provide common hardware standards to allow connectivity between devices.

Connections between devices operates at a set speed.

These speeds are measured in "bits per second" (bps)

A bit is a value of "0" or "1".
A byte is 8 bits (0s and 1s)

| Size | # of Bits |
| --- | --- |
| 1 kilobit (Kb) |  1,000 |
| 1 megabit (Mb) | 1,000,000 |
| 1 gigabit (Gb) | 1,000,000,000 |
| 1 terabit (Tb) | 1,000,000,000,000  |

Ethernet standards are:

- Defined in the IEEE 802.3 standard in 1983
- IEEE = Institute of Electrical and Electronics Engineers

ETHERNET STANDARDS (COPPER)

| Speed | Common Name | Standard | Cable Type | Max Transmission Distance |
| --- | --- | --- | --- | --- |
| 10 Mbps | Ethernet | 802.3i | 10BASE-T | 100m Max |
| 100 Mbps | Fast Ethernet | 802.3u | 100BASE-T | 100m Max |
| 1 Gbps | Gigabit Ethernet | 802.3ab | 1000BASE-T | 100m Max |
| 10 Gbps | 10 Gigabit Ethernet | 802.3an | 10GBASE-T | 100m Max |

BASE = refers to Baseband Signaling

T = Twisted Pair 

Most Ethernet uses copper cables.

UTP or Unshielded Twisted Pair
(no metallic shield)
Twist protects against EMI (Electromagnetic Interference)

Most use 8 wires (4 pairs) however ...

10/100BASE-T = 2 pairs (4 wires)

![image](https://github.com/psaumur/CCNA/assets/106411237/00b27997-a78a-4e81-a878-7f8ab7e3279e)


---

How do devices communicate via their connections?

Each ethernet cable has a RJ-45 plug with 8 pins on the ends.

![image](https://github.com/psaumur/CCNA/assets/106411237/323930c9-3387-4bf9-aae1-f61db0fd9c04)


- PCs Transmit(TX) data on Pins #1-2
- Switches Receive(RX) data on Pins #1-2
- PCs Receive(RC) data on Pins #3,6
- Switches Transmit(TX) data on Pins #3,6

This allows Full-Duplex transmission of data.

---

What if a Router / Switch connect?

![image](https://github.com/psaumur/CCNA/assets/106411237/907259d9-1837-4d53-8f45-a42934fb66f2)


- Routers Transmit(TX) data on Pins #1-2
- Routers Receive(RX) data on Pins #3,6
- Switches Transmit(TX) data on Pins #3,6
- Switches Receive(RX) data on Pins #1-2

Routers and PCs connect the same way with Switches.

The cable used to connect is called a "Straight-Through" cable.

---

What if we want to connect similar devices to each other?

We CANNOT use a "Straight-Through" cable.
We MUST use a "Crossover" cable.

This cable swaps the pins on one end to allow connection to work.

![image](https://github.com/psaumur/CCNA/assets/106411237/d98646ad-366f-4e96-8c6f-f6b5f32f9bdc)


PIN#1 -----> PIN#3
PIN#2 -----> PIN#6

PIN#3 -----> PIN#1
PIN#6 -----> PIN#2

---

| DEVICE TYPE | TRANSMIT (TX) PINS | RECEIVE (RX) PINS |
| --- | --- | --- |
| ROUTER | 1 and 2 | 3 and 6 |
| FIREWALL | 1 and 2 | 3 and 6 |
| PC | 1 and 2 | 3 and 6 |
| SWITCH | 3 and 6 | 1 and 2 |

---

Most modern equipment now has AUTO MDI-X which **automatically detects** which pins their neighbour is transmitting on and adjust the pins they receive data on.

1000BASE-T/10GBASE-T = 4 pairs (8 wires)

Each wire pair is **bidirectional** so can transmit/receive much faster than 10/100BASE-T.

![image](https://github.com/psaumur/CCNA/assets/106411237/763c841a-d7b5-4e87-8500-b54d623af620)


---

Fiber-Optic Connections:

- Defined in the IEEE 802.3ae standard

SFP Transceiver (Small Form-Factor Pluggable) allows fiber-optic cables to connect to switches/routers.

- Have separate cables to transmit / receive.

4 parts to a fiber-optic cable.

![image](https://github.com/psaumur/CCNA/assets/106411237/70b81cde-265f-413b-815b-3e7184ea0586)


There are TWO types of fiberoptic cable.

Single-Mode:

![image](https://github.com/psaumur/CCNA/assets/106411237/d9a4b633-44c2-491d-92e4-329dd3b9074b)


- Narrower than multimode
- Lighter enters at a single angle (mode) from a laser-based transmitter.
- Allows longer cables than both UTP and multimode fiber.
- More expensive than multimode fiber (due to more expensive laser-based SFP transmitters)

Multimode:

![image](https://github.com/psaumur/CCNA/assets/106411237/e73ec4d0-9aa1-4a75-848c-3af70e770dce)


- Core is wider than Single-mode
- Allows multiple angles (modes) of light waves to enter core
- Allows longer cables than UTP but shorter than single-mode
- Cheaper than single-mode fiber (due to cheaper LED-based SFP transmitter)

---

Fiber Optic Standards:

| Speed | Standard | Connection Speed | Mode Support | Max Transmission Distance |
| --- | --- | --- | --- | --- |
| 1000BASE-LX | 802.3z | 1 Gbps | Multimode / Single | 550 meters (Multi)  / 5km (Single) |
| 10GBASE-SR | 802.3ae | 10 Gbps | Multimode | 400 meters |
| 10GBASE-LR | 802.3ae | 10 Gbps | Single | 10 kilometers |
| 10GBASE-ER | 802.3ae | 10 Gbps | Single | 30 kilometers |

---

UTP vs Fiber-Optic Cabling:

UTP are:

- Lower cost than fiber-optic.
- Shorter maximum distance than fiber-optic (~100m).
- Can be vulnerable to EMI (Electromagnetic Interference).
- RJ45 ports used with UTP are cheaper than SFP ports.
- Emit (leak) a faint signal outside of cable, which can be copied (security risk).

Fiber-Optic:

- Higher cost than UTP.
- Longer maximum distance than UTP.
- No vulnerability to EMI.
- SFP ports are more expensive than RJ45 ports (single-mode is more expensive than multimode).
- Does not emit any signal outside of the cable (no security risk).

# 3. OSI MODEL & TCP/IP SUITE

## What is a networking model?

Networking models categorize and provide a structure for networking protocols and standards.

(Protocols are a set of logical rules defining how network devices and software should work)

## OSI MODEL

- Open Systems Interconnection Model
- Conceptual model that categorizes and standardizes the different functions in a network.
- Created by the "International Organization for Standardization" (ISO)
- Functions are divided into 7 "Layers"
- These layers work together to make the network work.

![image](https://github.com/psaumur/CCNA/assets/106411237/bbf46de2-e025-4ddd-b52b-614b280598da)

As data moves from the top layer, downward, the process is called “encapsulation”

As data moves from the bottom layer, upward, the process is called “de-encapsulation”

When interactions occur on the same layer, it’s called “same-layer interaction”

![image](https://github.com/psaumur/CCNA/assets/106411237/b7cf4900-993c-49f0-b6ea-70f4f0719633)

Mnemonic to help remember the Data Layer Names / Order

![image](https://github.com/psaumur/CCNA/assets/106411237/01f532f6-b636-4b7c-99d0-a67f7e483a99)


### The layers are :

### 7 - APPLICATION

- This Layer is closest to end user.
- Interacts with software applications.
- HTTP and HTTPS are Layer 7 protocols

Functions of Layer 7 include:

- Identifying communication partners
- Synchronizing communication

---

### 6 - PRESENTATION

- Translates data to the appropriate format (between Application and Network formats) to be sent over the network.

---

### 5 - SESSION

- Controls dialogues (sessions) between communicating hosts.
- Establishes, manages, and terminates connections between local application and the remote application.

---

Network engineers don't usually work with the top 3 layers.
Application developers work with the top layers of the OSI model to connect their applications over networks.

---

### 4 - TRANSPORT

- Segments and reassembles data for communication between end hosts.
- Breaks large pieces of data into smaller segments which can be more easily sent over the network and are less likely to cause transmission problems if errors occur.
- Provides HOST-TO-HOST (end to end) communication

When Data from Layer 7-5 arrives, it receives a Layer 4 Header in the Transport layer.

<< DATA + L4 Header >>

This is called a SEGMENT.

---

### 3 - NETWORK

- Provides connectivity between end hosts on different networks (ie: outside of the LAN).
- Provides logical addressing (IP Addresses).
- Provides path selection between source and destination
- **ROUTERS** operate at Layer 3.

When Data and the Layer 4 Header arrive in the Network Layer, it receives a Layer 3 Header.

<< DATA + L4 Header + L3 Header >>

This is called a **PACKET**.

---

### 2 - DATA LINK

- Provides NODE-TO-NODE connectivity and data transfer (for example, PC to Switch, Switch to Router, Router to Router)
- Defines how data is formatted for transmission over physical medium (for example, copper UTP cables)
- Detects and (possibly) corrects Physical (Layer 1) errors.
- Uses Layer 2 addressing, separate from Layer 3 addressing.
- **SWITCHES** operate at Layer 2

When the Layer 3 Packet arrives, a Layer 2 Trailer and Header are added.

<< L2 Trailer + DATA + L4 Header + L3 Header + L2 Header >>

This is called a FRAME.

All the steps leading up to transmission is called ENCAPSULATION.
When the frame is sent to the receiver, it then goes through the reverse process, DE-ENCAPSULATION, stripping off layers while travelling from OSI Layer 1 to Layer 7.

---

### 1 - PHYSICAL

- Defines physical characteristics of the medium used to transfer data between devices. For example : voltage levels, maximum transmission distances, physical connectors, cable specs.
- Digital bits are converted into electrical (for wired connections) or radio (for wireless connections) signals.
- All of the information in SECTION 2 (NETWORKING DEVICES) is related to the Physical Layer

---

### OSI MODEL - PDU's

![image](https://github.com/psaumur/CCNA/assets/106411237/9b885a51-91cd-4fe6-b1be-e7fa7aa220b5)

A PDU is a Protocol Data Unit. Each step of the process is a PDU.

| OSI LAYER # | PDU NAME | PROTOCOL DATA ADDED |
| --- | --- | --- |
| 7-5 | DATA | Data |
| 4 | SEGMENT | Layer 4 Header Added |
| 3 | PACKET | Layer 3 Header Added |
| 2 | FRAME | Layer 2 Trailer and Header Added |
| 1 | BIT | 0s and 1s Transmission |

<< L2 Trailer + DATA + L4 Header + L3 Header + L2 Header >>

---

### TCP/IP Suite

- Conceptual model and set of communications protocols used in the Internet and other networks.
- Known as TCP/IP because those are two of the foundational protocols in the suite.
- Developed by the US Dept. of Defense through DARPA (Defense Advanced Research Projects Agency).
- Similar structure to the OSI Model, but fewer layers.
- THIS is the model actually in use in modern networks.
- * Note : The OSI Model still influences how network engineers think and talk about networks.

![image](https://github.com/psaumur/CCNA/assets/106411237/e9593c06-46a3-4ff9-aa01-863e0aeb5df3)


---

### Layer Interactions

![image](https://github.com/psaumur/CCNA/assets/106411237/372c45a0-bb3e-4342-af2b-79d3606384ec)


Adjacent-Layer Interactions:

- Interactions between different layers of the OSI Model on same host.

Example:

Layers 5-7 sending Data to Layer 4, which then adds a Layer 4 header (creating a SEGMENT).

Same-Layer Interactions:

- Interactions between the same Layer on different hosts.
- The concept of Same-Layer interaction allows you to ignore the other layers involved and focus on the interactions between a single layer on different devices.

Example:

The Application Layer of YouTube's web server and your PC's browser.

# 4. INTRO TO THE CLI

### What is a CLI?

- A "Command-line Interface"
- The interface you use to configure Cisco devices

A GUI is a "Graphical User Interface"

### How do you connect to a Cisco Device?

- Console Port : When you first configure a device, you have to connect via the Console Port.

You can use a "Rollover cable" : DB9 serial connector to RJ45 OR a DB9 Serial to USB

![image](https://github.com/psaumur/CCNA/assets/106411237/0527c007-d607-4bef-8ce1-7b18a177614d)

### How do you actually access the CLI?

- You need to use a TERMINAL EMULATOR (Example: PuTTy is a popular choice) and connect via "Serial" (default settings)

### Cisco Default Settings are:

Speed (baud) : 9600 bits/second
Data bits: 8 data bits
Stop bits: 1 stop bit (sent after 8 data bits are sent)
Parity: None
Flow Control: None

---

When you first enter the CLI you will DEFAULT be in what is called 'User EXEC' mode.

USER EXEC MODE:

(Hostname) >		// Prompt looks like THIS //

- User EXEC mode is very limited.
- User can look at some things but can't make ANY changes to the configuration.
- AKA 'User Mode'

Using the 'enable' command, in User EXEC mode, switches you to 'Privileged EXEC' mode.

---

PRIVILEGED EXEC MODE:

- Provides complete access to view the device's configuration, restart the device, etc.
- Cannot change the configuration, but can change the time on the device, save the configuration file, etc.

(Hostname)#		// Prompt looks like THIS //

---

USE a Question Mark (?) to view the available commands in ANY mode. Combining ? with a letter or partial command will list all the commands with those letters.

![image](https://github.com/psaumur/CCNA/assets/106411237/52454e6f-d5b1-45f0-9a50-e412d356f6d2)


USE the TAB key to complete partially entered commands IF the command exists.

---

### GLOBAL CONFIGURATION MODE:

To enter Global Configuration Mode, enter the command, within Privileged EXEC mode

 'configure terminal' (or 'conf t')

Router# configure terminal
Router(config) #		

Router(config) # run 

Router(config) # no 

Type 'exit' to drop back into 'Privileged EXEC' mode.

---

### To Enable Password for User EXEC mode:

Router(config)# enable password (password)

- Passwords ARE case-sensitive.

// This command encrypts plain-text passwords, visible in the config files, using simple encryption.

Router(config)# service password-encryption

If you enable 'service password-encryption'

- Current passwords WILL be encrypted.
- Future passwords WILL be encrypted.
- The 'enable secret' WILL NOT be effected.

If you disable 'service password-encryption'

- Current passwords WILL NOT be decrypted.
- Future passwords WILL NOT be encrypted.
- The 'enable secret' WILL NOT be effected.

// This command enables passwords for the Privileged EXEC mode.

Router(config)# enable secret (password)

// enable secret will ALWAYS be encrypted (at level 5)

---

There are TWO separate configuration files kept on the device at once.

Running-config :

- The current, ACTIVE configuration file on the device. As you enter commands in the CLI, you edit the active configuration.

Startup-config :

- The configuration file that will be loaded upon RESTART of the device.

To see the configuration files, inside 'Privileged EXEC' mode:

Router# show running-config // for running config //

OR

Router# show startup-config // for startup config //

---

To SAVE the Running configuration file, you can:

Router# write
Building configuration...
[OK]

Router# write memory
Building configuration...
[OK]

Router# copy running-config startup-config

Destination filename [startup-config]?

Building configuration...
[OK]

---

To encrypt passwords:

Router# conf t

Router(config)# service password-encryption

This makes all current passwords *encrypted*

Future passwords will ALSO be *encrypted*

“Enable secret” will not be effected (it’s ALWAYS encrypted)

![image](https://github.com/psaumur/CCNA/assets/106411237/09c841fe-b5c0-4683-9082-baf060e24c03)


Now you will see that the password is no longer in plaintext.

“7” refers to the type of encryption used to encrypt the password. In this case, “7” uses Cisco’s proprietary encryption.

“7” is fairly easy to crack since the encryption is weak.

For BETTER / STRONGER encryption, use “enable secret”

![image](https://github.com/psaumur/CCNA/assets/106411237/346f3015-9211-47a9-888f-4e02a013a728)


“5” refers to MD5 encryption.

Can still be cracked but it’s much much stronger.

Once you use “enable secret” command, this will override “enable password”

---

To CANCEL or delete a command you entered, use the “no” keyword

![image](https://github.com/psaumur/CCNA/assets/106411237/2978d101-08d4-4ee3-8995-f36aa1c47d15)


In this instance, disabling “service password-encryption”:

- current passwords will NOT be decrypted (unchanged)
- future passwords will NOT be encrypted
- the “enable secret” will not be effected

---

![image](https://github.com/psaumur/CCNA/assets/106411237/e16966a3-674a-4376-bdab-2c06e3659e5f)

![image](https://github.com/psaumur/CCNA/assets/106411237/e449e074-bf4c-40f1-a61e-0442ad83f284)

![image](https://github.com/psaumur/CCNA/assets/106411237/4c1bdf58-7de6-4074-8189-1573a174474c)

![image](https://github.com/psaumur/CCNA/assets/106411237/e7771e65-5ed5-406d-9751-76520713210c)

![image](https://github.com/psaumur/CCNA/assets/106411237/5f7357d4-f44b-4a61-a24c-86f3368f30f7)

# 5. ETHERNET LAN SWITCHING : PART 1

![image](https://github.com/psaumur/CCNA/assets/106411237/a40e81d9-c008-4fb4-8580-2eaf63003e63)

![image](https://github.com/psaumur/CCNA/assets/106411237/2db46525-98b8-4211-aeb3-efc34bd84222)


LAN's

- A LAN is a network contained in a relatively small area.
- Routers are used to connect separate LAN's

![image](https://github.com/psaumur/CCNA/assets/106411237/2a4de9d4-3408-49b9-9492-42b7eb56fe27)


An ETHERNET FRAME looks like:

![image](https://github.com/psaumur/CCNA/assets/106411237/ad579917-f9a0-4cd8-be25-351ecbfc87af)


Ethernet Trailer --- PACKET --- Ethernet Header

The Ethernet Header contains 5 Fields:

Preamble -- SFD -- Destination -- Source -- Type
7 bytes  -- 1 byte -- 6 bytes -- 6 bytes -- 2 bytes

---

PREAMBLE:

- Length: 7 bytes (56 bits)
- Alternating 1's and 0's
- 10101010 * 7x
- Allows devices to synchronize their receiver clocks

SFD : ‘Start Frame Delimiter’

- Length: 1 byte(8 bits)
- 10101011
- Marks end of the PREAMBLE and beginning of rest of frame.

---

DESTINATION AND SOURCE

- Layer 2 Address
- Indicates the devices sending / receiving the frame
- MAC = ’Media Access Control’
- = 6 byte (48-bit) address of the physical device

---

TYPE / LENGTH

- 2 bytes (16-bit) field
- A value of 1**500 or less** in this field indicates the LENGTH of the encapsulated packet (in bytes)
- A value of **1536 or greater** in this field indicates the TYPE of the encapsulated packet and length is determined via other methods.
- IPv4 = 0x0800 (hexadecimal) = 2048 in decimal
- IPv6 = 0x86DD (hexadecimal) = 34525 in decimal
- Layer 3 protocol used in the encapsulated Packet, which is almost always Internet Protocol (IP) version 4 or version 6.

---

The ETHERNET TRAILER contains:

FCS

- ‘FRAME CHECK SEQUENCE’
- 4 bytes (32 bits) in length
- Detects corrupted data by running a 'CRC' algorithm over the received data
- CRC = "Cyclic Redundancy Check"

---

Altogether the ETHERNET FRAME = 26 bytes (header + trailer)

![image](https://github.com/psaumur/CCNA/assets/106411237/c8c1a143-0675-4aa4-83bc-6031d10cc0b8)


---

MAC ADDRESS (48 bits long)

- 6-bytes (48-bits) physical address assigned to the device when it is made.
- AKA 'Burned-In Address' (BIA)
- Is globally unique
- First 3 bytes are the OUI (Organizationally Unique Identifier) which is assigned to the company making the device
- The last 3 bytes are unique to the device itself
- Written as 12 hexadecimal characters

Example:

E8:BA:70 // 11:28:74
OUI    // Unique Device ID

HEXADECIMAL

![image](https://github.com/psaumur/CCNA/assets/106411237/65a5e84a-b8db-46f5-b288-518139e99453)


INTERFACE NAMES

F0/1, F0/2, F0/3... F stands for "Fast Ethernet" or 100 Mbps interfaces.

---

MAC ADDRESS TABLE

Each Switch stores a DYNAMICALLY LEARNED MAC ADDRESS TABLE, using the SOURCE MAC ADDRESS of frames it receives.

![image](https://github.com/psaumur/CCNA/assets/106411237/582421a9-6351-48b7-bfe1-c2153520920c)


When a Switch doesn't know the DESTINATION MAC ADDRESS of a frame (UNKNOWN UNICAST FRAME), it is forced to FLOOD the frame - Forward the frame out of ALL it's interfaces, except the one it received the packet from.

When a KNOWN Unicast Frame is known (MAC Address is recognized by the entry in the MAC ADDRESS TABLE), the frame is FORWARDED like normal.

![image](https://github.com/psaumur/CCNA/assets/106411237/ff731ab3-fad2-4e10-9fa7-ce583a6a0bb2)

- Note: Dynamic MAC Addresses are removed from the MAC ADDRESS TABLE every 5 minutes of inactivity.

# 6. ETHERNET LAN SWITCHING : PART 2

An ETHERNET FRAME looks like:

Ethernet Header --- DATA (Packet) --- Ethernet Trailer

![image](https://github.com/psaumur/CCNA/assets/106411237/27c1877f-57d7-44ea-8c64-b0ec2b308ad0)


The Ethernet Header contains 5 Fields:

Preamble -- SFD -- Destination -- Source -- Type/Length
7 bytes  -- 1 byte -- 6 bytes -- 6 bytes --   2 bytes

Ethernet Trailer contains 1 Field:

FCS (Frame Check Sequence) = 4 bytes

- The PREAMBLE + SFD is not usually considered part of the ETHERNET HEADER.

THEREFORE the size of the ETHERNET HEADER + TRAILER is 18 bytes

(6 + 6 + 2 + 4 bytes for the FRAME CHECK SEQUENCE)

---

The MINIMUM size for an ETHERNET FRAME (Header + Payload [PACKET] + Trailer) is 64 BYTES.

64 BYTES - 18 BYTES (Header + Trailer size) = 46 BYTES

THEREFORE the MINIMUM DATA PAYLOAD (PACKET) size is 46 BYTES!

IF the PAYLOAD is LESS than 46 BYTES then PADDING BYTES are added (padding bytes are a series of 0's) until it equals to 46 BYTES.

---

When a PC sends a packet to a device with an unknown IP address, it uses an ARP Request.

![image](https://github.com/psaumur/CCNA/assets/106411237/e2d0e5d2-7c98-4671-b356-903132fd7525)


- ARP stands for 'Address Resolution Protocol'.
- It is used to discover the Layer 2 address (MAC address) of a known Layer 3 address (IP address)
- Consists of two messages:
    - ARP REQUEST (Source message)
    - ARP REPLY (Destination message)
- ARP REQUEST is BROADCAST = sent to all hosts on network, except the one it received the request from.

An ARP REQUEST frame has:

- Source IP Address
- Destination IP Address
- Source MAC address
- BROADCAST MAC Address - FFFF.FFFF.FFFF

An ARP REPLY frame has:

- Source IP Address
- Destination IP Address
- Source MAC address
- Destination MAC Address

ARP REPLY is a known UNICAST frame = Sent only to the host that sent the ARP REQUEST.

![image](https://github.com/psaumur/CCNA/assets/106411237/914cdf2a-c631-47e5-80f9-46e32ebed311)


---

PING

- A network utility that is used to test reachability
- Measures round-trip time
- Uses two messages:
    - ICMP Echo REQUEST
    - ICMP Echo REPLY
- Is UNICAST
- Command to use ping:
    - ping <ip-address>

By Default, a CISCO IOS sends 5 ICMP requests/replies
(Default size is 100-bytes)

- A period (.) is a failed ping
- An exclamation mark (!) is a successful ping

---

USEFUL CISCO IOS COMMANDS (from Privileged EXEC mode)

PC1# show arp // shows hosts ARP table

![image](https://github.com/psaumur/CCNA/assets/106411237/da199d21-4f41-485e-8917-ca8e3d789617)


---

SW1#show mac address-table // show the switches MAC table

![image](https://github.com/psaumur/CCNA/assets/106411237/c1cd95dd-7742-4703-9487-946652c95485)


Will show:

Vlan --- MAC Address --- Type --- Ports(interfaces)

(Vlan = Virtual Local Area Network)

---

![image](https://github.com/psaumur/CCNA/assets/106411237/657b054b-a90c-4e5f-8544-2a51082cb631)


SW1# clear mac address-table dynamic <optional MAC address>

// clears the entire switches MAC table.
// IF the optional MAC address is used, it will clear the SPECFIC MAC address.

SW1 #clear mac address-table dynamic interface <optional Interface>

// clears the MAC table entry of the Switch by it's **INTERFACE n**ame.

# 7. IPv4 ADDRESSING : PART 1

OSI MODEL - NETWORK LAYER (Layer 3)

- Provides connectivity between end hosts on DIFFERENT networks (ie: outside of the LAN)
- Provides logical addressing (IP addresses)
- Provides path selection between SOURCE and DESTINATION
- ROUTERS operate at LAYER 3

ROUTING

SWITCHES (Layer 2 Devices) do no separate different networks. They connect and EXPAND networks within the same LAN.

By adding a ROUTER, however, between two SWITCHES, you create a SPLIT in the network; each with it's own network IP address.

Example:
192.168.1.0/24 (255.255.255.0)
192.168.2.0/24 (255.255.255.0)

![image](https://github.com/psaumur/CCNA/assets/106411237/3d414956-cb53-46f6-b386-3fc9bba11802)


ROUTERS have unique IP Addresses for EACH of their interface connections, depending on their location.

The IP Address for the ROUTER's G0/0 Interface is:
192.168.1.254/24

The IP Address for the ROUTER's G0/1 Interface is:
192.168.2.254/24

![image](https://github.com/psaumur/CCNA/assets/106411237/6e593774-4113-4493-89bb-4d394cb29e1d)


The IP Address depends on network address of the LAN it is connects to.

The NETWORK portion of given IP Address will be the same for all HOSTS on a given LAN.

Example:

192.168.1.100
192.168.1.105
192.168.1.205

All of these addresses are on the SAME Network because the NETWORK PORTION of their IP Address is the same (192.168.1) while the HOST part (100,105,205) is UNIQUE!

When a BROADCAST message hits a ROUTER, it does NOT continue onward. It stays within the LOCAL LAN (Switch/Hosts).

---

IPv4 HEADER

![image](https://github.com/psaumur/CCNA/assets/106411237/4f4bd7da-1876-4000-8229-be4b8792a86d)


IP (or Internet Protocol) is the primary Layer 3 protocol in use today. Version 4 is the version in use in most networks.

IPv4 Headers contain MORE fields than the ETHERNET header.

IPv4 Headers contain a SOURCE IP Address and DESTINATION IP Address field.

This FIELD is 32-bits(4-bytes) in length (0-31)

192.168.1.254 (each decimal number represents 8 bits)

Translated to Binary:

11000000 . 10101000 . 00000001 . 11111110

EACH of these 8 bit groups are referred to as an OCTET

Since Binary is difficult to read for people, we use the Dotted Decimal format.

---

REVIEW of DECIMAL and HEXADECIMAL

![image](https://github.com/psaumur/CCNA/assets/106411237/e45f0ea9-a705-463b-bb9b-d81034cf130d)


Decimal (base 10)

Ex: 3294 = (3 * 1000) + (2 * 100) + (9 * 10) + (4 * 1)

Hexadecimal (base 16)

Ex: 3294, would be CDE
```
C (C * 256 / 12 * 256 = 3072) // 256ths position
D (D * 16 / D=13 so 16*13 = 208) // 16ths position
E (E * 1 / E = 14)	// 1s position
```
Adding these up, we get 3294

---

So, how do we convert a BINARY NUMBER to a DECIMAL NUMBER?
The same way we convert to Hexadecimal.

10001111

So:
```
1 * 128 = 128
1 * 8 = 8
1 * 4 = 4
1 * 2 = 2
1 * 1 = 1
```
Add them all up : 128 + 8 + 4 + 2 + 1 = 143

The answer is 143.

---

Another example:

01110110
```
1 * 64 = 64
1 * 32 = 32
1 * 16 = 16
1 * 4 = 4
1 * 2 = 2
```
Add them all up: 64 + 32 + 16 + 4 + 2 = 118

The answer is 118.

---

Another example:

11101100
```
1 * 128 = 128
1 * 64 = 64
1 * 32 = 32
1 * 8 = 8
1 * 4 = 4
```
Add them all up: 128 + 64 + 32 + 8 + 4 = 236

The answer is 236.

---

So, how do we convert a DECIMAL NUMBER to a BINARY NUMBER?

Take the number 221.

We can take that number and start subtracting it from LEFT to RIGHT of our Binary slots.

221
```
221 - 128 = 93 so we place a 1 in the "128" slot
```
10000000
```
93 - 64 = 29 so we place another 1 in the "64" slot

29 - 32 isn't possible so we place a 0 in the "32" slot

29 - 16 = 13 so we place a 1 in the "16" slot

13 - 8 = 5 so we place a 1 in the "8" slot

5 - 4 = 1 so we place a 1 in the "4" slot

1 - 2 isn't possible so we put a 0 in the "2" slot

1 - 1 is possible so we put a 1 in the "1" slot
```
This, then, allows us to the write out the BINARY number for 221.

It is : 11011101

---

Another example: 127
```
127 - 128 is not possible so 0 in "128"
127 - 64 is possible so 1 in "64"
63 - 32 is possible so 1 in "32"
31 - 16 is possible so 1 in "16"
15 - 8 is possible so 1 in "8"
7 - 4 is possible so 1 in "4"
3 - 2 is possible so 1 in "2"
1 is possible so 1 in "1"
```
So 127, in BINARY, is 0111 1111

---

Another example: 207

Alternatively, you can subtract the number from '255' (which is 1111111).
The remainder, then, can be used to "find" where the 0's are in the binary number.

255 - 207 = 48 so ...

1 1 0 0 1 1 1 1 (32 + 16 = 48)

11001111 is the correct answer.

---

IPv4 ADDRESSES

So we now know that IP Addresses are the Dotted Decimal conversion of a series of BINARY NUMBERS (broken up into 4 OCTETS) like so:

192.168.1.254/24

But what does the /24 stand for?

![image](https://github.com/psaumur/CCNA/assets/106411237/808fa7fa-0239-42fa-9706-79db87ea167e)


It means the FIRST 24 BITS of this address represent the NETWORK portion of the address.

192.168.1 is the NETWORK PORTION (the first 3 OCTETS)

.254 is the HOST PORTION (the last OCTET)

![image](https://github.com/psaumur/CCNA/assets/106411237/2e7c64e1-5689-486a-bba0-9623f5e8de7d)


---

CONVERT this BINARY number into an IPv4 Address:

10011010010011100110111100100000

10011010 . 01001110 . 01101111 . 00100000

Octets:

1. 128 + 16 + 8 + 2 = 154
2. 64 + 8 + 4 + 2 = 78
3. 64 + 32 + 8 + 4 + 2 + 1 = 111
4. 32

The IPv4 address is: 154.78.111.32/16

154.78 is the NETWORK PORTION
111.32 is the HOST PORTION

Another Example:

00001100100000001111101100010111

00001100 . 10000000 . 11111011 . 00010111

Octets:

1. 8 + 4 = 12
2. 128
3. 255 - 4 = 251
4. 16 + 4 + 2 + 1 = 23

The IPv4 address is: 12.128.251.23/8

12 is the NETWORK PORTION
128.251.23 is the HOST PORTION

---

IPv4 ADDRESS CLASSES

IPv4 ADDRESSES are split up into 5 different 'classes'.
The class of an IPv4 is determined by the FIRST OCTET of the address.

CLASS 		FIRST OCTET 		FIRST OCTET NUMBERIC RANGE

A 			 0xxxxxxx 				0-126 + 127 'loopback'
B 			 10xxxxxx 				128-191
C 			 110xxxxx 				192-223
D 			 1110xxxx 				224-239
E 			 1111xxxx 				240-255

From the above chart, if the FIRST OCTECT STARTS with 0, the numeric RANGE of possible first DOTTED DECIMAL is between 0-127.

The CLASSES we will be focusing on are CLASS A to CLASS C.

![image](https://github.com/psaumur/CCNA/assets/106411237/7cc286bf-ce76-4eee-af52-062a63dac2b4)


D CLASS are reserved for 'MULTICAST' ADDRESSES

E CLASS are reserved for 'EXPERIMENTAL' ADDRESSES

---

A CLASS USUALLY have a range of 1-126? WHY?

Because 127 is usually reserved for 'loopback addresses'

127.0.0.0 to 127.255.255.255 are used to test the network.

- Used to test the 'Network stack' (OSI & TCP/IP model) on the local device.

---

![image](https://github.com/psaumur/CCNA/assets/106411237/25f7db1a-f934-4c73-9926-66bb207fd292)


The PREFIX LENGTH is the LENGTH of the NETWORK PORTION of the Address.

From the examples above:

12.128.251.23/8 is a CLASS A Address
154.78.111.32/16 is a CLASS B Address
192.168.1.254/24 is a CLASS C Address

Because the NETWORK portion of CLASS A is so short, it means there are a LOT more potential Hosts.

Because the NETWORK portion of CLASS C is so long, it means fewer potential Hosts.

---

NETMASK

![image](https://github.com/psaumur/CCNA/assets/106411237/874c022f-9b8c-4862-a495-597682b014a4)


A NETMASK is written like a Dotted Decimal IP Address

CLASS A: /8 = 255.0.0.0

CLASS B: / 16 = 255.255.0.0

CLASS C: /24 = 255.255.255.0

---

NETWORK ADDRESSES

![image](https://github.com/psaumur/CCNA/assets/106411237/12178b46-2604-468b-a11c-2a94087b023d)


If the HOST PORTION of an IP ADDRESS is ALL 0's, it means it is the NETWORK ADDRESS = the identifier of the network itself.

Example: 192.168.1.0/24 = THIS is a NETWORK ADDRESS.

A NETWORK ADDRESS cannot be assigned to a HOST.
A NETWORK ADDRESS is the FIRST ADDRESS.

![image](https://github.com/psaumur/CCNA/assets/106411237/53eafb43-2a6f-422c-af19-866946d78efa)


If the HOST PORTION of an IP ADDRESS is ALL 1's, it means it is the BROADCAST ADDRESS for the network.

A BROADCAST ADDRESS cannot be assigned to a HOST.

DESTINATION IP : 192.168.1.255 (Broadcast IP address)
DESTINATION MAC : FFFF.FFFF.FFFF (Broadcast MAC address)

Because of the two 'reserved' addresses, the range of USABLE HOST ADDRESSES is 1 to 254.

# 8. IPv4 ADDRESSING : PART 2

MAXIMUM HOSTS PER NETWORK

Let's take a Class C Network:

192.168.1.0/24

(gives a range of 0 ---> 255)

Said another way, the HOST portion (the .0) is equal to 8 bits so...

Host portion = 8 bits = 2^8 = 256

HOWEVER, since the Network Address (Network ID)

192.168.1.0 is Reserved

AND

192.168.1.255 (BROADCAST ADDRESS) is ALSO reserved.

The MAXIMUM Hosts per Network = 2^8-2 = 254 hosts

---

What about a Class B Network ?

172.16.0.0/16 ----> 172.16.255.255/16

Host portion = 16 bits = 2^16 = 65,536

Maximum hosts per network = 2^16-2 = 65,534 hosts

---

What about a Class A Network ?

10.0.0.0/8 -------------> 10.255.255.255/8

Host portion = 24 bits = 2^24 = 16,777,216

Maximum hosts per network = 2^24-2 = 16,777,214 hosts

---

THEREFORE:

The formula for calculating the number of HOSTS on a network is:

2 ^ N - 2 (2 to the power of N - 2)

where N = number of HOST bits

---

FIRST / LAST USABLE ADDRESSES

Class C Network

192.168.1.0/24 (NETWORK ADDRESS)

Add 1 so the Host Portion = 00000001

192.168.1.1/24 = FIRST USABLE ADDRESS

---

192.168.1.255/24 (BROADCAST ADDRESS)

Subtract 1 from the BROADCAST ADDRESS = 11111110

192.168.1.254/24 = LAST USABLE ADDRESS

---

Class B Network

172.16.0.0/16 (NETWORK ADDRESS)

Add 1 to Host portion so 0000 0000 0000 0001

172.16.0.1/16 is the FIRST USABLE ADDRESS

---

172.16.255.255/16 (BROADCAST ADDRESS)

Subtract 1 to Broadcast Address so 1111 1111 1111 1110

172.16.255.254/16 is the LAST USABLE ADDRESS

---

Class A Network

10.0.0.0/8 (NETWORK ADDRESS)

Add 1 to Host portion so 00000000 00000000 00000001

10.0.0.1/8 is the FIRST USABLE ADDRESS

---

10.255.255.255/8 (BROADCAST ADDRESS)

Subtract 1 to Broadcast Address so 1111 1111 1111 1110

10.255.255.254/16 is the LAST USABLE ADDRESS

---

CISCO CLI DEVICE CONFIGURATION

R1> enable
R1# show ip interface brief

Lists the Interfaces, IP Addresses, Method, Status, and Protocol.

Interfaces:

- What port interfaces are available/connected

IP Addresses

- Self explanatory. What IP Address is assigned.

Method

- What method was the IP address assigned?

Status (Layer 1 Status)

- Current status of interface
- 'administratively down' = Interface has been disabled with the 'shutdown' command

Administratively down is the DEFAULT status of Cisco Router interfaces.

Cisco Switch interfaces are NOT administratively down by DEFAULT.

Protocol (Layer 2 Status)

- Cannot operate if Status (Layer 1) is down
  
![image](https://github.com/psaumur/CCNA/assets/106411237/fa113ff0-a8ee-410b-ab3e-64684654cac6)


---

// configure terminal cmd

R1# conf t

// This enters interface configuration mode

R1(config)# interface gigabitethernet 0/0

This can be shortened to 'g0/0' like they are listed in physical network maps.

![image](https://github.com/psaumur/CCNA/assets/106411237/df83bf09-c391-45b7-b1b4-41db061b84f4)


// This sets the IP ADDRESS and SUBNET MASK of device

R1(config-if) #ip address 10.255.255.254 255.0.0.0

// This enables the device

R1(config-if) #no shutdown

---

Two messages should appear showing the state has changed to 'up' (Status). Second message should show line protocol is now 'up' (Protocol).

// 'do' allows you to run a Privileged EXEC command from outside the mode.

R1(config-if) #do show ip interface brief

Good to confirm that the device/interface you have configured is up and running.

---

More 'show' CLI Commands

![image](https://github.com/psaumur/CCNA/assets/106411237/bdc1152e-1946-4ddb-ae72-1e23b9c9defa)


'show interfaces <interface name>'

- Shows Layer 1 and Layer 2 information about the interface and some Layer 3.
- Shows MAC Address (or BIA address)
- IP Address
- ... and so much more

'show interfaces description'

- Allows you to add descriptions for interfaces.

Example:

// Configure mode for interface Gigabyte Interface 0/0

R1(config) #int g0/0

R1(config) #description ## to SW1 ##

This sets the 'Description' column to display:

Interface 				Description

Gi0/0                   ## to SW1 ##

# 9. SWITCH INTERFACES

![image](https://github.com/psaumur/CCNA/assets/106411237/5d0d80dc-74d1-4656-841c-fcaa2b89c760)


CISCO CLI for SWITCHES

![image](https://github.com/psaumur/CCNA/assets/106411237/e3947ef5-9100-426f-8d62-fd4ce5224351)


// enter Privileged EXEC mode

SW1>enable

// Show all interfaces of Switch 1.

SW# show ip interface brief

This will show the interfaces currently on Switch 1. It has the same information structure as Cisco Routers.

Notice the Status (Layer 2) and Protocol (Layer 1) columns are showing "up/up".

Unlike ROUTERS, SWITCHES do no DEFAULT to 'administrative down/down'(shutdown).

Unconnected devices will show as "down" and "down" (not connected to another device)

![image](https://github.com/psaumur/CCNA/assets/106411237/e0fdc339-21d9-4313-b7d8-78303a7ba1ea)


// Show the status of all interfaces on SW1

SW1#show interfaces status

This will list:

- Ports
- Name (which is description)
- Status (connection status)
- Vlan (can be used to divide up LANs) - Vlan 1 is the default.
- Duplex (can the connection send/receive at same time?) - Auto is default
- Speed (speed in bps) - Auto is default
- Type (what medium is being used, speed of interface)

---

![image](https://github.com/psaumur/CCNA/assets/106411237/12a33be7-795f-467a-87a4-42c5b218960b)


![image](https://github.com/psaumur/CCNA/assets/106411237/7b5953f7-77d3-4826-8efc-072498a7f9c0)


---

INTERFACE RANGE

Unused Interfaces can pose a security risk so it's a good idea to deactivate them.

However, if you have 28+ interfaces not in use, do you have to do them one at a time?

Answer: No! There is a command to apply configurations to a range of interfaces.

Inside Global Config Mode (config t):

![image](https://github.com/psaumur/CCNA/assets/106411237/06e2e267-1e07-48a1-8c8c-8edbd5bd48ae)


SW1(config)#interface range f0/5 - 12   // Choose all interfaces from 0/5 to 0/12

SW1(config-if-range)#description ## not in use ##

SW1(config-if-range)#shutdown

<< this will list all the interfaces being set to administratively down >>

Confirm with 'show interface status' in Privileged EXEC mode or if in CONFIG mode, use 'do show interface status'

![image](https://github.com/psaumur/CCNA/assets/106411237/8d1d49d3-e000-4570-ab7e-b994b959ebd5)

---

FULL / HALF DUPLEX

HALF DUPLEX:

- Device cannot send / receive data at the same time. If it is receiving a frame, it must wait before sending a frame.

FULL DUPLEX:

- Device CAN send / receive data at the same time. It does NOT have to wait.

MOST modern SWITCHES support FULL DUPLEX.

---

WHERE is HALF DUPLEX used? Almost nowhere.

In the past, LAN HUBS used HALF DUPLEX.

When multiple packets were received by the HUB, the HUB would simple FLOOD the connections with frame data, causing a COLLISION (on the interface), and hosts would not receive the frame  intact.

All devices connected to a HUB are called a COLLISION DOMAIN.

To DEAL with COLLISIONS, Ethernet devices use a mechanism called CSMA/CD.

CSMA/CD = CARRIER SENSE MULTIPLE ACCESS with COLLISION DETECTION.

- Before sending frames, devices 'listen' to the collision domain until they detect that other devices are not sending.
- IF a collision occurs, the device sends a jamming signal to inform the other devices that a collision happened.
- Each device will wait a random period of time before sending frames again.
- The process repeats.

---

SWITCHES are more sophisticated than HUBS.

HUBS are Layer 1 Devices - Collisions are common and use CSMA/CD.
SWITCHES are Layer 2 Devices - Collisions RARELY occur.

---

![image](https://github.com/psaumur/CCNA/assets/106411237/feff3816-1449-4282-bc44-71575333a1e0)


SPEED / DUPLEX AUTONEGOTIATION

- Interfaces that can run at different speeds (10/100 or 10/100/1000) have a default setting of SPEED AUTO and DUPLEX AUTO.
- Interfaces 'advertise' their capabilities to the neighbouring device, and they negotiate the best SPEED and DUPLEX settings they are both capable of.

WHAT if AUTONEGOTIATION is DISABLED on the device connected to the SWITCH ?

![image](https://github.com/psaumur/CCNA/assets/106411237/30519cf7-0a79-4996-a8d8-dfac689f4005)


- SPEED: The SWITCH will try to send at the speed that the other device is operating at.
If it fails to send the speed, it will use the slowest supported speed (ie: 10 Mbps on a 10/100/1000 interface).
- DUPLEX: If the speed is 10 or 100 Mbps the SWITCH will use HALF DUPLEX.
If the speed is 1000 Mbps or great, it will use FULL DUPLEX.

---

INTERFACE COUNTERS AND ERRORS

Show using the:

// Privileged EXEC mode

SW1#show interfaces <interface name>

Error stats will be at the bottom.

![image](https://github.com/psaumur/CCNA/assets/106411237/20d6affd-6014-427d-9ad9-c638ace358f8)


**Packets Received / Total bytes received.**

**Runts**: Frames that are smaller than the minimum frame size (64 bytes)

**Giants**: Frames that are larger than the maximum frame size (1518 bytes)

**CRC**: Frames that failed the CRC check (in the Ethernet FCS trailer)

**Frame**: Frames that have an incorrect format (due to an error)

**Input errors**: Total of various counters, such as the above four

**Output errors**: Frames the SWITCH tried to send, but failed due to an error

# 10. THE IPv4 HEADER

INTERNET PROTOCOL version 4 HEADER or IPv4 HEADER

HEADER is used at LAYER 3 to help send data between devices on separate networks, even on other sides of the world over the Internet.

This is known as ROUTING.

THE IPv4 HEADER is used to ENCAPSULATE a TCP or UDP Segment.

To Review:

![image](https://github.com/psaumur/CCNA/assets/106411237/64906e3c-0bae-4c2c-96ca-4e6850f3844a)


---

FIELDS OF THE IPv4 HEADER

![image](https://github.com/psaumur/CCNA/assets/106411237/f2667488-2769-4e62-bee7-eddbf9e00058)


| FIELD | # OF BITS |
| --- | --- |
| VERSION | 4 |
| IHL | 4 |
| DSCP | 6 |
| ECN | 2 |
| TOTAL LENGTH | 16 |
| IDENTIFICATION | 16 |
| FLAGS | 3 |
| FRAGMENT OFFSET | 13 |
| TIME TO LIVE | 8 |
| PROTOCOL | 8 |
| HEADER CHECKSUM | 16 |
| SOURCE ADDRESS | 32 |
| DESTINATION ADDRESS | 32 |
| OPTIONS | 320 Max |

---

VERSION:

- LENGTH is 4 bits.
- IDs version of IP used (IPv4 or IPv6)
    - IPv4 = 0100 in Binary (Decimal 4)
    - IPv6 = 0110 in Binary (Decimal 6)

---

INTERNET HEADER LENGTH (IHL):

- LENGTH is 4 bits.
- Final field of IPv4 Header (Options) is variable in length so this field is necessary to indicate the total length of the header.
- IDs the length of the header in 4-BYTE INCREMENTS.
- The MINIMUM value is 5 (5 * 4-bytes = 20 bytes) - Empty OPTIONS Field
- The MAXIMUM value is 15 (15 * 4-bytes = 60 bytes)

MINIMUM IPv4 HEADER LENGTH = 20 Bytes!
MAXIMUM IPv4 HEADER LENGTH = 60 Bytes!

---

DSCP (Differentiated Services Code Point):

- LENGTH is 6 bits.
- Used for QoS (Quality of Service)
- Used to prioritize delay-sensitive data (streaming voice, video, etc.)

---

ECN (Explicit Congestion Notification):

- LENGTH is 2 bits.
- Provides end-to-end (between two endpoints) notification of network congestion WITHOUT dropping packets.
- Optional feature that requires both endpoints, as well as the underlying network infrastructure to support it.

---

TOTAL LENGTH:

- LENGTH is 16 bits.
- Indicates the TOTAL length of the packet (L3 Header + L4 Segment)
- Measured in bytes (not 4-byte increments like IHL)
- Minimum value of 20 Bytes (IPv4 Header with NO encapsulated data)
- Maximum value of 65,535 (MAXIMUM 16-bit value) = 2^16

---

IDENTIFICATION:

- LENGTH is 16 bits.
- If a packet is fragmented due to being too large, this field is used to identify which packet the fragment belongs to.
- All fragments of the same packet will have their own IPv4 header with the same value in this field.
- Packets are fragmented, if larger than the MTU (Maximum Transmission Unit)
- The MTU is usually 1500 bytes (Max size of an Ethernet frame)
- Fragments are reassembled by the receiving host.

---

FLAGS:

- LENGTH is 3 bits
- Used to control/identify fragments.
- Bit 0: Reserved, always set to 0.
- Bit 1: Don't Fragment (DF bit), used to indicate a packet that should not be fragmented.
- Bit 2: More Fragments (MF bit), set to 1 if there are more fragments in the packet, set to 0 for the last fragment or NO fragments.

---

FRAGMENT OFFSET:

- LENGTH is 13 bits
- Used to indicated the position of the fragment within the original, unfragmented IP Packet.
- Allows fragmented packets to be reassembled even if the fragments arrive out of order.

---

TIME TO LIVE (TTL):

- LENGTH is 8 bits
- A router will drop a packet with a TTL of 0
- Used to prevent infinite loops
- Originally designed to indicated a packets maximum lifetime in seconds.
- In practice, indicates a 'hop count': each time the packet arrives at a router, the router decreases the TTL by 1.
- Recommended default TTL is 64.

---

PROTOCOL:

- LENGTH is 8 bits
- Indicates the protocol of the encapsulated Layer 4 PDU
- Value of 1 : ICMP
- Value of 6 : TCP
- Value of 17 : UDP
- Value of 89 : OSPF (Dynamic Routing Protocol)
- List of protocol numbers on Wikipedia : List of IP Protocol Numbers

HEADER CHECKSUM:

- LENGTH is 16 bits
- A calculated checksum used to check for errors in the IPv4 header.
- When a router receives a packet, it calculates the checksum of the header and compares it to the one in this field of a header.
- If they do not match, the router drops the packet.
- Used to check for ERRORS only in the IPv4 Header.
- IP relies on the encapsulated protocol to detect errors in the encapsulated data.
- Both TCP and UDP have their own checksum fields to detect errors in the encapsulated data.

---

SOURCE and DESTINATION:

- LENGTH is 32 bits each
- SOURCE IP = IPv4 ADDRESS of the Sender of the Packet.
- DESTINATION IP = IPv4 ADDRESS of the intended Receiver of the Packet.

---

OPTIONS:

- LENGTH is 0-320 bits
- Optional / Rarely Used
- If the IHL field is greater than 5, it means that Options are present.

# 11. ROUTING FUNDAMENTALS : PART 1




### WHAT IS ROUTING ?



ROUTING is the process that routers use to determine the path that IP packets should take over a network to reach their destination.

- ROUTERS store routes to all their known destinations in a ROUTING TABLE
- When ROUTERS receive PACKETS, they look in the ROUTING TABLE to find the best route to forward that packet.

There are two main routing methods (methods that routers use to learn routes):

- DYNAMIC ROUTING : ROUTERS use Dynamic Routing Protocols (ie: OSPF) to share routing information with each other automatically and build their routing tables.
- STATIC ROUTING : A network engineer / Admin manually configures routes on the router.

A ROUTE tells the ROUTER :

- to send a packet to Destination X, you should send the pack to ***next-hop*** Y
- or if the Destination is directly connected to the router, *send the packet directly to the destination.*
- or if the Destination is the router’s own IP address, *receive the packet for yourself (don’t forward it).*

![image](https://github.com/psaumur/CCNA/assets/106411237/8ceefb10-d70d-4530-969d-40347ed34297)


WAN (Wide Area Network) = network that extends over a large geographic area.

![image](https://github.com/psaumur/CCNA/assets/106411237/b3555fdd-37a4-4bc8-b998-76e0b5455bb1)

![image](https://github.com/psaumur/CCNA/assets/106411237/99e75230-de1c-4f48-acd0-3482bba256af)

![image](https://github.com/psaumur/CCNA/assets/106411237/13a77d5c-497d-49ca-9717-ea3bb4a560d0)

![image](https://github.com/psaumur/CCNA/assets/106411237/6e3a2b3b-1590-4625-9bcf-cdaed95738d2)

![image](https://github.com/psaumur/CCNA/assets/106411237/891fcfbe-7dc5-4fb2-9b02-c6905236761e)

# 11. STATIC ROUTING : PART 2

REVIEW:

SWITCHES forward traffic WITHIN LAN's
ROUTERS forward traffic BETWEEN LAN's

WAN (Wide Area Network)

- Network spread over a large area

![image](https://github.com/psaumur/CCNA/assets/106411237/e44ac71c-91e3-4963-85da-ac07e475b248)


![image](https://github.com/psaumur/CCNA/assets/106411237/289212da-6c94-44fb-a1e3-1c066b56d79c)


![image](https://github.com/psaumur/CCNA/assets/106411237/f8f7d58b-89b7-412c-9cf6-c038338e105d)


![image](https://github.com/psaumur/CCNA/assets/106411237/63611407-719e-46d3-8331-a18533616285)

---

STATIC ROUTES:

![image](https://github.com/psaumur/CCNA/assets/106411237/10135afa-ace6-47f1-aada-1b73f243589b)

---

STATIC ROUTE CONFIGURATION:

![image](https://github.com/psaumur/CCNA/assets/106411237/d375a428-e171-4212-9698-2f2589878884)


![image](https://github.com/psaumur/CCNA/assets/106411237/012f4134-2667-421b-9b36-f449faebf423)


![image](https://github.com/psaumur/CCNA/assets/106411237/0a3ed6cb-c414-4365-aef4-754b4b82483e)


![image](https://github.com/psaumur/CCNA/assets/106411237/4379f8fb-a366-4279-a31c-ff2ba3f6fdb8)


![image](https://github.com/psaumur/CCNA/assets/106411237/6fed6489-c53c-404e-b794-b71c2e9b8e4f)

---

STATIC ROUTE CONFIGURATION with *exit-interface*

![image](https://github.com/psaumur/CCNA/assets/106411237/dc93b5f9-791c-44fc-8b88-2053491183a9)

---

DEFAULT ROUTE

![image](https://github.com/psaumur/CCNA/assets/106411237/a0eef93a-b40b-409b-8b51-6cdbace4ff45)

# 12. LIFE OF A PACKET

![image](https://github.com/psaumur/CCNA/assets/106411237/ec16b9fd-4d90-4b73-b930-cd825ff13b00)


EACH Network device's interfaces have a UNIQUE MAC Addresses.

In a TCP HEADER

SOURCE IP ADDRESS comes before DESTINATION IP ADDRESS

while...

in an ETHERNET HEADER

DESTINATION MAC ADDRESS comes before SOURCE MAC ADDRESS

---

![image](https://github.com/psaumur/CCNA/assets/106411237/5eb94811-32f3-47f6-884e-f45a71456e84)


![image](https://github.com/psaumur/CCNA/assets/106411237/dc0d05cc-9b76-4921-895d-bfbe78ceb0a7)


![image](https://github.com/psaumur/CCNA/assets/106411237/884f7113-21a9-407f-a38e-44489ae3b47e)


![image](https://github.com/psaumur/CCNA/assets/106411237/36459aeb-e802-4347-b626-0c9cc168c624)


![image](https://github.com/psaumur/CCNA/assets/106411237/163bfaf6-15c7-4f7d-9429-4c62a28f0292)


![image](https://github.com/psaumur/CCNA/assets/106411237/1f7e5683-00e6-4ce0-b52a-ca8fdb24c87b)


![image](https://github.com/psaumur/CCNA/assets/106411237/18d04c9d-3734-44e7-995d-b53ab3aaa2a1)


![image](https://github.com/psaumur/CCNA/assets/106411237/07c44007-a208-47a2-a0e8-ca289f86be75)


![image](https://github.com/psaumur/CCNA/assets/106411237/4bcbdba0-234a-4cfa-aa25-cbc3c3c061e1)


![image](https://github.com/psaumur/CCNA/assets/106411237/81c2e8ad-be55-487c-b9da-02540f70b0d9)


![image](https://github.com/psaumur/CCNA/assets/106411237/91cfe407-28b5-48e8-b5f8-a60b324e0706)


![image](https://github.com/psaumur/CCNA/assets/106411237/4bf8c10b-1240-4e7d-8db4-85ea5f3f619f)


![image](https://github.com/psaumur/CCNA/assets/106411237/f938e440-ebdb-444c-b4c7-705d8fd2a4e9)


![image](https://github.com/psaumur/CCNA/assets/106411237/1f236bda-d2cf-4252-af3b-bdc5ec5c2aca)


When a HOST sends a packet to another HOST, the SOURCE or DESTINATION IP doesn't change - even though ROUTERS may change the ETHERNET HEADER (SRC/DEST MAC ADDRESSES).

# 13. SUBNETTING : PART 1

![image](https://github.com/psaumur/CCNA/assets/106411237/a475e909-59b8-4615-a0b9-8a3c1fbdc313)


HOWEVER, only Class A, B, C Addresses can be assigned to a device as an IP Address.

CLASS 		PREFIX LENGTH

A 			/8
B 			/16
C 			/24

![image](https://github.com/psaumur/CCNA/assets/106411237/f0836136-c4a9-475b-b6c2-d1c550b8cfdd)


The IANA (Internet Assigned Numbers Authority) assigns IPv4 addresses/networks to companies based on their size.

The problem with 'CLASSFUL' assignment is that it led to IP Address wastefulness.

Example: A company requiring 5000 address was assigned a CLASS B IP, leaving 60000+ addresses unused.

---

The IETF (Internet Engineering Task Force) introduce CIDR in 1993 to replace the "classful" addressing system.

CIDR (Classless Inter-Domain Routing) removed the requirements of CLASS A, B, and C regarding size.

- This allowed larger networks to be split into smaller networks, allowing greater efficiency.
- These smaller networks are called "SUB-NETWORKS" or "SUBNETS"

---

HOW MANY USABLE ADDRESSES ARE THERE IN EACH NETWORK?

REMEMBER:

2^n - 2 = Usable Address
n = number of host bits

CIDR PRACTICE!

203.0.113.0/25

/25 means the Subnetwork bit is 25 bits

203 . 0 . 113 . 0 is written in binary as :

1100 1011 . 0000 0000 . 0111 0001 . 0 | 000 0000

(Subnet prefix is the first 25 bits)

Flipping all the bits to 1’s, we get the SUBNET MASK for /25:

1111 1111 . 1111 1111 . 1111 1111 . 1 | 000 0000

which is equal to:

255.255.255.128 (because the last octet is 1000 0000 = 128 in binary)

SO - the based on previous definition of USABLE ADDRESSES, the number of hosts for
203.0.113.0 /25 is:

2^(7 bits) or (128) - 2 = 126 hosts.

---

What about /28 ?

203 . 0 . 113 . 0 is written in binary as :

1100 1011 . 0000 0000 . 0111 0001 . 0000 | 0000

(Subnet prefix is the first 28 bits)

flipping all the bits to 1’s, we get the SUBNET MASK for /28:

1111 1111 . 1111 1111 . 1111 1111 . 1111 | 0000

which is equal to:

255.255.255.240 (because the last octet is 1111 0000) = 128+64+32+16 =  (128+32) + (64+16) = 160 + 80 = 240

The SUBNET MASK for /28 is 255.255.255.240
which has 16 hosts / group (2 * 4 bits = 16) - 2 Reserved IPs for Network and Broadcast 

---

SUBNETTING CHEATSHEET:

| Group Size | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Subnet Mask | 128 | 192 | 224 | 240 | 248 | 252 | 254 | 255 |
| CIDR | /25 | /26 | /27 | /28 | /29 | /30 | /31 | /32 |
| 3rd Octet | /17 | /18 | /19 | /20 | /21 | /22 | /23 | /24 |
| 2nd Octet | /9 | /10 | /11 | /12 | /13 | /14 | /15 | /16 |
| 1st Octet | /1 | /2 | /3 | /4 | /5 | /6 | /7 | /8 |

---

1. Use a given CIDR/Mask to find column on Cheat Sheet
    
    a) CIDR/Subnet Mask map to each other
    
    b) Locate Group Size
    
    c) Increase by Group Size until you PASS the Target IP (not less or equal !)
    
    d) If passing the Target IP reaches 256, increase the Octet BEFORE it by one and current Octet becomes 0 : IF NECESSARY
    
    Example: 10.2.2.256 → 10.2.3.0
    

1. Number BEFORE Target IP is NETWORK ID
2. Number AFTER Target IP is NEXT NETWORK
3. IP Address BEFORE Next Network is BROADCAST
4. IP Address AFTER Network ID is First Host
5. IP Address BEFORE Broadcast IP is Last Host
6. Group Size is total # of IP Addresses
    - Don’t forget to subtract 2 for USABLE #

---

Solving CIDR/Subnet for 3rd Octet IPs :

Every number LEFT of 3rd Octet is 255. Every number RIGHT of 3rd Octet is 0

Example: 10.4.77.188 / 19 → Subnet : 255.255.224.0

You use the SAME process as above except when finding Target IPs, you use the 3rd Octet for your Target.

Example: 10.4.77.188 /19 → Subnet : 255.255.224.0

256 - 224 = 32 so…

Using 32, we step through the address blocks 0, 32,64, and 96.
Since 77 is between 64 and 96, there’s our range.

Network: 10.4.64.0 (Start / First Block)

Next: 10.4.96.0 (Second Block)
…

Number of IP Addresses is : 2^(32-CIDR). In this example 2^13 = 8192

Solving for 2nd and 1st Octet is the same as above, keeping in mind the Octet column is USED to check for the Target number of a given address.

---
Alternative method to "Cheat Sheet"

![image](https://github.com/user-attachments/assets/d1e103b8-142a-44cc-8ab4-f5337268c9de)

1. Find the "magic octet" where a given IP /Prefix lies, from the bit chart shown (boundary digits are inclusive of the octet preceding them)
2. Count the number of network bits (left to right) in that octet and count the same amount, using the red bit slot chart. This'll be your address group size.
3. Subtract that number from 256 to find your Subnet Mask number used in the "magic octet" (any octet LEFT of that "magic octet" will be 255, everything RIGHT of that octet will be 0)
4. Divide whatever IP octet number is in the "magic octet" by the address group size.
  - If there is a remainder, multiple the whole integer by the address group size - your Base Network Address is that value, with every octet to the right of that as all 0's
  - If there is NO remainder, the IP number in the "magic octet" IS the Base Network Address is that value, with every octet to the right of that as all 0's
5. The Base Broadcast Number will be Network Base Number + Group Size - 1 in the "magic octet", every value to the right of that octet will be 255.
6. Number of subnets is (2 to the power of the number of network bits in the "magic octet". ** 2^8 or 256 is equal to 0 **)
7. Total Useable Hosts size is (2 to the power of (32 - Prefix Length) -2)
---
Example 1:
```
154 . 219 . 154 . 180 /20

Third Octet = Magic

Address Group Size = 16 (L/R count of 4)
256 - 16 = 240 therefore Subnet Mask is 255.255.240.0

Divide 3rd digit / Address Group Size (16)
154 / 16 = 9 (with remainder)
9 * 16 = 144 (Base Network #)

Network : 154 . 219 . 144 . 0

Broadcast Base # = 144 + 16 - 1 = 159

Broadcast : 154. 219 . 159 . 255

Subnets = 2^4 network bits = 16
Total Host Size = (2^(32 - 20))-2 = 4094
```
---
Example 2:
```
84 . 75 . 21 .6 /10

Second Octet = Magic

Address Group Size = 64
256 - 64 = 192

Subnet = 255.192.0.0

75 / 64 = 1 + remainder
1 * 64 = 64 (Base Network #)

Network : 84.64.0.0

Broadcast Base # = 64 + 64 -1 = 127

Broacast : 84.127.255.255

Subnets : 2^2 = 4 Subnets
Total Host Size = (2^(32-10))-2 = 4194302
```

# 14. SUBNETTING : PART 2

CLASS C NETWORKS

![image](https://github.com/psaumur/CCNA/assets/106411237/08be5a37-fa2c-4483-94c9-6c3d05229894)


CLASS B NETWORKS

![image](https://github.com/psaumur/CCNA/assets/106411237/44e8cdcb-16c2-41c4-8f22-a0a31071550a)

# 15. SUBNETTING (VLSM) : PART 3

The process of subnetting Class A, Class B, and Class C is identical.

SUBNETTING CLASS A NETWORKS

Given a 10.0.0.0/8 network, you must create 2000 subnets which will distributed to various enterprises. What prefix length must you use?

2^10 = 1024 so 2^11 = 2048. We have to "borrow" 11 bits (Left to Right) to get enough subnets

0000 1010 . 0000 0000 . 000 | 00000 . 0000 0000

8 bits + 8 bits + 3 = 19 bits

0000 1010 . 0000 0000 . 000 | 00000 . 0000 0000
1111 1111 . 1111 1111 . 111 | 00000 . 0000 0000

255.255.224.0 is the Subnet mask

The answer is /19 (/8 + /11 = /19)

How many hosts per subnet? There are 13 host bits remaining so:

2^13 - 2 = 8190 hosts per subnet

---

VARIABLE-LENGTH SUBNET MASKS (VLSM)

- Until now, we have practiced subnetting using FLSM (Fixed-Length Subnet Masks).
- This means that all of the subnets use the same prefix length (ie: Subnetting a Class C network into 4 subnets using /26)
- VLSM (Variable-Length Subnet Masks) is the process of creating subnets of different sizes, to make your use of network addresses more efficient.
- VLSM is more complicated than FLSM, BUT it's easy if you follow the steps correctly.

![image](https://github.com/psaumur/CCNA/assets/106411237/30a08f93-796a-4fe9-854e-58af0bcbd69b)

![image](https://github.com/psaumur/CCNA/assets/106411237/ad7d7ac0-5e00-4662-8192-f7f9db86f1d9)

![image](https://github.com/psaumur/CCNA/assets/106411237/dc006342-4bd9-40d4-b1c5-9ac7a670ed96)


So, in order:
```
TOKYO LAN A (110 HOSTS)
TORONTO LAN B (45 HOSTS)
TORONTO LAN A (29 HOSTS)
TOKYO LAN B (8 HOSTS)
and
THE POINT TO POINT CONNECTION (between the two ROUTERS)
```
192.168.1.0 / 24

1000 0000 . 1010 1000 . 0000 0001 | 0000 0000  (last is host octet = 254 usable hosts)

Shifting LEFT - we DOUBLE the # of hosts
Shifting RIGHT - we HALF the # of hosts

TOKYO LAN A (we need to borrow 1 host bits, to the RIGHT, to leave enough for 2^7 or 128 hosts. More than enough for TOKYO A)

so:
```
192.168.1.0/25 (Network Address)
1000 0000 . 1010 1000 . 0000 0001 . 0 | 000 0000

Converting remaining Host Bits to 1s:
0111 1111, we get 127 so

192.168.1.127/25 is the Broadcast Address
```
---
TOKYO LAN A
```
NETWORK ADDRESS: 192.168.1.0/25
BROADCAST ADDRESS: 192.168.1.127/25
FIRST USABLE: 192.168.1.1/25
LAST USABLE: 192.168.1.126/25
TOTAL NUMBER OF USABLE HOSTS: 126 (2^7 -2)

Since TOKYO LAN A is 192.168.1.127, the next Subnet (TOKYO LAN B) starts at 192.168.1.128 (Network Address)
```
---
TORONTO LAN B
```
NETWORK ADDRESS: 192.168.1.128 / 26
BROADCAST ADDRESS: 192.168.1.191 / 26
FIRST USABLE: 192.168.1.129 /26
LAST USABLE: 192.168.1.190 / 26
TOTAL NUMBER OF USABLE HOSTS: 62 (2^6 -2)
```

We need to borrow to get enough for 45 hosts.

|128|64|32|16|8|4|2|1|
|---|--|--|--|-|-|-|-|
|x  |x | 0| 0|0|0|0|0|
```
1000 0000 . 1010 1000 . 0000 0001 . 10 | 00 0000

192 . 168 . 1 . 128

1000 0000 . 1010 1000 . 0000 0001 . 10 | 11 1111

192 . 168 . 1 . 191 (Broadcast Address)
```
---

TORONTO LAN A

We need to borrow to get enough for 29 hosts.

|128|64|32|16|8|4|2|1|
|---|--|--|--|-|-|-|-|
|x  |x | x| 0|0|0|0|0|
```
1000 0000 . 1010 1000 . 0000 0001 . 110 | 0 0000

192.168.1.192 (Net Address)

1000 0000 . 1010 1000 . 0000 0001 . 110 | 1 1111

192.168.1.224 (Broadcast address)

NETWORK ADDRESS: 192.168.1.192 / 27
BROADCAST ADDRESS: 192.168.1.223 / 27
FIRST USABLE: 192.168.1.193 /27
LAST USABLE: 192.168.1.222 / 27
TOTAL NUMBER OF USABLE HOSTS: 30 hosts (2^5 - 2)
```
---

TOKYO LAN B
We need to borrow to get enough for 8 hosts. Remember total usable hosts is equal to x - 2.

|128|64|32|16|8|4|2|1|
|---|--|--|--|-|-|-|-|
|x  |x | x| x|0|0|0|0|
```
1000 0000 . 1010 1000 . 0000 0001 . 1110 | 0000

192.168.1.224 (Net Address)

1000 0000 . 1010 1000 . 0000 0001 . 1110 | 1111

192.168.1.239 (Broadcast address)

NETWORK ADDRESS: 192.168.1.224 / 28
BROADCAST ADDRESS: 192.168.1.239 / 28
FIRST USABLE: 192.168.1.225 /28
LAST USABLE: 192.168.1.238 / 28
TOTAL NUMBER OF USABLE HOSTS: 14 hosts (2^4 - 2)
```
---

POINT TO POINT CONNECTIONS

We need to borrow to get enough for 4 hosts. Remember total usable hosts is equal to x - 2.
|128|64|32|16|8|4|2|1|
|---|--|--|--|-|-|-|-|
|x  |x | x| x|x|x|0|0|
```
1000 0000 . 1010 1000 . 0000 0001 . 1111 00 | 00

192.168.1.240 (Net Address)

1000 0000 . 1010 1000 . 0000 0001 . 1111 00 | 11

192.168.1.243 (Broadcast address)

NETWORK ADDRESS: 192.168.1.240 / 30
BROADCAST ADDRESS: 192.168.1.243 / 30
FIRST USABLE: 192.168.1.241 / 30
LAST USABLE: 192.168.1.242 / 30
TOTAL NUMBER OF USABLE HOSTS: 2 hosts (2^2 - 2)
```
---

ADDITIONAL PRACTICE FOR SUBNETTING

[http://www.subnettingquestions.com](http://www.subnettingquestions.com/)
[http://subnetting.org](http://subnetting.org/)
[https://subnettingpractice.com](https://subnettingpractice.com/) *** Preferred site ***

# 16. VLANS : PART 1

WHAT IS A LAN ? 

- A LAN is a single BROADCAST DOMAIN, including all devices in that broadcast domain.

BROADCAST DOMAINS

- A BROADCAST DOMAIN is the group of devices which will receive a BROADCAST FRAME (Destination MAC : FFFF.FFFF.FFFF) sent by any one of the members.

Image of LAN with FOUR BROADCAST DOMAINS (192.168.1.0 / 24)

![image](https://github.com/psaumur/CCNA/assets/106411237/de712483-e881-41f5-9525-576216186498)


Performance :

Lots of unnecessary BROADCAST traffic can reduce network performance.

![image](https://github.com/psaumur/CCNA/assets/106411237/a807fdc5-27b9-4735-8b8d-51bdc0c91a8c)


BROADCAST FRAME flooding all our subnets with unnecessary traffic.

![image](https://github.com/psaumur/CCNA/assets/106411237/fcd03904-a193-4423-8940-09be1df1bd2c)


Security :

Even within the same office, you want to limit who has access to what. You can apply security policies on a ROUTER / FIREWALL. Because this is one LAN, PC’s can reach each other directly, without traffic passing through the router. So, even if you configure security policies, they won’t have any effect.

![image](https://github.com/psaumur/CCNA/assets/106411237/7bd562fc-7dff-4692-81d7-c026b007df8f)

---

WHAT IS A VLAN ? 

VLANS:

- logically separate end-hosts at LAYER 2
- are configured on Layer 2 SWITCHES on a per-interface basis.
- any END HOST connected to that interface is part of that VLAN

---

PURPOSE OF VLANs:

Network Performance :

- Reduce unnecessary BROADCAST traffic, which helps prevent network congestion, and improve network performance

Network Security :

- Limiting BROADCAST and unknown UNICAST traffic, also improves network security, since messages won’t be received by devices outside of the VLAN

![image](https://github.com/psaumur/CCNA/assets/106411237/fae2f1ed-ffc3-4d91-adf7-16a67c2dc5aa)


SWITCHES do not forward traffic directly between HOSTS in different VLANS

![image](https://github.com/psaumur/CCNA/assets/106411237/2e5834e9-9096-46eb-bb96-ba8459338107)


![image](https://github.com/psaumur/CCNA/assets/106411237/3046f727-fad4-421e-85ef-63a73e109f83)


Sending Packets to another VLAN (Routed through R1)

![image](https://github.com/psaumur/CCNA/assets/106411237/7090ef6d-ce8c-454f-b80d-f6dfd82745c8)


![image](https://github.com/psaumur/CCNA/assets/106411237/b7237602-5b46-4c31-bd75-2e50e0fb1017)

---

HOW TO CONFIGURE VLANS ON CISCO SWITCHES

#show vlan brief

![image](https://github.com/psaumur/CCNA/assets/106411237/13ce8382-6aea-484e-9580-d91c98189522)


Shows which VLANS that exist on the SWITCH and what INTERFACES are in each VLAN

VLANs 1 (DEFAULT), 1002-1005 exist by default and **cannot be deleted (5 VLANs)**

---

HOW TO ASSIGN INTERFACES TO A VLAN

![image](https://github.com/psaumur/CCNA/assets/106411237/ed31145d-7949-4c68-b88a-97716beaf074)


1) Use the “interface range” command to select all the interfaces at once

2) Use the “switchport mode access” command to set the interface as an ACCESS PORT

---

WHAT IS AN ACCESS PORT?

- An ACCESS PORT is a SWITCHPORT which belongs to a single VLAN, and usually connects to end hosts like PCs.

SWITCHPORTS which carry multiple VLANs are called “TRUNK PORTS” (more info on TRUNK in next chapter)

3) Use the “switchport access” command to assign a VLAN to a PORT

![image](https://github.com/psaumur/CCNA/assets/106411237/b1bdb937-3707-496f-bc49-445df354d16b)


Use “#vlan <#>” to enter **Configuration Mode** for a given VLAN (this can also create a VLAN)

Use “#name <name>” to configure a NAME for your VLAN

To check your VLAN configuration, use “#show vlan brief”

![image](https://github.com/psaumur/CCNA/assets/106411237/2f7d26d8-9b2a-43a3-b213-fec4f984a309)


Testing VLAN 10

Pinging from PC1 using 255.255.255.255 (FFFF:FFFF:FFFF) floods broadcast packets to R1 and VLAN10 hosts only

![image](https://github.com/psaumur/CCNA/assets/106411237/5c64e485-f492-4436-9c1d-3a1ab20fbe05)

# 17. VLANS : PART 2

Basic VLAN topology from PART 1

![image](https://github.com/psaumur/CCNA/assets/106411237/f6df37e0-d494-4e46-b6e8-6d2ba0cd0ff6)


What about THIS Network Topology ?

![image](https://github.com/psaumur/CCNA/assets/106411237/e6aff877-3792-469f-8955-0f3e17c6f1ed)


Notice this one has TWO Switches (SW1 and SW2) and ENGINEERING (VLAN 10) has two separate locations on the network.

---

TRUNK PORTS

- In a small network with few VLANS, it’s possible to use a separate interface for EACH VLAN when connecting SWITCHES to SWITCHES, and SWITCHES to ROUTERS

- HOWEVER, when the number of VLANS increases, this is not viable. It will result in wasted interfaces, and often ROUTERS won’t have enough INTERFACES for each VLAN

- You can use TRUNK PORTS to carry traffic from multiple VLANS over a single interface

A TRUNK PORT carrying multiple VLAN connections over single interface

![image](https://github.com/psaumur/CCNA/assets/106411237/5cb7c933-689a-499b-9f30-51fe63d8b059)


![image](https://github.com/psaumur/CCNA/assets/106411237/8ea9a799-cf0d-4b1d-9706-db002772fe6d)


How does a packet know WHICH VLAN to send traffic to over the TRUNK PORT ?

VLAN TAGS !

SWITCHES will “tag” all frames that they send over a TRUNK LINK. This allows the receiving SWITCH to know which VLAN the frame belongs to.

TRUNK PORT = “Tagged” ports

ACCESS PORT = “Untagged” ports

---

VLAN TAGGING

- There are TWO main TRUNK protocols:
    - ISL (Inter-Switch Link)
    - IEEE 802.1Q (also known as “dot1q”)

ISL is an old Cisco proprietary protocol created before industry standard IEEE 802.1Q

IEEE 802.1Q is an industry standard protocol created by the IEEE (Institute of Electrical and Electronics Engineers)

You will probably NEVER use ISL in the real world; even modern Cisco equipment doesn’t use it.

For the CCNA, you will only need to learn 802.1Q

---

ETHERNET HEADER with 802.1Q

![image](https://github.com/psaumur/CCNA/assets/106411237/00e817cd-1cac-44c5-a5f6-5459d383236d)


- The 802.1Q TAG Is inserted between the SOURCE and TYPE/LENGTH fields in the ETHERNET FRAME
- The TAG is 4 bytes (32 bits) in length
- The TAG consists of TWO main fields:
    - Tag Protocol Identifier (TPID)
    - Tag Control Information (TCI)
        - TCI consists of THREE sub-fields:

![image](https://github.com/psaumur/CCNA/assets/106411237/8e52856b-58b9-448e-a007-254973fe707e)


TPID (TAG Protocol Identifier) :

- 16 bits (2 bytes) in length
- Always set to a value of 0x8100. This indicates that the frame is 802.1Q TAG

TCI / PCP (Priority Code Point) :

- 3 bits in length
- Used for Class of Service (CoS), which prioritizes important traffic in congested networks

TCI / DEI (Drop Eligible Indicator) :

- 1 bit in length
- Used to indicated frames that can be dropped if the network is congested

TCI / VID (VLAN ID) :

- 12 bits in length
- Identifies the VLAN the frame belongs to
- 12 bits in length = 4096 total VLANS (2^12), range of 0 - 4095
- VLANs 0 and 4095 are reserved and can’t be used
- Therefore, the actual range of VLANs is 1 - 4094

NOTE : Cisco’s ISL also had a VLAN range of 1 - 4094

---

VLAN RANGES

![image](https://github.com/psaumur/CCNA/assets/106411237/1c55a830-bfdd-423a-9688-334a3dd2bfa3)


---

NATIVE VLAN

![image](https://github.com/psaumur/CCNA/assets/106411237/8b1e09a1-e9c5-410e-ad87-581b95eaca81)


![image](https://github.com/psaumur/CCNA/assets/106411237/f8145795-b3f7-4766-9507-4fba7c743a14)


![image](https://github.com/psaumur/CCNA/assets/106411237/a1811276-c043-4035-9957-800873068615)

---

TRUNK CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/d73b8f0b-2154-4e7f-8057-7c5b3f5078cc)


![image](https://github.com/psaumur/CCNA/assets/106411237/29313a87-cf16-439c-8a9e-90b518326954)

Many modern switches do not support Cisco’s ISL at all. They only support 802.1Q (dot1q)

However, SWITCHES that do support both (like the one I am using in this example) have a TRUNK encapsulation of “AUTO” by default

To MANUALLY configure the INTERFACE as a TRUNK PORT, you must first set the encapsulation to “802.1Q” or “ISL”. On SWITCHES that only support 802.1Q, this is not necessary

After you set the encapsulation type, you can then configure the interface as a TRUNK

1) Select the interface to configure

2) Use “#switchport trunk encapsulation dot1q” to set the encapsulation mode to 802.1Q

3) Use “#switchport mode trunk” to manually configure the interface to TRUNK

![image](https://github.com/psaumur/CCNA/assets/106411237/6b897fb0-14a3-4e6a-b4e8-e278a6aec08e)


Use the “#show interfaces trunk” command to confirm INTERFACES on TRUNK

![image](https://github.com/psaumur/CCNA/assets/106411237/d3e144c7-90e3-4ab0-8021-7eb4d1420282)


Commands to allow a VLAN on a given TRUNK

![image](https://github.com/psaumur/CCNA/assets/106411237/6a60f6ce-55be-4df5-a715-b871e5e461f4)


![image](https://github.com/psaumur/CCNA/assets/106411237/b39b091d-1ea9-4f72-b592-1eeb8ef25f90)


Command to change the NATIVE VLAN

![image](https://github.com/psaumur/CCNA/assets/106411237/5109becb-27dd-4c63-9c7b-74b6f55e9d5f)


![image](https://github.com/psaumur/CCNA/assets/106411237/36abc437-69cb-4c56-8a59-87479ce01a7f)


---

Setting up our TRUNKS for this Network

![image](https://github.com/psaumur/CCNA/assets/106411237/892b5322-807b-4d76-91cb-a039766794c5)


We will need to configure :

SW1 : g0/0 interface (already configure above this section)

SW2: g0/0, and g0/1 interface

SW2 g0/0

![image](https://github.com/psaumur/CCNA/assets/106411237/7b313959-b710-4bb6-a281-727ec9477c3e)


SW2 g0/1

![image](https://github.com/psaumur/CCNA/assets/106411237/c26f17c8-0ec9-4406-ab66-83adf28c8550)


What about the ROUTER, R1 ? 

---

ROUTER ON A STICK (ROAS)

![image](https://github.com/psaumur/CCNA/assets/106411237/66c4ace0-8341-4c9c-8ff5-7c171034df53)


![image](https://github.com/psaumur/CCNA/assets/106411237/b409165d-39e6-4fba-ade1-2451f7e2fa8c)


![image](https://github.com/psaumur/CCNA/assets/106411237/112a2089-5a9e-4b13-945c-6be7f188d6a8)


NOTE the Sub-Interface names (like the network diagram) of 0.10, 0.20 and 0.30

You assign them IP addresses identically like you would a regular interface (using the last usable IP address of a given VLAN subnet)

Sub-interfaces will appear with the “show ip interface brief” command

![image](https://github.com/psaumur/CCNA/assets/106411237/9b7ecbd1-c5f4-4ed0-9988-8fd17e16c9ae)


They also appear in the “show ip route” command (Route Table)

![image](https://github.com/psaumur/CCNA/assets/106411237/1e9bb3fa-5aca-4883-8aff-52a554dcfba6)


ROAS is used to route between multiple VLANs using a SINGLE interface on a ROUTER and SWITCH

The SWITCH interface is configured as a regular TRUNK

The ROUTER interface is configured using SUB-INTERFACES. You configure the VLAN tag and IP address on EACH SUB-INTERFACE

The ROUTER will behave as if frames arriving with a certain VLAN tag have arrived on the SUB-INTERFACE configured with that VLAN tag

The ROUTER will TAG frames sent out of EACH SUB-INTERFACE with the VLAN TAG configured on the SUB-INTERFACE

# 18. VLANS : PART 3

NATIVE VLAN ON A ROUTER (ROAS)

![image](https://github.com/psaumur/CCNA/assets/106411237/838b9835-d17d-4d57-bac1-52f7e3adfd77)

Native VLAN untagged frames are faster and more efficient (smaller) than tagged ones.

Let’s reset all SWITCHES (SW1 and SW2) to native vlan 10

![image](https://github.com/psaumur/CCNA/assets/106411237/1e903c1b-b814-40b5-aaea-1ba9f3f192c8)



There are **TWO methods** of configuring the native VLAN on a router:

- Use the command “encapsulation dot1q <vlan-id>” on a Sub-Interface

![image](https://github.com/psaumur/CCNA/assets/106411237/2ea65208-6b2a-4cac-a463-982a731c9e24)


OR

- Configure the IP address for the native VLAN on the router’s physical interface (the “**encapsulation dot1q** <vlan-id> command is not necessary”

![image](https://github.com/psaumur/CCNA/assets/106411237/dabcc3b4-13c3-4d60-abe2-c7cbb5edd4c2)


Output of “show running-config” of G0/0 Interface

![image](https://github.com/psaumur/CCNA/assets/106411237/37ce4f0f-0ac0-45ce-802f-5fd11057f69d)


---

LAYER 3 (MULTILAYER) SWITCHES

ICON APPEARANCE

![image](https://github.com/psaumur/CCNA/assets/106411237/0d63f5f9-5efe-4c61-a8e6-3cd6a1161d2a)


- A MULTILAYER SWITCH is capable of both SWITCHING and ROUTING
- It is LAYER 3 AWARE
- You can assign IP Addresses to its L3 Virtual Interface, like a router
- You can create Virtual Interfaces for each VLAN, and assign IP addresses to those interfaces
- You can configure routes on it, just like a ROUTER
- It can be used for inter-VLAN routing

![image](https://github.com/psaumur/CCNA/assets/106411237/af59481b-d0cb-41d7-9eba-7c8d47131c28)


SW2 Replaced with a Layer 3 Switch

Multi-VLAN connections to R1 removed and replaced with a point-to-point Layer 3 connection

![image](https://github.com/psaumur/CCNA/assets/106411237/8f3ad167-d774-4fcb-96a5-66e568edead8)


- SVIs (Switch Virtual Interfaces) are the virtual interfaces you can assign IP addresses to in a MULTILAYER SWITCH.
- Configure each HOST to use the SVI (NOT the ROUTER R1) as their Gateway Address
- To send traffic to different SUBNETS / VLANS, the PCs will send traffic to the SWITCH, and the SWITCH will route the traffic.

![image](https://github.com/psaumur/CCNA/assets/106411237/5409b2cc-f876-4754-afe3-33298930fd7a)


![image](https://github.com/psaumur/CCNA/assets/106411237/953372de-579a-4803-9418-0bd1aeef229d)


Clearing R1 configuration to set to work with the Layer 3 Point-to-Point connection

![image](https://github.com/psaumur/CCNA/assets/106411237/40354cbe-df39-4a78-97cd-bbb0bc10549c)


#no interface <sub-interface id> : removes the VLAN interface

#default interface g0/0 : resets the g0/0 interface to it’s default settings

Then configure the default R1 G0/0 interface’s to IP address : 192.168.1.194 (as per the network diagram)

Configuration of SW2 to use SVI and the Layer 3 Point-to-Point connection with R1

![image](https://github.com/psaumur/CCNA/assets/106411237/24d64087-f98c-4a1e-a07f-3f93f06f93a9)


“default interface <interface-id>” : resets settings on specified interface to defaults

“ip routing” : **IMPORTANT** command to enable Layer 3 routing on the SWITCH

“no switchport” : configures the interface from a Layer 2 Switchport to a Layer 3 “routed port” 

The sets the Default Route to R1 (192.168.1.194) so that all traffic leaving the network gets routed through R1’s Gateway of Last Resort (aka The Default Gateway)

![image](https://github.com/psaumur/CCNA/assets/106411237/7a682a2f-3ae3-420b-8f68-9e1050dd82c6)


![image](https://github.com/psaumur/CCNA/assets/106411237/c0b544b7-8f32-49ae-9a46-d09390a3d08c)


SVI CONFIGURATION ON SW2 (Virtual LAYER 3 ROUTING INTERFACES)

![image](https://github.com/psaumur/CCNA/assets/106411237/7c1710fb-40d7-44a4-8336-b037e1c2ea77)



SVIs are **shut down** by default, so remember to use “no shutdown”

![image](https://github.com/psaumur/CCNA/assets/106411237/2b5b13c3-1364-4296-886c-0bd9b00b4167)


Creating an unknown SVI (VLAN 40) and the Status/Protocol is “down/down”

What are the conditions for a SVI to be “up/up” ? 

- The VLAN must exist on the SWITCH
- The SWITCH must have at least ONE access port in the VLAN in an “up/up” state AND/OR one TRUNK port that allows the VLAN that is in an “up/up” state
- The VLAN must not be shutdown (you can use the “shutdown” command to disable a VLAN)
- The SVI must not be shutdown (SVIs are disabled, by default)

![image](https://github.com/psaumur/CCNA/assets/106411237/558ef418-5902-42d0-b4a5-cce14b56b77e)


The VLAN trunk has been successfully replaced by an Layer 3 SWITCH SVI.

All hosts should be able to connect with each other (tested with “ping”) as well as reach the external internet (via the Cloud symbol attached to R1)

# 19. DTP / VTP (Not in Syllabus)

DTP (Dynamic Trunking Protocol)

- Protocol that allows SWITCHES to negotiate the status of their SWITCHPORTS, without manual configuration, to be:
    - ACCESS PORTS
    - TRUNK PORTS

- DTP is ENABLED by default on all Cisco SWITCH interfaces

We’ve been manually configuring SWITCHPORTS using :

- “switchport mode access”
- “switchport mode trunk”

```
💡 'show interfaces <interface-id> switchport' will show you a switchport’s settings.
```
For security purposes, **manual configuration** is recommended. DTP should be disabled on ALL SWITCHPORTS

![image](https://github.com/psaumur/CCNA/assets/106411237/bf716a33-8e11-4c09-bb0b-336ba48ef26d)


DYNAMIC DESIRABLE:

- This MODE will actively try to form a TRUNK with other Cisco SWITCHES.
- Will form a TRUNK if connected to another SWITCHPORT in the following modes:
    - “switchport mode trunk”
    - “switchport mode dynamic desirable”
    - “switchport mode dynamic auto”
    

HOWEVER … if the other interface is set to “static access” (ACCESS mode), it will NOT form a TRUNK, it will be an ACCESS PORT

DYNAMIC AUTO:

- This MODE will NOT actively try to form a TRUNK with other Cisco SWITCHES
- Will form a TRUNK if connected SWTICH is actively trying to form a TRUNK.
- It will form a TRUNK with a SWITCHPORT in the following modes:
    - “switchport mode trunk”
    - “switchport mode dynamic desirable”

TRUNK to ACCESS connection will operate in a **Mismatched Mode**.

This configuration does NOT work and SHOULD result in an error. Traffic will NOT work.

TABLE SHOWING THE DIFFERENT MODES AND COMPATIBILITY IN FORMING A TRUNK

![image](https://github.com/psaumur/CCNA/assets/106411237/93d5e4f4-cb24-4d3f-ba62-fd002581cfbb)

---

DTP will NOT form a TRUNK with:

a ROUTER

a PC

etcetera …

The SWITCHPORT will be in ACCESS Mode only!

OLD SWITCHES:

- “switchport mode dynamic desirable”  = Default administrative mode.

NEWER SWITCHES:

- “switchport mode dynamic auto” = Default administrative mode.

HOW TO DISABLE DTP NEGOTIATION ON AN INTERFACE:

- “switchport nonegotiate”
- “switchport mode access”

It is a security recommendation to disable DTP on all SWITCHPORTS and manually configure them as ACCESS or TRUNK ports.

---

ENCAPSULATION:

SWITCHES that support both:

- 802.1Q
- ISL

TRUNK encapsulation can use DTP to negotiate the encapsulation they will use.

- Negotiation is Enabled by default

```
💡 'switchport trunk encapsulation negotiate'
```    

- ISL is favored over 802.1Q
    - If BOTH SWITCHES support ISL, ISL will be selected.
- DTP frames are sent in:
    - VLAN1 when using ISL
    - Native VLAN when using 802.1Q (the default native VLAN is VLAN1, however)

---

VTP (VLAN Trunking Protocol)

In Privileged EXEC mode:

```
💡 #show vtp status
```

- Protocol for configuring VLANs on a Central SWITCH
    - A SERVER that other SWITCHES synch. to (auto configuring by connection)
- Other switches (VTP CLIENTS) will synchronize their VLAN database to the SERVER
- Designed for large networks with many VLANs (reduces manual configuration)
- RARELY used. Recommended you DO NOT USE it
- There are THREE VTP Versions :

    - v1
        - Does NOT supports Extended VLAN Range 1006-4094
    - v2
        - Does NOT supports Extended VLAN Range 1006-4094
        - Supports Token Ring VLANs ; otherwise similar to V1
    - v3
        - Supports Extended VLAN Range 1006-4094
        - CLIENTS store VLAN dBase in NVRAM

- There are **THREE VTP modes**:
    - SERVER
    - CLIENT
    - TRANSPARENT

- Cisco SWITCHES operate in VTP SERVER mode, by default

---

![image](https://github.com/psaumur/CCNA/assets/106411237/87dcd7ff-f3d3-4441-841c-a0506c249f03)

---

VTP SERVERS:

- Can ADD / MODIFY / DELETE VLANs
- Store the VLAN dBase in NVRAM
- Increase Revision Number every time VLAN is Added / Modified / Deleted
- Advertises **Latest Version** of VLAN dBase on TRUNK interfaces.
- VTP CLIENTS synchronize their VLAN dBase to it
- **VTP SERVERS also function as VTP CLIENTS**
    - **THEREFORE, a VTP SERVER will synchronize to another VTP SERVER with a higher Revision Number**

<aside>
🚨 One danger of VTP:
Connecting an old SWITCH with higher Revision Number to network (and if the VTP Domain Name matches), all SWITCHES in Domain will synchronize their VLAN dBase to SWITCH

</aside>


VTP CLIENTS:

```
💡 (config)# vtp mode client
```

- Cannot Add / Modify / Delete VLANs
- Does NOT store the VLAN database in NVRAM
    - **VTP v3 CLIENTS DO**
- Will synchronize their VLAN dBase to the SERVER with the highest version number in their VTP Domain
- Advertise their VLAN dBase and forward VTP Advertisements to other CLIENTS over TRUNK Ports

VTP TRANSPARENT MODE:

```
💡 (config)# vtp mode transparent
```

- Does NOT participate in VTP Domain (does NOT sync VLAN database)
- Maintains own VLAN dBase in NVRAM.
- Can Add / Modify / Delete VLANs
- Won’t Advertise to other SWITCHES
- Will forward VTP advertisements to SWITCHES in the same Domain as it.

---

VTP DOMAINS

If a SWITCH with no VTP Domain (Domain NULL) receives a VTP advertisement with a VTP Domain name, it will automatically join that VTP Domain

If a SWITCH receives a VTP advertisement in the same VTP domain with a higher revision number, it will update it’s VLAN database to match

---

REVISION NUMBERS:

There are TWO ways to RESET a REVISION NUMBER to 0:

- Change VTP Domain to an unused Domain
- Change VTP mode to TRANSPARENT

---

VTP VERSION NUMBER

```
💡 (config)#vtp version <version number>
```
  
Changing the Version # will force sync/update all connected SWITCHES to the latest Version #

# 20. SPANNING TREE PROTOCOL (STP) : PART 1

REDUNDANCY IN NETWORKS

- Essential in network design
- Modern networks are expected to run 24/7/265; even a short downtime can be disastrous for business.
- If one network component fails, you must ensure that other components will take over with little or no downtime.
- As much as possible, you must implement REDUNDANCY at every possible point in the network

AN EXAMPLE OF A POORLY DESIGNED NETWORK

![image](https://github.com/psaumur/CCNA/assets/106411237/b3b76af5-11e6-495b-8c40-40eb5800704b)


NOTE the many single-point failures that could occur (single connections)

A BETTER NETWORK DESIGN

![image](https://github.com/psaumur/CCNA/assets/106411237/01c20d92-2cf6-4d1f-a193-ded7753aeb38)


UNFORTUNATELY : 

- Most PCS only have a single network interface card (NIC), so they can only be plugged into a single SWITCH. However, important SERVERS typically have multiple NICs, so they can be plugged into multiple SWITCHES for redundancy!

So HOW can all this redundancy be a BAD thing?

BROADCAST STORMS

![image](https://github.com/psaumur/CCNA/assets/106411237/a0bf91be-a463-45df-bfc5-df471d0544b5)


![image](https://github.com/psaumur/CCNA/assets/106411237/d13b6ab5-5298-4166-bdfa-3315f05a2961)


![image](https://github.com/psaumur/CCNA/assets/106411237/f719de69-df9e-4549-b3cb-914d7c5aabc4)


FLOODED WITH ARP REQUESTS (Red = Clockwise Loops // Purple = Counter-Clockwise Loops)

Network Congestion isn’t the only problem.

Each time a FRAME arrives on a SWITCHPORT, the SWITCH uses the SOURCE MAC ADDRESS field to “learn” the MAC ADDRESS and update it’s MAC ADDRESS TABLE.

When frames with the same SOURCE MAC ADDRESS repeatedly arrive on different interfaces, the SWITCH is continuously updating the interface in it’s MAC ADDRESS TABLE.

This is called MAC ADDRESS FLAPPING

So how we design a network, with redundant paths, that doesn’t result in LAYER 2 LOOPS.

SPANNING TREE PROTOCOL is one solution

---

STP (SPANNING TREE PROTOCOL) : 802.1D

- “Classic Spanning Tree Protocol” is IEEE **802.1D**
- SWITCHES from ALL vendors run STP by Default
- STP prevents LAYER 2 loops by placing redundant PORTS in a BLOCKING state, essentially disabling the INTERFACE
- These INTERFACES act as backups that can enter a FORWARDING state if an active (=currently forwarding) INTERFACE fails.
- INTERFACES in a BLOCKING state only send or receive STP messages (called BPDUs = Bridge Protocol Data Units)

💡 SPANNING TREE PROTOCOL still uses the term “BRIDGE”. However, when use the term “BRIDGE”, we really mean “SWITCH”. BRIDGES are not used in modern networks.

![image](https://github.com/psaumur/CCNA/assets/106411237/f253770d-22fa-4e3f-91b0-8f2b4c2f1a61)


ORANGE INTERFACE is “BLOCKED” causing a break in the loops

![image](https://github.com/psaumur/CCNA/assets/106411237/45125471-da23-4753-b5b1-16c23a2bfeff)


If changes occur in the connections, the traffic will adjust the topology.

- By selecting WHICH ports are FORWARDING and which ports are BLOCKING, STP creates a single path TO / FROM each point in the NETWORK. This prevents LAYER 2 Loops.
- There is a set process that STP uses to determine which ports should be FORWARDING and which should be BLOCKING
- STP-enabled SWITCHES send / receive “Hello BPDUs” out of all INTERFACES
    - The default timer is : ONCE every TWO seconds per INTERFACE!
- If a SWITCH receives a “Hello BPDU” on an INTERFACE, it knows that INTERFACE is connected to another SWITCH (ROUTERS, PCs, etc. do NOT use STP so do not send “Hello BPDUs”)

---

WHAT ARE BPDUs USED FOR?

- SWITCHES use one field in the STP BPDU, the BRIDGE ID field, to elect a ROOT BRIDGE for the NETWORK
- The SWITCH with the lowest BRIDGE ID becomes the ROOT BRIDGE
- ALL PORTS on the ROOT BRIDGE are put in a FORWARDING state, and other SWITCHES in the topology must have a path to reach the ROOT BRIDGE

![image](https://github.com/psaumur/CCNA/assets/106411237/05177f47-882e-47ea-8bec-22e073392e1c)

![image](https://github.com/psaumur/CCNA/assets/106411237/17f921f6-0583-4070-9493-5f5d80ad4866)

![image](https://github.com/psaumur/CCNA/assets/106411237/bb49a034-9f6d-4e92-9ea0-8bc71c4f2ec8)


To REDUCE the BRIDGE PRIORITY, we can only change it in units of 4096 !

![image](https://github.com/psaumur/CCNA/assets/106411237/39fe6239-1217-4885-b07b-8f368dad0e28)


In THIS TOPOLOGY, SW1 becomes the ROOT BRIDGE due to it’s MAC ADDRESS being LOWEST

(Hex “A” = 10)

![image](https://github.com/psaumur/CCNA/assets/106411237/b1e1a69d-4b9c-46bf-9b77-f30b9f7c3933)


ALL INTERFACES on the ROOT BRIDGE are DESIGNATED PORTS.

DESIGNATED PORTS ARE IN A FORWARDING STATE!

ROOT BRIDGE

- When a SWITCH is powered on, it assumes it is the ROOT BRIDGE
- It will only give up its position if it receives a “SUPERIOR” BPDU (lower BRIDGE ID)
- Once the topology has converged and all SWITCHES agree on the ROOT BRIDGE, only the ROOT BRIDGE sends BPDUs
- Other SWITCHES in the network will forward these BPDUs, but will not generate their own original BPDUs

---

SPANNING TREE PROTOCOL STEPS

1) One SWITCH is elected as ROOT BRIDGE. All PORTS on the ROOT BRIDGE are DESIGNATED PORTS (FORWARDING STATE)

- ROOT BRIDGE selection order:
    - 1) Lowest BRIDGE ID
    - 2) Lowest MAC Address (in case of Bridge ID tie)

2) Each remaining SWITCH will select ONE of its INTERFACES to be it’s ROOT PORT (FORWARDING STATE). PORTS across from the ROOT PORT are always DESIGNATED PORTS.

- ROOT PORT selection order:
    - 1) LOWEST ROOT COST (see STP COST CHART)
    - 2) LOWEST NEIGHBOUR BRIDGE ID
    - 3) LOWEST NEIGHBOUR PORT ID

3) Each remaining COLLISION DOMAIN will select ONE INTERFACE to be a DESIGNATION PORT (FORWARDING STATE). The other PORT in the COLLISION DOMAIN will NON-DESIGNATED (BLOCKING)

- DESIGNATED PORT SELECTION:
    - 1) INTERFACE on SWITCH with LOWEST ROOT COST
    - 2) INTERFACE on SWITCH with LOWEST BRIDGE ID

---

STP COST CHART

💡 Only OUTGOING INTERFACES toward the ROOT BRIDGE have a STP COST; not RECEIVING INTERFACES. Add up all the OUTGOING PORT costs until you reach the ROOT BRIDGE

![image](https://github.com/psaumur/CCNA/assets/106411237/0ee95883-aed8-42a3-ba82-11209ef8cd40)


SW1 is the ROOT BRIDGE so has a STP COST of 0 on ALL INTERFACES

![image](https://github.com/psaumur/CCNA/assets/106411237/35037ae9-3430-44ac-be6d-c8d2a2a42c24)


The PORTS connected to another SWITCH’s ROOT PORT MUST be DESIGNATED (D). 

Because the ROOT PORT Is the SWITCH’s path to the ROOT BRIDGE, another SWITCH must not block it.

STP PORT ID (in case of a tie-breaker)

![image](https://github.com/psaumur/CCNA/assets/106411237/63d2fb87-31fa-4b57-a2c3-a203feded8ba)


NEIGHBOUR SWITCH PORT ID (in case of a tie-breaker)

(D) = DESIGNATED PORT

(R) = ROOT PORT

![image](https://github.com/psaumur/CCNA/assets/106411237/c3fcc32b-e95f-4d4b-a241-f9f3080e858f)


HOW TO DETERMINE WHICH PORT WILL BE BLOCKED TO PREVENT LAYER 2 LOOPS

![image](https://github.com/psaumur/CCNA/assets/106411237/1b69a092-4150-44c3-b605-5916fdea91d6)


QUIZ

Identify the ROOT BRIDGE and the ROLE of EACH INTERFACE on the NETWORK (ROOT / DESIGNATED / NON-DESIGNATED)

#1

![image](https://github.com/psaumur/CCNA/assets/106411237/62bcf349-dd89-48be-92f6-d6a184edeb6f)


ALL SWITCHES have the same PRIORITY NUMBER (32769)

Tie-breaker goes to the LOWEST MAC ADDRESS

SW3 has the LOWEST so it’s the ROOT BRIDGE and ALL it’s INTERFACES become DESIGNATED

Connections from SW1 (G0/1) and S4 (G0/0) to SW3 become ROOT INTERFACES

Because SW2 has TWO connections to SW1, both of SW1’s INCOMING interfaces become DESIGNATED.

SW2 G0/2 INTERFACE becomes a ROOT INTERFACE because the G0/0 INTERFACE of SW1 is LOWER than it’s G0/2 INTERFACE

The remaining interfaces on SW2 become NON-DESIGNATED because it has the HIGHEST ROOT COST (12 = 4x 1 GB connection). INTERFACES they are attached to on other SWITCHES become DESIGNATED

#2

![image](https://github.com/psaumur/CCNA/assets/106411237/ae382ec2-9c0f-4673-94b5-5d1411c8db6b)


SW4 has the LOWEST Priority Number so it is designated ROOT BRIDGE

All of SW4 INTERFACES become DESIGNATED

SW2 G0/0 becomes ROOT PORT because SW4 G0/0 connection is a LOWER NUMBER than G0/1. 

SW3 G0/1 becomes ROOT PORT

SW1 G0/1 becomes ROOT PORT because G0/1 cost is LESS than Fa1/0 and 2/0

EACH remaining PORT will be either DESIGNATED or NON-DESIGNATED

SW1 Fa1/0 and 2/0 become NON-DESIGNATED since they have a HIGHER STP COST (38) than SW2 outbound ports (8) making SW2 Fa1/0 and 2/0 DESIGNATED

SW2 remaining connection, G0/1, NON-DESIGNATED

# 21. SPANNING TREE PROTOCOL (STP) : PART 2

STP STATES

![image](https://github.com/psaumur/CCNA/assets/106411237/5c9a17ff-b0d6-455c-8677-5144dd5a0048)


- ROOT / DESIGNATED PORTS remain STABLE in a FORWARDING state
- NON-DESIGNATED PORTS remain STABLE in a BLOCKING state
- LISTENING and LEARNING are TRANSITIONAL states which are passed through when an interface is activated, or when a BLOCKING PORT must transition to a FORWARDING state due to a change in network topology.

**1) BLOCKING / STABLE**

- NON-DESIGNATED PORTS are in a BLOCKING state
- Interfaces in a BLOCKING state are effectively disabled to prevent loops
- Interfaces in a BLOCKING state do NOT Send/Receive regular network traffic
- Interfaces in a BLOCKING state do NOT forward STP BPDUs
- Interfaces in a BLOCKING state do NOT learn MAC ADDRESSES

**2) LISTENING / TRANSITIONAL**

- After the BLOCKING state, interfaces with the DESIGNATED or ROOT role enter the LISTENING state
- ONLY DESIGNATED or ROOT PORTS enter the LISTENING state (NON-DESIGNATED PORTS are ALWAYS BLOCKING)
- The LISTENING state is 15 seconds long by Default. This is determined by the FORWARD DELAY TIMER
- Interfaces in a LISTENING state do NOT Send / Receive regular network traffic
- Interfaces in a LISTENING state ONLY Forward/Receive STP BPDUs
- Interfaces in a LISTENING state does NOT learn MAC ADDRESSES from regular traffic that arrives on the interface

**3) LEARNING / TRANSITIONAL**

- After the LISTENING state, a DESIGNATED or ROOT port will enter the LEARNING state
- The LEARNING state is 15 seconds long by Default. This is determined by the FORWARD DELAY TIMER (same one used for both LISTENING and LEARNING states)
- Interfaces in a LEARNING state do NOT Send / Receive regular network traffic
- Interfaces in a LEARNING state ONLY Sends/Receives STP BPDUs
- Interfaces in a LEARNING state **learns** MAC ADDRESSES from regular traffic that arrives on the interface

4) FORWARDING / STABLE

- ROOT and DESIGNATED PORTS are in a FORWARDING state
- A PORT in the FORWARDING state operate as NORMAL
- A PORT in the FORWARDING state Sends/Receives regular network traffic
- A PORT in the FORWARDING state Sends/Receives STP BPDUs
- A PORT in the FORWARDING state **learns** MAC ADDRESSES

SUMMARY : 

![image](https://github.com/psaumur/CCNA/assets/106411237/f4cea5ca-b90a-423e-9160-f206b8b1621d)


---

STP TIMERS

![image](https://github.com/psaumur/CCNA/assets/106411237/a174469f-9e75-4645-aff8-d4bfe46fb207)


💡 SWITCHES do NOT forward the BPDUs out of their ROOT PORTS and NON-DESIGNATED PORTS - ONLY their DESIGNATED PORTS !!!


MAX AGE TIMER:

- If another BPDU is received BEFORE MAX AGE TIMER counts down to 0, the TIME will RESET to 20 Seconds and no changes will occur.
- If another BPDU is not received, the MAX AGE TIMER counts down to 0 and the SWITCH will re-evaluate it’s STP choices, including ROOT BRIDGE, LOCAL ROOT, DESIGNATED, and NON-DESIGNATED PORTS.
- If a NON-DESIGNATED PORT is selected to become a DESIGNATED or ROOT PORT, it will transition from the BLOCKING state to the LISTENING state (15 Seconds), LEARNING state (15 Seconds), and then finally the FORWARDING state.
    - So… it can take 50 Seconds for a BLOCKING interface to transition to FORWARDING! (MAX AGE TIMER  + (LISTENING + LEARNING 15 Second timers))
- These TIMERS and TRANSITIONAL STATES are to make sure that LOOPS are not accidentally created by an INTERFACE moving to FORWARDING STATE too soon

 HOWEVER …

💡 A FORWARDING interface can move DIRECTLY to a BLOCKING state (there is no worry about creating a loop)

💡 A BLOCKING interface can NOT move DIRECTLY to a FORWARDING state. It MUST go through the LISTENING and LEARNING states first!


---

STP BPDU (BRIDGE PROTOCOL DATA UNIT)

Ethernet Header of a BPDU

![image](https://github.com/psaumur/CCNA/assets/106411237/0e68839f-c4ec-448b-8876-791212462009)


💡 PVST+ uses the MAC ADDRESS : 

01 : 00 : 0c : cc : cc : cd

PVST = ONLY ISL Trunk Encapsulation

PVST+ = Supports 802.1Q

💡 Regular STP (not Cisco’s PVST+) uses the MAC ADDRESS : 

01 : 80 : c2 : 00 : 00 : 00

💡 The STP TIMERS on the ROOT BRIDGE determine ALL STP TIMERS for the entire network!

---

STP OPTIONAL FEATURES (STP TOOLKIT)

PORTFAST:

- Can be Enabled on INTERFACES which are connected to END HOSTS

💡 PORTFAST allows a PORT to move immediately to the FORWARDING state, bypassing LISTENING and LEARNING

- If used, it MUST be ENABLED only on PORTS connected to END HOSTS
- If ENABLED on a PORT connected to another SWITCH, it could cause a LAYER 2 LOOP

![image](https://github.com/psaumur/CCNA/assets/106411237/43c91f09-0d9f-4b81-b5a2-f02003e25b88)


You can also ENABLE PORTFAST with the following command:

💡 SW1(config)# spanning-tree portfast default

This ENABLES PORTFAST on ALL ACCESS PORTS (not TRUNK PORTS)

BPDU GUARD:

- If an INTERFACE with BPDU GUARD ENABLED receives a BPDU from another SWITCH, the INTERFACE will be SHUT DOWN to prevent loops from forming.

![image](https://github.com/psaumur/CCNA/assets/106411237/00c61767-72b4-4d51-b964-f76b6f4f6ae9)


You can also ENABLE BPDU GUARD with the following command:

💡 SW1(config)# spanning-tree portfast bpduguard default


This ENABLES BPDU GUARD on all PORTFAST-enabled INTERFACES

ROOT GUARD / LOOP GUARD:

![image](https://github.com/psaumur/CCNA/assets/106411237/bb38aedc-df38-4d76-b6cb-30319e74ecc1)


You probably do NOT have to know these STP optional features (or others such as UplinkFast, Backbone Fast, etcetera) for the CCNA. 

BUT…

💡 Make sure you know PORTFAST and BPDU GUARD.

---

STP CONFIGURATION

Command to CONFIGURE Spanning-Tree mode on a SWITCH

![image](https://github.com/psaumur/CCNA/assets/106411237/f29e2f41-3fac-463c-ab14-bb2d2f49816d)


Modern Cisco SWITCHES run **rapid-pvst**, by default

---

CONFIGURE THE PRIMARY ROOT BRIDGE

Command to CONFIGURE Spanning-Tree PRIMARY ROOT BRIDGE on a SWITCH

![image](https://github.com/psaumur/CCNA/assets/106411237/e90f16ad-c85c-4868-bbf4-9095c0abd581)


Confirm with “(do) show spanning-tree”

Can see in the above example, SW3 has become the “root”

- The “spanning-tree vlan <vlan-number> root primary” command sets the STP PRIORITY to 24576. If another SWITCH already has a priority number lower than 24576, it sets this SWITCH’s priority to 4096 LESS THAN the other SWITCH’s Priority (remember STP PART 1 lecture)

---

SECONDARY ROOT BRIGE (backup ROOT BRIDGE)

Command to CONFIGURE Spanning-Tree SECONDARY ROOT BRIDGE on a SWITCH

![image](https://github.com/psaumur/CCNA/assets/106411237/7d28f782-4673-4bc8-9aae-999aeac90685)



- The “spanning-tree vlan <vlan-number> root secondary” command sets the STP PRIORITY to 28672 (exactly 4096 higher than 24576).

---

VLAN 1 TOPOLOGY running PVST+

![image](https://github.com/psaumur/CCNA/assets/106411237/880a4cc7-e472-4764-a68b-a62288066796)


SW1 WAS the PRIMARY ROOT BRIDGE but : 

- We have configured SW3 to be the PRIMARY
- We have configured SW2 to be the SECONDARY

The TOPOLOGY for VLAN 2, however, won’t be the same. It will be the OLD Topology.

![image](https://github.com/psaumur/CCNA/assets/106411237/2cedeb36-27f1-4984-96e7-28ab70957c51)


WHY?
Because we made changes ONLY to the TOPOLOGY found in VLAN 1 (see the commands we used)

---

CONFIGURE STP PORT SETTINGS

![image](https://github.com/psaumur/CCNA/assets/106411237/58af0a8d-eeb4-4c34-8b54-6b8ff511695c)


“cost” = “ROOT COST”

“port-priority” = “PORT PRIORITY”

# 22. RAPID SPANNING TREE PROTOCOL

*COMPARISON OF STP VERSIONS (Standard vs. Cisco)*

![image](https://github.com/psaumur/CCNA/assets/106411237/ca5ff85c-842e-4ed3-9b6a-f9d6ed546a78)


We are only concerned with 802.1w for MOST use cases.

MSTP (802.1s) is more useful for VERY LARGE networks.

WHAT IS RAPID PER-VLAN SPANNING TREE PLUS?

> RSTP is not a time-based spanning tree algorithm like 802.1D. Therefore, RSTP offers an improvment over teh 30 seconds or more 802.1D takes to move a link to forwarding. The heart of the protocol is a new bridge-bridge handshake mechanism, which allows ports to move directly to forwarding

---

SIMILARITIES BETWEEN STP AND RSTP:

- RSTP serves the same purpose as STP, blocking specific PORTS to prevent LAYER 2 LOOPS.
- RSTP elects a ROOT BRIDGE with the same rules as STP
- RSTP elects ROOT PORTS with the same rules as STP
- RSTP elects DESIGNATED PORTS with the same rules as STP

---

DIFFERENCES BETWEEN STP AND RSTP:

**PORT COSTS**

![image](https://github.com/psaumur/CCNA/assets/106411237/b250c6da-2579-4576-8e93-5a8f8e66d873)


(STUDY AND MEMORIZE PORT COSTS OF STP AND RSTP)

RSTP PORT STATES

![image](https://github.com/psaumur/CCNA/assets/106411237/054d5037-a60e-478e-986b-6f43825a0d1a)

- If a PORT has been ADMINISTRATIVELY DISABLED (”shutdown” command) = DISCARDING STATE
- If a PORT is ENABLED but BLOCKING traffic to prevent LAYER 2 LOOPS = DISCARDING STATE

---

RSTP ROLES

- The ROOT PORT role remains unchanged in RSTP
    - The PORT that is closest to the ROOT BRIDGE becomes the ROOT PORT for the SWITCH
    - The ROOT BRIDGE is the only SWITCH that doesn’t have a ROOT PORT
- The DESIGNATED PORT role remains unchanged in RSTP
    - The PORT on a segment (Collision Domain) that sends the best BPDU is that segment’s DESIGNATED PORT (only one per segment!)
- The NON-DESIGNATED PORT role is split into TWO separate roles in RSTP:
    - The ALTERNATE PORT role
    - The BACKUP PORT role

**RSTP : ALTERNATE PORT ROLE**

- The RSTP ALTERNATE PORT ROLE is a DISCARDING PORT that receives a superior BPDU from another SWITCH
- This is the same as what you’ve learned about BLOCKING PORTS in classic STP

![image](https://github.com/psaumur/CCNA/assets/106411237/7d81e70c-3b31-4448-9d45-9aadb738c74d)

- An ALTERNATE PORT (labelled “A” above) functions as a backup to the ROOT PORT
- If the ROOT PORT fails, the SWITCH can immediately move it’s best alternate port to FORWARDING

![image](https://github.com/psaumur/CCNA/assets/106411237/41f3be85-6225-4749-83b4-f76952c5756a)

💡 This immediate move to FORWARDING STATE functions like a classic STP optional feature called **UplinkFast.** Because it is built into RSTP, you do not need to activate UplinkFast when using RSTP/Rapid PVST+

One more STP optional feature that was built into RSTP is **BackboneFast**

![image](https://github.com/psaumur/CCNA/assets/106411237/c4cea7b7-599f-4ec8-b9d3-a5acba71a5f5)

- **BackboneFast** allows SW3 to expire the MAX AGE TIMERS on it’s INTERFACE and rapidly FORWARD the superior BPDUs to SW2
- This FUNCTIONALITY is built into RSTP, so it does not need to be configured.

UPLINKFAST and BACKBONE FAST (SUMMARY)

💡 **UplinkFast** and **BackboneFast** are two optional features in Classic STP. They must be configured to operate on the SWITCH (not necessary to know for the CCNA)

- Both features are built into RSTP, so you do NOT have to configure them. They operate, by DEFAULT
- You do NOT need to have a detailed understanding of them for the CCNA. Know their names and their BASIC purpose (to help BLOCKING / DISCARDING PORTS rapidly move to FORWARDING)

---

**RSTP : BACKUP PORT ROLE**

- The RSTP BACKUP PORT role is a DISCARDING PORT that receives a superior BPDU from another INTERFACE on the same SWITCH
- This only happens when TWO INTERFACES are connected to the SAME COLLISION DOMAIN (via a HUB)
- Hubs are NOT used in modern networks, so you will probably NOT encounter an RSTP BACKUP PORT
- Hubs are NOT used in modern networks, so you will probably NOT encounter an RSTP BACKUP PORT.
- Functions as a BACKUP for a DESIGNATED PORT

💡 The INTERFACE with the LOWERS PORT ID will be selected as the DESIGNATED PORT, and the other will be the BACKUP port.

![image](https://github.com/psaumur/CCNA/assets/106411237/61aefc04-b3a9-484a-bbfa-1efe792c73c7)

WHICH Switch will be ROOT BRIDGE?
What about the OTHER ports ?

![image](https://github.com/psaumur/CCNA/assets/106411237/be4d404d-829d-41ab-ba39-34e918ed7ea9)

![image](https://github.com/psaumur/CCNA/assets/106411237/b5dec396-d5fc-486b-9110-5dcc2c4dc4aa)

![image](https://github.com/psaumur/CCNA/assets/106411237/1930a17b-6c74-4756-b89d-4148008f586b)

💡 RAPID STP *is* compatible with CLASSIC STP.
💡 The INTERFACE(S) on the RAPID STP-enabled SWITCH connected to the CLASSIC STP-enabled SWITCH will operate in CLASSIC STP MODE (Timers, BLOCKING >>> LISTENING >>> LEARNING >>> FORWARDING, etc.)

---

RAPID STP BPDU

CLASSIC RSTP (LEFT) vs RAPID STP BPDU (RIGHT)

![image](https://github.com/psaumur/CCNA/assets/106411237/2d2deb45-3f81-4c60-b9fa-0f6c3fe7c060)


💡 NOTE:

Classic STP BPDU has a “Protocol Version Identifier: Spanning Tree (0)

BPDU Type: Configuration (0x00)

BPDU flags: 0x00

RAPID STP BPDU has a “Protocol Version Identifier: Spanning Tree (2)

BPDU Type: Configuration (0x02)

BPDU flags: 0x3c


In CLASSIC STP, only the ROOT BRIDGE originated BPDUs, and other SWITCHES just FORWARDED the BPDUs they received. 

In RAPID STP, ALL SWITCHES originate and send their own BPDUs from their DESIGNATED PORTS

---

RAPID SPANNING TREE PROTOCOL

- ALL SWITCHES running RAPID STP send their own BPDUs every “hello” time (2 Seconds)
- SWITCHES “age” the BPDU information much more quickly
    - In CLASSIC STP, a SWITCH waits 10 “hello” intervals (20 seconds)
    - In RAPID STP, a SWITCH considers a neighbour lost if it misses 3 BPDUs (6 seconds). It will then “flush” ALL MAC ADDRESSES learned on that interface

![image](https://github.com/psaumur/CCNA/assets/106411237/c03d2645-42d8-4d95-b486-999e82ac12a8)

---

RSTP LINK TYPES

![image](https://github.com/psaumur/CCNA/assets/106411237/e837a271-ad13-4d6a-a800-434a0eff2576)

```
<E> = EDGE

<P> = POINT-TO-POINT

<S> = SHARED
```

RSTP distinguishes between THREE different “link types” : **EDGE**, **POINT-TO-POINT**, and **SHARED**

EDGE PORTS

- Connected to END HOSTS
- Because there is NO RISK of creating a LOOP, they can move straight to the FORWARDING STATE without the negotiation process!
- They function like a CLASSIC STP PORT with PORTFAST ENABLED

💡 SW1(config-if)# spanning-tree portfast

---

POINT-TO-POINT PORTS

- Connect directly to another SWITCH
- They function in FULL-DUPLEX
- You don’t need to configure the INTERFACE as POINT-TO-POINT (it should be detected)

💡 SW1(config-if)# spanning-tree link-type point-to-point

---

SHARED PORTS

- Connect to another SWITCH (or SWITCHES) via a HUB
- They function in HALF-DUPLEX
- You don’t need to configure the INTERFACE as SHARED (it should be detected)

💡 SW1(config-if)# spanning-tree link-type shared

---

QUIZ:

![image](https://github.com/psaumur/CCNA/assets/106411237/a7314f6f-55f0-4e62-bd24-b311b090afe8)

SW1 :

- **ROOT BRIDGE**
- G0/0 - 0/3= DESIGNATED

SW2 : 

- G0/0 = ROOT PORT
- G0/1 = DESIGNATED PORT
- G0/2 = BACKUP PORT
- G0/3 = DESIGNATED PORT

SW3 :

- G0/0 = DESIGNATED PORT
- G0/1 = ALTERNATE PORT
- G0/2 = ROOT PORT
- G0/3 = DESIGNATED PORT

SW4:

- G0/0 = ROOT
- G0/1 = ALTERNATE PORT
- G0/2 = DESIGNATED PORT

Connection between SW1 G0/0 and SW2 G0/0 = POINT-TO-POINT

Connection between SW3 G0/0 and SW4 G0/0 = POINT-TO-POINT

Connection between SW1 G0/1 and G0/2 to SW3 G0/1 and G0/2 = POINT-TO-POINT

Connections to all the END HOSTS = EDGE 

Connection from SW4 to HUB = SHARED

Connections from SW2 to HUB = SHARED

ANSWER

![image](https://github.com/psaumur/CCNA/assets/106411237/b76eb7be-897a-4617-990e-f399ceaea5f2)

# 23. ETHERCHANNEL

WHAT IS ETHERCHANNEL?

ETHERCHANNEL allows you to GROUP multiple physical INTERFACES into a group which operates as a SINGLE LOGICAL INTERFACE - so they BEHAVE as if they are a single INTERFACE

A LAYER 2 ETHERCHANNEL is a group of SWITCH PORTS which operate as a SINGLE INTERFACE

A LAYER 3 ETHERCHANNEL is a group of ROUTED PORTS which operate as a SINGLE INTERFACE which you assign an IP ADDRESS to.

![image](https://github.com/psaumur/CCNA/assets/106411237/86cecd4a-1554-4ece-8a88-6f97e24788f1)

When the bandwidth of the INTERFACES connected to END HOSTS is greater than the bandwidth of the connection to the DISTRIBUTION SWITCH(es), this is called **OVERSUBSCRIPTION.** 

Some OVERSUBSCRIPTION is acceptable, but too much will cause congestion.

![image](https://github.com/psaumur/CCNA/assets/106411237/6ada996f-8fd4-4339-9ad7-d52e51a3553e)

- If you connect TWO SWITCHES together with multiple links, ALL except ONE will be DISABLED by SPANNING TREE PROTOCOL (Green Lights vs. Orange Lights above on ASW1)

WHY?

- If ALL of ASW1s INTERFACES were FORWARDING, LAYER 2 LOOPS would form between ASW1 and DSW1, leading to a BROADCAST STORM (Bad!)
- Other links will be unused unless the active link fails. In that case, one of the inactive link will start forwarding.

An ETHERCHANNEL (in network topology diagrams) is represented like THIS (circle around multi-connections)

![image](https://github.com/psaumur/CCNA/assets/106411237/4c2cfcf8-57f2-4907-8322-2f26cc7dc7e4)

- ETHERCHANNEL groups multiple channels together to act as a SINGLE INTERFACE
- STP will treat this GROUP as a SINGLE INTERFACE

![image](https://github.com/psaumur/CCNA/assets/106411237/a48bed14-11b4-42ba-965a-9724598d3b69)

(All INTERFACES Green!)

TRAFFIC using ETHERCHANNEL will be load-balanced among the physical INTERFACES in the group.

An algorithm is used to determine WHICH TRAFFIC will use WHICH physical INTERFACE (more details later)

Some other names for an ETHERCHANNEL are:

- PORT CHANNEL
- LAG (Link Aggregation Group)

---

HOW DOES AN ETHERCHANNEL LOAD-BALANCE?

![image](https://github.com/psaumur/CCNA/assets/106411237/bc257ff8-bf91-4744-a6cb-8f603ee9d294)

- ETHERCHANNEL load-balances based on **“flows”**
- A “flow” is a communication between TWO NODES in the NETWORK
- FRAMES in the same “flow” will be FORWARDED using the SAME physical INTERFACE
- If FRAMES in the same “flow” were FORWARDED using different physical INTERFACES, some FRAMES may arrive at the DESTINATION out of order/sequence, which can cause problems.
- You can CHANGE the INPUTS used in the INTERFACE SELECTION calculation (for “flows”)
    - INPUTS that can be used:
        - SOURCE MAC ADDRESS
        - DESTINATION MAC ADDRESS
        - SOURCE and DESTINATION MAC ADDRESS
        - SOURCE IP ADDRESS
        - DESTINATION IP ADDRESS
        - SOURCE and DESTINATION IP ADDRESS

How to see the configuration for LOAD-BALANCING method

![image](https://github.com/psaumur/CCNA/assets/106411237/571623bf-b96b-4382-ada5-f14f93ec1a6a)

How to CHANGE the LOAD-BALANCING method

![image](https://github.com/psaumur/CCNA/assets/106411237/5919f2fd-80bb-4b10-bfa0-ce403f52c710)

![image](https://github.com/psaumur/CCNA/assets/106411237/bc30e17e-716a-41cd-a57a-69a661b5d58e)

---

HOW TO CONFIGURE LAYER 2 / LAYER 3 ETHERCHANNELS

There are THREE methods of ETHERCHANNEL configuration on Cisco SWITCHES

**PAgP (Port Aggregation Protocol)**

- Cisco proprietary protocol
- Dynamically negotiates the creation/maintenance of the ETHERCHANNEL (like DTP does for trunks)

💡 **LACP (Link Aggregation Control Protocol)**
- Industry standard protocol (IEEE 802.3ad)
- Dynamically negotiates the creation/maintenance of the ETHERCHANNEL (like DTP does for trunks)


**Static EtherChannel**

- A protocol isn’t used to determine if an EtherChannel should be formed
- Interfaces are statically configured to form an EtherChannel

Up to 8 INTERFACES can be formed into a single ETHERCHANNEL (LACP allows up to 16 but only 8 will be ACTIVE, the other 8 will in STANDBY mode, waiting for an active INTERFACE to fail)

 
---

PAgP CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/d0c734e2-79ad-43ad-a50b-c17ced608021)

💡 NOTE that “auto” and “desirable” are the ONLY available modes for PAgP

![image](https://github.com/psaumur/CCNA/assets/106411237/9eabb76a-1846-48d3-abb1-bd6898a432e7)

PAgP negotiations to form an ETHERCHANNEL


💡 AWS1(config-if-range)# channel-group 1 mode desirable.
Creating a port-channel interface Port-channel1

Shows up in the interface as “Port-channel1”

![image](https://github.com/psaumur/CCNA/assets/106411237/bc0c1190-9e39-4ea2-923c-b29e03e9d40a)

The “channel-group” number has to MATCH for member INTERFACES on the same SWITCH.

It DOESN’T have to MATCH the “channel-group” number on the OTHER SWITCH!

💡 (channel-group 1 on AWS1 can form an ETHERCHANNEL with channel-group 2 on DSW1)

---

LACP CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/ba4adcf6-dec5-456f-b8d7-ab4e6b722cbf)

💡 NOTE that “active” and “passive” are the ONLY available modes for LACP

![image](https://github.com/psaumur/CCNA/assets/106411237/0a314613-d398-49f1-a4d3-1b50fb96ab7d)

LACP negotiations for form an ETHERCHANNEL

The “channel-group” number has to MATCH for member INTERFACES on the same SWITCH.

It DOESN’T have to MATCH the “channel-group” number on the OTHER SWITCH!

💡 (channel-group 1 on AWS1 can form an ETHERCHANNEL with channel-group 2 on DSW1)

---

STATIC ETHERCHANNEL CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/92db26e7-21ae-40c6-89ee-abe0197ed8ad)

💡 NOTE that “on” is the ONLY available mode for STATIC ETHERCHANNEL

ON mode only works with ON Mode

ON + desirable = DOES NOT WORK)

ON + active = DOES NOT WORK

---

HOW TO MANUALLY CONFIGURE THE NEGOTIATION PROTOCOL

![image](https://github.com/psaumur/CCNA/assets/106411237/83ef9bc8-4bd4-4dd3-b28e-83439ba96860)

TWO OPTIONS: 

- LACP Protocol
- PAgP Protocol

(Above shows a protocol mismatch error because LACP does not support “desirable” - only PAgP does)

(“channel-group 1 mode active” works because LACP supports “active”)

---

AFTER CONFIGURING THE ETHERCHANNEL MODE

CONFIGURING THE PORT INTERFACE

![image](https://github.com/psaumur/CCNA/assets/106411237/c485cdf1-f0ed-44b8-8c91-c0553bf6d82d)

“show running-config” shows “interface Port-channel1” in the configuration

![image](https://github.com/psaumur/CCNA/assets/106411237/6adda3dd-6408-445f-bb3f-61847b3920b6)

💡 NOTE the PHYSICAL INTERFACES (g0/0-g0/3) were auto-configured by the Port-channel1 configuration!

---

IMPORTANT NOTES ABOUT ETHERCHANNEL CONFIGURATION

- Member INTERFACES must have matching CONFIGURATIONS
    - Same DUPLEX (Full / Half)
    - Same SPEED
    - Same SWITCHPORT mode (Access / Trunk)
    - Same allowed VLANs / Native VLAN (for TRUNK interfaces)

- If an INTERFACE’s configurations do NOT MATCH the others, it will be EXCLUDED from the ETHERCHANNEL

---

VERIFYING STATUS OF ETHERCHANNEL

💡 “show etherchannel summary”

![image](https://github.com/psaumur/CCNA/assets/106411237/9e0edb15-2806-4d51-afc9-ad67ed465a97)

NOTE information at bottom. (”SU” means S - Layer2 + U - in use)

Protocol = What protocol the Etherchannel is using (in this case, LACP)

“Ports” = the list of interfaces in the EtherChannel (P = bundled in port-channel)

OTHER FLAGS

![image](https://github.com/psaumur/CCNA/assets/106411237/23d92ae1-9cc6-4f3a-9ddf-2ead59705c1c)

“D” = Down

![image](https://github.com/psaumur/CCNA/assets/106411237/b1b3ce70-d9a6-4bd2-be4d-976077438c85)

Changing one of the Member interfaces using “switchport mode access” has made it different than the other members so it is now appearing as “s” = suspended

Another useful command

💡 “show etherchannel port-channel”

![image](https://github.com/psaumur/CCNA/assets/106411237/61731b0c-1cc5-4a7e-b92c-d0afbea0ac2d)

💡 “show spanning-tree” will show the single EtherChannel port interface

![image](https://github.com/psaumur/CCNA/assets/106411237/df0b9cc8-0448-4bbd-aefa-62fadf2b6089)

---

LAYER 3 ETHERCHANNELS

![image](https://github.com/psaumur/CCNA/assets/106411237/c553ad64-1d8e-4a2a-a741-3102c89dc030)

HOW TO CONFIGURE A LAYER 3 ETHERCHANNEL (from a clean configuration)

![image](https://github.com/psaumur/CCNA/assets/106411237/c4520b2f-1e3b-49b8-85b1-458cdb6fc865)

💡 “show running-config”

![image](https://github.com/psaumur/CCNA/assets/106411237/8638f32d-47c3-4c64-b68e-a9e2e0070ac9)

NOTE : No SWITCHPORT and NO IP INTERFACE.

Where do we configure the IP Address?  Directly on the PORT INTERFACE !

![image](https://github.com/psaumur/CCNA/assets/106411237/3ec55a24-1de5-44a7-926c-f85500042115)

![image](https://github.com/psaumur/CCNA/assets/106411237/f99ea2a6-82fb-494a-b80d-a171732d5786)

(”RU” - “R” = Layer 3, “U” = in use)

![image](https://github.com/psaumur/CCNA/assets/106411237/acfe62c5-6908-4782-9440-1f75f842c2c9)

---

COMMANDS LEARNED IN THIS CHAPTER
```
SW(config) port-channel load-balance *mode*
```
Configures the EtherChannel load-balancing method on a SWITCH 
```
SW# show etherchannel load-balance
```
Displays information about the load-balancing settings
```
SW(config-if)# channel-group *number* mode {desirable | auto | active | passive | on}
```
Configures an interface to be PART of an EtherChannel
```
SW# show etherchannel summary
```
Displays a summary of EtherChannels on a SWITCH
```
SW# show etherchannel port-channel
```
Displays information about the virtual port-channel interfaces on a SWITCH

![image](https://github.com/psaumur/CCNA/assets/106411237/6cae87f0-0226-40cc-92ba-b839c7a5ff53)

# 24. DYNAMIC ROUTING

WHAT IS DYNAMIC ROUTING?

![image](https://github.com/psaumur/CCNA/assets/106411237/8acc17ee-5d4b-4725-b5e4-18dc5743340e)

- LAYER 3
- Involves configuring a DYNAMIC ROUTING PROTOCOL on the ROUTER and letting the ROUTER take care of finding the best routes to DESTINATION NETWORKS.
- Not Fixed (will adapt to changes in the LAN)

![image](https://github.com/psaumur/CCNA/assets/106411237/deb9abf6-6e21-4c94-a407-bfc501a1d739)


💡 A NETWORK ROUTE :  A ROUTE to a NETWORK or SUBNET (Mask Length < /32)

Ex: **10.0.12.0/30** and **10.0.13.0/30** (above) are NETWORK ROUTES

💡 A HOST ROUTE : A ROUTE to a specific HOST (/32 Mask)

Ex: **10.0.12.1/32** and **10.0.13.1/32** (above) are HOST ROUTES

These two ROUTES were AUTOMATICALLY added to R1’s G0/0 and G1/0s INTERFACES

---

HOW DYNAMIC ROUTING WORKS ?

![image](https://github.com/psaumur/CCNA/assets/106411237/9d2d7f88-a325-461f-99fd-0dc88ee23749)

(R4 ADVERTISES to R2 who ADVERTISES to R1 who ADVERTISES to R3 - They add the NETWORK ROUTE to R4 in their ROUTE TABLE)

If the NETWORK ROUTE breaks, the ROUTE is DYNAMICALLY REMOVED from the ROUTE TABLE

![image](https://github.com/psaumur/CCNA/assets/106411237/a477d438-f6cb-4a09-b66d-e07826755bd1)

(R1 removing the ROUTE to R4 from it’s ROUTE TABLE)

IN STATIC ROUTING, a downed ROUTER will still have traffic passed to it. The ROUTE TABLES are unchanged.

![image](https://github.com/psaumur/CCNA/assets/106411237/e689a88a-7275-489c-80b4-18894a7ce4c9)

(R1 has a STATIC ROUTE to R4 and passes traffic destined to it’s NETWORK regardless of status)

DYNAMIC ROUTING is good but still requires REDUNDANCY so we add another connection between R3 and R4

![image](https://github.com/psaumur/CCNA/assets/106411237/8a7cb9cb-beea-4522-87f7-7fd11df9f745)

(Secondary DYNAMIC ROUTE added to R4 from R1 via R3. ROUTE TABLE updated appropriately)

A failure in the ROUTE, via R2 to R4’s G0/0 INTERFACE, automatically reroutes traffic via R3

![image](https://github.com/psaumur/CCNA/assets/106411237/d4509ce2-07f1-4fb0-8e31-cf58c049c355)

Why does the path prefer using R2’s path versus R3? 

Because of COST !  This is similar to how SPANNING-TREE works (with SWITCHES)

---

INTRODUCTION TO DYNAMIC ROUTING PROTOCOLS

- ROUTERS can use DYNAMIC ROUTING PROTOCOLS to ADVERTISE information about the ROUTES they know to OTHER ROUTES
- They form ‘ADJACENCIES’ / ‘NEIGHBOR RELATIONSHIPS’ / ‘NEIGHBORSHIPS’ with ADJACENT ROUTERS to exchange this information
- If multiple ROUTES to a DESTINATION are learned, the ROUTER determines which ROUTE is SUPERIOR and adds it to the ROUTING TABLE. It uses the ‘METRIC’ of the ROUTE to decide which is superior (lower metric = superior)

---

TYPES OF DYNAMIC ROUTING PROTOCOLS

DYNAMIC ROUTING PROTOCOLS can be divided into TWO main categories:

- IGP (Interior Gateway Protocol)
- EGP (Exterior Gateway Protocol)

IGP

- Used to SHARE ROUTES within a single *autonomous system* (AS), which is a single organization (ie: a company)

![image](https://github.com/psaumur/CCNA/assets/106411237/06af6c77-3a03-44fa-8c55-9382347d3f5e)

EGP

- Used to SHARE ROUTES *between* different *autonomous systems (AS)*

![image](https://github.com/psaumur/CCNA/assets/106411237/37680a4b-caab-4e1d-ac64-00a799bd965f)

Algorithms used for IGP and EGP and the PROTOCOL for each

![image](https://github.com/psaumur/CCNA/assets/106411237/36729569-0e56-4eb2-91ee-e7cd25a8c234)

💡 YOU MUST MEMORIZE WHICH ALGORITHM IS USED FOR EACH PROTOCOL FOR THE CCNA!

---

DISTANCE VECTOR ROUTING PROTOCOLS

- Called DISTANCE VECTOR because the ROUTERS only learn the ‘distance’ (METRIC) and ‘vector’ (DIRECTION, NEXT-HOP ROUTER) of each ROUTE

- DISTANCE VECTOR PROTOCOLS were invented before LINK STATE PROTOCOLS
- Early examples are RIPv1 and Cisco’s IGRP (which was updated to EIGRP)
- DISTANCES VECTOR PROTOCOLS operate by sending the following to their directly connection neighbors:
    - Their KNOWN DESTINATION networks
    - Their METRIC to reach their KNOWN DESTINATION networks
- This METHOD of sharing ROUTE information is often called ***‘routing by rumor’***
    - ***‘routing by rumor’*** = because the ROUTER doesn’t know about the NETWORK beyond it’s NEIGHBOURS. It only knows the information that the NEIGHBOURS tell it.

![image](https://github.com/psaumur/CCNA/assets/106411237/773eb20d-7983-4da4-ae66-e97e421e83ba)

---

DYNAMIC ROUTING PROTOCOL METRICS

- A ROUTER’S ROUTE TABLE contains the BEST ROUTE to each DESTINATION NETWORK it knows about

If a ROUTER using a DYNAMIC ROUTING PROTOCOL learns TWO different routes to the same DESTINATION, how does it determine which is **‘best’** ?

It uses the METRIC value of the ROUTES to determine which is BEST.

A lower METRIC = BETTER! (just like STP)

EACH ROUTING PROTOCOL uses a different METRIC to determine which ROUTE is best

![image](https://github.com/psaumur/CCNA/assets/106411237/bf324652-f4b8-482e-af17-03da590ac85d)

The above choose the RED PATH because the “cost”, using R3 F2/0 and R4 F2/0 (FastEthernet) is HIGHER than the  R2 G1/0 and R4 G0/0 (GigabyteEthernet)

What if BOTH connections were GigabyteEthernet? (ie: the same METRIC value)

![image](https://github.com/psaumur/CCNA/assets/106411237/3f8437cc-5b38-4f1e-b185-c5e9fce6c5f1)

BOTH ROUTES are added to the ROUTE TABLE

So …

💡 If a ROUTER learns TWO (or more) ROUTES via the same ****ROUTING PROTOCOL to the same DESTINATION (same network address, same subnet mask) with the same METRIC, both will be added to the routing table. Traffic will be LOAD-BALANCED over both ROUTES

![image](https://github.com/psaumur/CCNA/assets/106411237/79662f99-a847-457b-8080-76f77c25c5e6)

“O” = OSPF PROTOCOL (next to ROUTES)

[110/3] :

- the “3” part is the METRIC.
- the “110” part is ADMINISTRATIVE DISTANCE (covered later)


💡 Since BOTH ROUTES share the same METRIC, this is called ECMP (EQUAL COST MULTI-PATH)

You can have ECMP with STATIC ROUTES, as well (they don’t use METRIC, however)

---

SUMMARY OF DIFFERENT METRICS

![image](https://github.com/psaumur/CCNA/assets/106411237/7b8390aa-46d4-49d3-83a4-03ba095bf927)

(IS-IS won’t be covered in detail)

EXAMPLE

![image](https://github.com/psaumur/CCNA/assets/106411237/d0c6c9f2-3526-46b2-b520-1f4b6b28ea8f)

Using RIP, both ROUTES would be put in R1’s ROUTE TABLE

Using OSPF, only the ROUTE from R1 > R2 > R4 would be added to R1’s ROUTE TABLE because of the TOTAL COST of each link.

However, BOTH METRICS are trying to achieve the same thing :

To let the ROUTER select the BEST ROUTE to the DESTINATION

---

ADMINISTRATIVE DISTANCE

- In MOST cases, a company will only use a single IGP - usually OSPF or EIGRP
- However, in some RARE cases, they might use TWO.
    - Ex: If TWO companies connect their networks to share information, TWO different ROUTING PROTOCOLS might be in use.

- METRIC is used to compare ROUTES learned via the same ROUTING PROTOCOL

- Different ROUTING PROTOCOLS use totally different METRICS, so they cannot be compared
    - An OSPF ROUTE to 192.168.4.0/24 might have a METRIC of 30, while an EIGRP ROUTE to the same DESTINATION has a METRIC of 33280. Which ROUTE is better? Which route should the ROUTER put in the ROUTE TABLE ?

- The **ADMINISTRATIVE DISTANCE (AD)**, is used to determine which ROUTING PROTOCOL is preferred.
    - A LOWER AD is preferred, and indicates that the ROUTING PROTOCOL is considered more ‘trustworthy’ (more likely to select good ROUTES)

---

ADMINISTRATIVE DISTANCE NUMBERS

![image](https://github.com/psaumur/CCNA/assets/106411237/0f5ea405-d321-41bc-b2c0-2185874d07db)

(USE THE FLASHCARDS TO MEMORIZE THESE)

💡 IF the ADMINISTRATIVE DISTANCE is 255, the ROUTER does not believe the SOURCE of that ROUTE and does not install the ROUTE in the ROUTING TABLE!

![image](https://github.com/psaumur/CCNA/assets/106411237/33dbbe2b-7471-4c17-ae27-4d363d115a4c)

METRIC is used to COMPARE ROUTES learned from the SAME ROUTING PROTOCOL

However, before comparing METRICS, AD is used to select the BEST ROUTE

Therefore, the BEST ROUTE is :

“next hop 192.168.3.1, learned via OSPF (lower AD than RIP), metric 10”

- You can CHANGE the AD of a ROUTING PROTOCOL (This will be demonstrated in the lecture for OSPF CONFIGURATION)
- You can also change the AD of a STATIC ROUTE:

![image](https://github.com/psaumur/CCNA/assets/106411237/ec167f95-e5d7-49c8-aff7-1957e51934b1)

![image](https://github.com/psaumur/CCNA/assets/106411237/db6bef3b-ed82-49f0-b094-804c82f67f8d)

WHY WOULD YOU WANT TO DO THIS?

FLOATING STATIC ROUTES

- By CHANGING the AD of a STATIC ROUTE, you can make it less preferred than ROUTES learned by a DYNAMIC ROUTING PROTOCOL to the same DESTINATION (make sure the AD is HIGHER than the ROUTING PROTOCOL’s AD!)
- This kind of ROUTE is called a ‘FLOATING STATIC ROUTE’
- The ROUTE will be inactive (not in the ROUTING TABLE) unless the ROUTE learned by the DYNAMIC ROUTING PROTOCOL is removed.
    - **Ex:** The remote ROUTER stops ADVERTISING it for some reason, or an INTERFACE failure causes an ADJACENCY with a NEIGHBOR to be lost.

---

LINK STATE ROUTING PROTOCOLS

- When using a LINK STATE ROUTING PROTOCOL, every ROUTER creates a ‘connectivity map’ of the NETWORK
- To allow this, each ROUTER ADVERTISES information about its INTERFACES (connected NETWORKS) to its NEIGHBOURS. These ADVERTISEMENTS are passed along to the other ROUTERS, until all ROUTERS in the NETWORK develop the same map of the NETWORK
- Each ROUTER independently uses this MAP to calculate the BEST ROUTES to each DESTINATION
- LINK STATE PROTOCOLS use more resources (CPU) on the ROUTER, because MORE information is shared.
- However, LINK STATE PROTOCOLS tend to be FASTER in reacting to CHANGES in the NETWORK than DISTANCES VECTOR PROTOCOLS

# 25. RIP and EIGRP (IGP : DYNAMIC VECTOR)

ROUTING INFORMATION PROTOCOL (RIP)

- Routing Information Protocol (Industry Standard)
- is a DISTANCE VECTOR IGP
    - uses Routing-By-Rumor logic to learn/share routes
- Uses HOP COUNT as it’s METRIC (One Router = One Hop)  Bandwidth is irrelevant
- MAX HOP COUNT is 15 (anything more is considered unreachable)
- Has THREE VERSIONS:
    - RIPv1 and RIPv2; used for IPv4
    - RIPng (RIP Next Generation) used for IPv6
- Uses TWO MESSAGE TYPES:
    - REQUEST :
        - To ask RIP-ENABLED neighbour ROUTERS to send their ROUTING TABLE
    - RESPONSE:
        - To SEND the LOCAL router’s ROUTING TABLE to neighbouring ROUTERS

By DEFAULT, RIP-Enabled ROUTERS will share their ROUTING TABLE every 30 seconds

RIPv1 and RIPv2

RIPv1:

- Only advertises *classful addresses* (Class A, Class B, Class C)
- Doesn’t support VLSM, CIDR
- Doesn’t include SUBNET MASK information in ADVERTISEMENTS (RESPONSE messages)
    - Example:
        - 10.1.1.0/24 will become 10.0.0.0 (Class A Address, so assumed to be /8)
        - 172.16.192.0/18 will become 172.16.0.0 (Class B Address, so assumed to be /16)
        - 192.168.1.40/30 will become 172.168.1.0 (Class C Address, so assumed to be /24)
- Messages are BROADCAST to 255.255.255.255

RIPv2:

- Supports VLSM, CIDR
- Includes SUBNET MASK information in ADVERTISEMENTS
- Messages are **multicast** to 224.0.0.9
    - Broadcast Messages are delivered to ALL devices on the local network
    - Multicast Messages are delivered only to devices to have joined that specific ***multicast group***

---

CONFIGURING RIP

![image](https://github.com/psaumur/CCNA/assets/106411237/1d14ec8b-121c-4666-b608-1e5d1889424c)

The **“network”** command tells the router to:

- Look for INTERFACES with an IP ADDRESS that is in the specific RANGE
- ACTIVATES RIP on the INTERFACES that fall in the RANGE
- Form ADJACENCIES with connected RIP neighbors
- Advertise the **NETWORK PREFIX of the INTERFACE** (NOT the prefix in the “network” command)

The OSPF and EIGRP **“network”** commands operate in the same way

Because the RIP “network” command is CLASSFUL. It will automatically convert to CLASSFUL networks

- 10.0.0.0 is assumed to be 10.0.0.0/8
- R1 will look for ANY INTERFACES with an IP ADDRESS that matches 10.0.0.0/8 (because it is /8 it only needs to match the FIRST 8 bits)
- 10.0.12.1 and 10.0.13.1 both match SO RIP is ACTIVATED on G0/0 and G0/1
- R1 then forms ADJACENCIES with its neighbors R2 and R3
- R1 ADVERTISES 10.0.12.0/30 and 10.0.13.0/30 (NOT 10.0.0.0/8) to it’s RIP neighbors

![image](https://github.com/psaumur/CCNA/assets/106411237/2a9452f0-b48f-499d-938f-0a3db5ff6587)

- Because the “network” command is CLASSFUL, 172.16.0.0 is assumed to be 172.16.0.0/16
- R1 will look for ANY INTERFACES that match 172.16.0.0/16
- 172.16.1.14 matches, so R1 will ACTIVATE RIP on G2/0
- There are NO RIP neighbors connected to G2/0 so no NEW ADJACENCIES are formed
    - Although there are NO RIP neighbors, R1 will still send ADVERTISEMENTS out of G2/0.
    - This is unnecessary traffic, so G2/0 should be configured as a **passive interface**

![image](https://github.com/psaumur/CCNA/assets/106411237/634f4c6b-291c-4a21-8ae2-c8283044efce)

- the “passive-interface” command tells the ROUTER to stop sending RIP advertisements out of the specified interface (G2/0)
- However, the ROUTER will continue to ADVERTISE the network prefix of the interface (172.16.1.0/28) to it’s RIP neighbors (R2, R3)
- You should ALWAYS use this command on INTERFACES which don’t have any RIP neighbors
- EIGRP and OSPF both have the same passive INTERFACE functionality, using the same command.

---

HOW TO ADVERTISE A DEFAULT ROUTE INTO RIP

![image](https://github.com/psaumur/CCNA/assets/106411237/57de003e-0e8e-48c7-bb72-fbe25208d847)

![image](https://github.com/psaumur/CCNA/assets/106411237/1c500efd-e96b-4e49-b1f4-f99c54b0e877)

To SHARE this DEFAULT ROUTE with R1’s RIP neighbors, using this command:

![image](https://github.com/psaumur/CCNA/assets/106411237/799d818a-06cc-4f29-8c74-c67639c9d014)

RIP doesn’t care about interface AD cost (RIP cost is 120), only “hops”.

Since both have an equal number of “hops”, both paths appear in the DEFAULT ROUTE (Gateway of Last Resort)

![image](https://github.com/psaumur/CCNA/assets/106411237/1deccb54-02e0-4d3b-b203-277d656504b3)

---

“show ip protocols” (for RIP)

![image](https://github.com/psaumur/CCNA/assets/106411237/b7ab4046-b6eb-4e19-b7eb-2c5d2889293a)

“Maximum path: 4” is the DEFAULT but can be changed with this command:

![image](https://github.com/psaumur/CCNA/assets/106411237/35d524bd-055d-4c5e-a84b-f507a87738e0)

“Distance” (AD) can be changed with this command (DEFAULT is 120)

![image](https://github.com/psaumur/CCNA/assets/106411237/5247942b-1d6b-419f-a4c7-75bfcca43fe6)

---

ENHANCED INTERIOR GATEWAY ROUTING PROTOCOL (EIGRP)

- Enhanced Interior Gateway Routing Protocol
- is a DISTANCE VECTOR IGP
- Was Cisco proprietary, but Cisco has now published it openly so other vendor can implement it on their equipment
- Considered an “advanced” / “hybrid” DISTANCE VECTOR ROUTING PROTOCOL
- Much faster than RIP in reacting to changes in the NETWORK
- Does NOT have the 15 ‘hop count’ limit of RIP
- Sends messages using MULTICAST ADDRESS **224.0.0.10 (Memorize this number)**
- Is the ONLY IGP that can perform **unequal**-cost load-balancing (by DEFAULT, it performs ECMP load-balancing over 4 paths like RIP)

---

CONFIGURATION OF EIGRP

![image](https://github.com/psaumur/CCNA/assets/106411237/f2b42631-bcb9-4f62-afe9-b7bb1e7e0d7e)

“router eigrp <Autonomous System number>”

- The AS (Autonomous System) number MUST MATCH between ROUTERS or they will NOT form an ADJACENCY and share ROUTE information
- Auto-summary might be ENABLED or DISABLED by DEFAULT; depending on the ROUTER/IOS version. If ENABLED, DISABLE it.
- The **“network”** command will assume a CLASSFUL ADDRESS, if you don’t specify the SUBNET MASK
- EIGRP uses a *wildcard mask* instead of a regular subnet mask

A WILDCARD MASK is an “inverted” SUBNET MASK

- All 1’s in the SUBNET MASK are 0 in the equivalent WILDCARD MASK.
- All 0s in the SUBNET MASK are 1 in the equivalent WILDCARD MASK.

![image](https://github.com/psaumur/CCNA/assets/106411237/f64e06d3-75ad-4f4f-b7d6-26f27ffae541)

“0” in the WILDCARD MASK = BITS MUST MATCH !

“1” in the WILDCARD MASK = Do not have to match

![image](https://github.com/psaumur/CCNA/assets/106411237/13130e3c-de62-4f80-9c7d-256a2ed47e74)

![image](https://github.com/psaumur/CCNA/assets/106411237/1aa2cd2c-397f-4f3b-86ed-81eddf2677a6)

![image](https://github.com/psaumur/CCNA/assets/106411237/500ac3b0-5d83-4691-ab94-06fd330a9111)

---

“show ip protocols” (for EIGRP)

![image](https://github.com/psaumur/CCNA/assets/106411237/f3f169da-d733-4da9-8d8a-c90e2077d8a7)

“Router ID”

ROUTER ID order of priority:

- Manual configuration
- Highest IP ADDRESS on a LOOPBACK INTERFACE
- Highest IP ADDRESS on a PHYSICAL INTERFACE

![image](https://github.com/psaumur/CCNA/assets/106411237/29757624-9e79-4878-8724-36d5da43f39b)

“Distance” (AD)

EIGRP has TWO VALUES:

- Internal = 90
- External = 170

MEMORIZE THESE VALUES!

“show ip route” (for EIGRP)

![image](https://github.com/psaumur/CCNA/assets/106411237/8216ceb6-0d3f-42e7-8e5b-46e810097fb8)

NOTE the large METRIC numbers. This is a DOWNSIDE to EIGRP - even on small networks!

---

EIGRP METRIC

- By DEFAULT, EIGRP uses BANDWIDTH and DELAY to calculate METRIC
- Default “K” values are:
    - K1 = 1, K2 = 0, K3 = 1, K4 = 0, K5 = 0

💡 Simplified calculation : METRIC = BANDWIDTH (Slowest Link) + DELAY (of ALL LINKS)

---

EIGRP TERMINOLOGY

- **Feasible Distance** = This ROUTER’s METRIC value to the ROUTE’s DESTINATION
- **Reported Distance** (aka **Advertised Distance**) = The neighbor’s METRIC value to the ROUTE’s DESTINATION

![image](https://github.com/psaumur/CCNA/assets/106411237/436ba2c2-43e7-4fea-a527-f88a8e4460bc)

- **Successor =** the ROUTE with the LOWEST METRIC to the DESTINATION (the best route)
- **Feasible Successor** = An alternate ROUTE to the DESTINATION (not the best route) which meets the *feasibility condition*

**FEASIBILITY CONDITION** : A ROUTE is considered a ***Feasible Successor*** if it’s ***Reported Distance*** is LOWER than the Successor ROUTE’s ***Feasible distance***

![image](https://github.com/psaumur/CCNA/assets/106411237/206db633-3a7e-4d11-bb80-029ea8107503)

---

EIGRP : UNEQUAL-COST LOAD-BALANCED

![image](https://github.com/psaumur/CCNA/assets/106411237/23a2045b-a925-4f75-b0f8-78cbae2aa1e2)

“maximum metric variance 1” = the DEFAULT value

Variance 1 = only ECMP (Equal-Cost Multiple Path) load-balancing will be performed

![image](https://github.com/psaumur/CCNA/assets/106411237/824dac1d-38dc-4e7e-bb48-b382918230ff)

Variance 2 = ***feasible successor*** routes with an FD up to 2x the ***successor*** route’s FD can be used to load-balance

💡 EIGRP will only perform UNEQUAL-COST LOAD-BALANCING over ***feasible successor*** ROUTES. If a ROUTE doesn’t meet the ***feasibility condition***, it will NEVER be selected for load-balancing, regardless of **variance**

# 26.  OSPF : PART 1 (IGP : LINK STATE)

![image](https://github.com/psaumur/CCNA/assets/106411237/f58477d1-f574-4195-8f6c-851823dedfbf)

LINK STATE ROUTING PROTOCOLS

- When using a LINK STATE ROUTING PROTOCOL, every ROUTER creates a ‘connectivity map’ of the NETWORK
- To allow this, each ROUTER ADVERTISES information about its INTERFACES (connected NETWORKS) to its NEIGHBOURS. These ADVERTISEMENTS are passed along to the other ROUTERS, until all ROUTERS in the NETWORK develop the same map of the NETWORK
- Each ROUTER independently uses this MAP to calculate the BEST ROUTES to each DESTINATION
- LINK STATE PROTOCOLS use more resources (CPU) on the ROUTER, because MORE information is shared.
- However, LINK STATE PROTOCOLS tend to be FASTER in reacting to CHANGES in the NETWORK than DISTANCES VECTOR PROTOCOLS

---

BASIC OSPF OPERATIONS

- Stands for **Open Shortest Path First**
- Uses the **Shortest Path First** algorithm
    - Created by Dutch comp. scientist - Edsger Dijkstra
    - aka **Dijkstra’s Algorithm** (Could be Exam Question)

THREE Versions:

- OSPFv1 (1989) : OLD, not in use anymore
- OSPFv2 (1998) : Used for IPv4
- OSPFv3 (2008) : Used for IPv6 (can be used for IPv4, but v2 is usually used)

- Routers store information about the NETWORK in LSAs (Link State Advertisements), which are organized in a structure called the LSDB (Link State Database)
- Routers will **FLOOD** LSAs until all ROUTERS in the OSPF *area* develop the same map of the network (LSDB)

![image](https://github.com/psaumur/CCNA/assets/106411237/2a6a126b-74f1-49e2-96be-fc411c8812fd)

💡 LSA’s have an AGING TIMER of 30 Minutes, by Default). The LSA will be FLOODED again after the timer expires

In OSPF, there are THREE MAIN STEPS in the process of sharing LSAs and determining the BEST ROUTE to each DESTINATION in the network

1) **BECOME NEIGHBORS** with other ROUTERS connected to same SEGMENT

2) **EXCHANGE LSAs** with neighbor ROUTERS

3) **CALCULATE THE BEST ROUTES** to each DESTINATION, and insert them into the ROUTING TABLE

---

OSPF AREAS

- OSPF uses **AREAS** to divide up the NETWORK
- SMALL NETWORKS can be *single-area* without any negative effects on performance
- LARGE NETWORKS, *single-area* design can have NEGATIVE effects:
    - SPF ALGORITHM takes more time to calculate ROUTES
    - SPF ALGORITHM requires exponentially more processing power on ROUTERS
    - Larger LSDB takes up more MEMORY on ROUTERS
    - Small changes in NETWORK cause every ROUTER to FLOOD LSAs and run the SPF algorithm again
- By dividing up a large OSPF NETWORK into several SMALLER ***areas***, you can avoid the above NEGATIVE effects (sounds similar to VLANs re: broadcast domains)

WHAT IS AN OSPF AREA?

![image](https://github.com/psaumur/CCNA/assets/106411237/0f5084fe-f7fb-4b33-a8d0-2ed0155d7502)

- An **AREA is** a set of ROUTERS and LINKS that share the same LSDB
- The **BACKBONE AREA** (Area 0) is an AREA that all other AREAS must connect to
- ROUTERS with ALL INTERFACES in the SAME AREA are called INTERNAL ROUTERS
- ROUTERS with INTERFACES in MULTIPLE AREAS are called **AREA BORDER ROUTERS** (ABRs)
    

💡 ABRs maintain a SEPARATE LSDB for each AREA they are connected to.

💡 It is recommended that you connect an ABR to a MAXIMUM of TWO AREAS.

💡 Connecting an ABR to 3+ AREAS can overburden the ROUTER

- ROUTERS connected to the BACKBONE AREA (Area 0) are called **BACKBONE ROUTERS**
- An **INTRA-AREA ROUTE** is a ROUTE to a DESTINATION inside the same OSPF AREA
- An INTER-AREA ROUTE is a ROUTE to a DESTINATION in a DIFFERENT OSPF AREA

--- 

OSPF RULES

- OSPF AREAS should be CONTIGUOUS (no split AREAS)
- All OSPF AREAS must have *at least* ONE ABR connected to the BACKBONE AREA
- OSPF INTERFACES in the SAME SUBNET *must* be in the SAME AREA

---
BASIC OSPF CONFIGURATION

OSPF AREA 0

![image](https://github.com/psaumur/CCNA/assets/106411237/ad9648f4-736a-43b5-96de-8a30f6f800c8)

Commands for configuring an OSPF 

![image](https://github.com/psaumur/CCNA/assets/106411237/38fcce32-8d15-4db0-9a0c-170d6083a534)

- The OSPF **Process ID** is **locally significant.** ROUTERS with different Process IDs can become OSPF Neighbors
- The OSPF “network” command requires you to specify the AREA (in this case, it’s “area 0”)
- For the CCNA, you only need to configure single-area OSPF (AREA 0)

The “network” command tells OSPF to:

- Look for ANY INTERFACES with an IP ADDRESS contained in the RANGE specified in the “network” command
- Activate OSPF on the INTERFACE in the specified AREA
- The ROUTER will then try to become OSPF neighbors with other OSPF-Activated neighbor ROUTERS

![image](https://github.com/psaumur/CCNA/assets/106411237/41da3fe8-f24a-468c-beeb-91cc12066c70)

- Know this command from RIP and EIGRP
- The “passive-interface” command tells the ROUTERS to stop sending OSFP ‘hello’ messages out of the INTERFACE
- However, the ROUTER will continue to send LSA’s informing it’s neighbors about the SUBNET configured on the INTERFACE
- You should ALWAYS USE this command on neighbors which don’t have any OSPF neighbors

![image](https://github.com/psaumur/CCNA/assets/106411237/a0422f88-dbd9-4965-8c73-16cfd438b05e)

![image](https://github.com/psaumur/CCNA/assets/106411237/aaa1daaa-8ab7-441a-bec2-9f0391a82ecc)

“show ip protocols”

![image](https://github.com/psaumur/CCNA/assets/106411237/f02c3838-c9ad-4836-8c89-ecad42e205b2)

NOTE the "no" in square brackets - this indicates this is the DEFAULT choice

![image](https://github.com/psaumur/CCNA/assets/106411237/c222d290-4d10-4e63-b7d5-8317ae5ccdfc)

DISTANCE (AD) for OSPF is 110 (DEFAULT) but can be changed with the “distance” command

![image](https://github.com/psaumur/CCNA/assets/106411237/849a7fd3-457e-4310-be08-b4c8b4c8a8a2)

# 27. OSPF : PART 2 (IGP : LINK STATE)

OSPF METRIC (Cost)

- OSPFs METRIC is called **COST**
- It is automatically calculated based on the bandwidth (SPEED) of the INTERFACE
- It is calculated by DIVIDING a REFERENCE BANDWIDTH value by the INTERFACE bandwidth
- The DEFAULT REFERENCE BANDWIDTH is 100 mbps
    - REFERENCE: 100 mbps / INTERFACE: 10 mbps = COST (10)
    - REFERENCE: 100 mbps / INTERFACE: 100 mbps = COST (1)
    - REFERENCE: 100 mbps / INTERFACE: 1000 mbps = COST (1)
    - REFERENCE: 100 mbps / INTERFACE: 10000 mbps = COST (1)
- ALL COST values less than 1 will be CONVERTED to 1
- Therefore FastEthernet (100 mbps), Gigabit Ethernet (1000 mbps), 10 Gig Ethernet, etc. are EQUAL and all have a COST of 1

FastEthernet COST

![image](https://github.com/psaumur/CCNA/assets/106411237/453258a2-e724-4bf5-b07c-6c533dcef46c)

Gigabit Ethernet COST

![image](https://github.com/psaumur/CCNA/assets/106411237/17adfd0e-8944-4016-93bd-98b82ceb8a66)

You can (and SHOULD) change the REFERENCE BANDWIDTH with this command:

💡 R1(config-router)# **auto-cost reference-bandwidth** *megabits-per-second*

The command is entered in “megabits per second” (DEFAULT is “100”)

Example: using a value of “100000”

- 100000 / 100 = COST of 1000 for FastEthernet
- 100000 / 1000 = COST of 100 for Gig Ethernet

You should configure a reference bandwidth GREATER than the FASTEST links in your NETWORK (to allow for future upgrades)

Changing the REFERENCE BANDWIDTH needs to be done on ALL OSPF ROUTERS in the NETWORK

---

THE OSPF COST to a DESTINATION is the TOTAL COST of the ‘outgoing/exit INTERFACES’

LOOPBACK INTERFACES have a COST of 1

![image](https://github.com/psaumur/CCNA/assets/106411237/ef8de0f8-c22d-4259-bf4c-6fc9894bae29)

To CHANGE the OSPF COST of an INTERFACE, you use the command :

<aside>
💡 R1(config-if)# ip ospf cost <cost>
</aside>

MANUAL COSTS take precedent over AUTOMATIC CALCULATED COST

One more option to change the OSPF COST of an INTERFACE is to change the BANDWIDTH of the INTERFACE with the **“bandwidth”** command

The FORMULA to CALCULATE OSPF COST is :

<aside>
💡 **reference bandwidth / interface bandwidth**

</aside>

- Although the BANDWIDTH matches the INTERFACE SPEED (by DEFAULT), changing the INTERFACE BANDWIDTH **doesn’t actually change the speed at which the INTERFACE operates**
- The BANDWIDTH is just a VALUE that is used to calculate OSPF COST, EIGRP METRIC, etcetera…
- To CHANGE the SPEED at which the INTERFACE operates, use the **“speed”** command
- Because the BANDWIDTH VALUE is used in other calculations, it is NOT recommended to change this VALUE to alter the INTERFACE’s OSPF COST

It is RECOMMENDED that you CHANGE the REFERENCE BANDWIDTH

THEN use the **“ip ospf cost”** command to change the COST of the individual INTERFACES, if you want.

![image](https://github.com/psaumur/CCNA/assets/106411237/00196380-4452-4ec9-8cd9-b1949665a5d8)

---

SUMMARY:

THREE WAYS to modify the OSPF COST:

1) Change the ***reference bandwidth***

<aside>
💡 R1(config-router)# **auto-cost reference-bandwidth** *megabits-per-second*
</aside>

2) Manual configuration:

<aside>
💡 R1(config-router)# ip ospf cost <cost>
</aside>

3) Change the ***interface bandwidth***

<aside>
💡 R1(config-router)# **bandwidth <***kilobits-per-second>*
</aside>

![image](https://github.com/psaumur/CCNA/assets/106411237/aba02fbc-174c-41a1-a8e3-0ffdda3a6cbd)

---

BECOMING OSPF NEIGHBORS

- Making sure that ROUTERS successfully become OSPF NEIGHBORS is the MAIN task in configuring and troubleshooting OSPF.
- Once ROUTERS become NEIGHBORS, they AUTOMATICALLY do the work of sharing NETWORK information, calculating routes, etc.
- When OSPF is activated on an INTERFACE, the ROUTER starts sending OSPF **“hello”** messages out of the INTERFACE at regular intervals (determined by the **“hello timer”).** These are used to introduce the ROUTER to potential OSPF NEIGHBORS
- The DEFAULT “**hello timer**” is **10 SECONDS** on an Ethernet connection
- **Hello** messages are MULTICAST to **224.0.0.5** (multicast address for ALL OSPF ROUTERS)
- OSPF messages are ENCAPSULATED in an IP HEADER, with a **value of “89”** in the PROTOCOL field.

DOWN STATE

- OSPF is activated on R1s G0/0 INTERFACE
- It sends an OSPF “hello” message to 224.0.0.5
- It doesn’t know about any OSPF neighbors yet, so the current neighbor state is DOWN

![image](https://github.com/psaumur/CCNA/assets/106411237/fa9b91da-e0c3-42d9-8c0a-eb47991b1894)

INIT STATE

- When R2 receives the “hello” packet, it will add an entry for R1 to its OSPF neighbor table
- In R2’s neighbor table, the relationship with R1 is now in the INIT state
- INIT state = “hello” packet received, but own ROUTER ID is not in the “hello” packet

![image](https://github.com/psaumur/CCNA/assets/106411237/70f3474f-f4bf-4194-b479-d7a65ad82505)

2-WAY STATE

- R2 will send a “hello” packet containing the RID of BOTH ROUTERS
- R1 will insert R2 into its OSPF neighbor table in the 2-WAY state
- R1 will send another “hello” message, this time containing R2’s RID
- Both ROUTERS are now in the 2-WAY state

![image](https://github.com/psaumur/CCNA/assets/106411237/4d5e5310-4680-4176-94ab-2d8015032d18)

- The 2-WAY state means the ROUTER has received a “hello” packet with its own RID in it
- If both ROUTERS reach the 2-WAY state, it means that ALL of the conditions have been met for them to become OSPF neighbors.
- They are now READY to SHARE LSAs to build a common LSDB.
- In SOME NETWORK types, a DR (Designated ROUTER) and BDR (Backup Designated Router) will be elected at this point (OSPF Network Types and DR/DBR elections will be discussed in Day 28)

EXSTART STATE

- The TWO ROUTERS will now prepare to exchange information about their LSDB
- Before that, they have to choose which one will START the exchange
- They do THIS in the EXSTART state
    - The ROUTER with the higher RID will become the MASTER and initiate the exchange.
    - The ROUTER with the lower RID will become the SLAVE
- To decide the MASTER and SLAVE, they exchange DBD (Database Description) packets

![image](https://github.com/psaumur/CCNA/assets/106411237/34fa7cca-f837-432b-9296-d1be69a8869c)

EXCHANGE STATE

- In the EXCHANGE state, the ROUTERS exchange DBDs which contain a LIST of the LSAs in their LSDB
- These DBDs do NOT include detailed information about the LSAs, just BASIC INFORMATION
- The ROUTERS compare the information in the DBD they received to the information in their OWN LSDB to determine which LSAs they must receive from their neighbor

![image](https://github.com/psaumur/CCNA/assets/106411237/600722df-4737-4a69-867e-662c03a6b4b4)

LOADING STATE

- In the LOADING state, ROUTERS send **Link State Requests (LSR)** messages to request that their neighbors SEND them any LSAs they don’t have
- LSAs are sent in **Link State Update (LSU)** messages
- The ROUTERS send **LSAck** messages to acknowledge that they received the LSAs

![image](https://github.com/psaumur/CCNA/assets/106411237/4fc0fc23-ce00-4381-afef-259091b8f8ef)

FULL STATE

- In the FULL state, the ROUTERS have a FULL OSPF adjacency and identical LSDBs
- They continue to SEND and LISTEN for “hello” packets (every 10 seconds by default) to maintain the neighbor adjacency
- Every time a “hello” packet is received, the “DEAD” timer (40 seconds by default) is reset
- If the DEAD timer counts down to 0 and no “hello” message is received, the neighbor is REMOVED
- The ROUTERS will continue to share LSAs as the network changes to make sure each ROUTER has a COMPLETE and ACCURATE map of the NETWORK (LSDB)

![image](https://github.com/psaumur/CCNA/assets/106411237/daaa3a7b-ddd0-4ad0-ace7-056cbf2fbe32)

---

OSPF NEIGHBORS SUMMARY:

![image](https://github.com/psaumur/CCNA/assets/106411237/0d9f9d7e-04fd-472c-8449-a4f12172c055)

1 ) BECOME NEIGHBORS

- DOWN STATE
- INIT STATE
- 2-WAY STATE
- (DR/BDR ELECTION)

2) EXCHANGE LSAs

- EXSTART STATE
- EXCHANGE STATE
- LOADING STATE

---

SUMMARY OF OSPF MESSAGE TYPES

![image](https://github.com/psaumur/CCNA/assets/106411237/05b6d3ee-8fdb-4f25-9214-557eeb9a53a6)

---

MORE OSPF CONFIGURATIONS

Activate OSPF DIRECTLY on an INTERFACE with this command:

<aside>
💡 R1(config-if)# ip ospf *process-id* area *area*

</aside>

![image](https://github.com/psaumur/CCNA/assets/106411237/ad7aafd6-9cd8-4259-bd32-aff7b5893b46)

Configure ALL INTERFACES as OSPF Passive Interfaces

<aside>
💡 R1(config-router) #passive-interface default

</aside>

![image](https://github.com/psaumur/CCNA/assets/106411237/e953696d-283f-4676-8df2-9aff0418d78d)

Can then REMOVE specific INTERFACES from being passive using:

<aside>
💡 R1(config-router) #no passive-interface *interface-id*

</aside>

Activating OSPF DIRECTLY on INTERFACES will show a different output in “show ip protocols”

![image](https://github.com/psaumur/CCNA/assets/106411237/915e31ee-4fee-455b-a947-229e0af4b182)

They will appear under “Routing on Interfaces Configured Explicitly (Area #) :” (as above)

Showing the OSPF LSDB of a Device

![image](https://github.com/psaumur/CCNA/assets/106411237/75c941ca-b6bd-45f0-9a85-c7e5baff4654)

# 28. OSPF : PART 3 (IGP: LINK STATE)

LOOPBACK INTERFACES

- A LOOPBACK INTERFACE is a virtual INTERFACE in the ROUTER
- It is ALWAYS UP/UP - unless you manually shut it down
- It is NOT dependent on a PHYSICAL INTERFACE
- So, it provides a consistent IP ADDRESS that can be used to REACH / IDENTIFY the ROUTER

![image](https://github.com/psaumur/CCNA/assets/106411237/697e7d43-b428-4fe3-a270-5fc1c9ad13d0)

---

OSPF NETWORK TYPES

- The OSPF “NETWORK TYPE” refers to the TYPES of connection between OSPF neighbors (Ethernet, etc.)

- There are THREE MAIN OSPF NETWORK TYPES:

- BROADCAST :
    - Enabled by DEFAULT on **ETHERNET** and **FDDI** (Fiber Distributed Data Interfaces) INTERFACES

- POINT TO POINT :
    - Enabled by DEFAULT on **PPP** (Point-to-Point) and **HDLC** (High-Level Data Link Control) INTERFACES

- NON-BROADCAST :
    - Enabled by DEFAULT on **FRAME RELAY** and **X.25** INTERFACES

<aside>
💡  CCNA focuses on BROADCAST and POINT-TO-POINT types

</aside>

---

OSPF BROADCAST NETWORK TYPE

![image](https://github.com/psaumur/CCNA/assets/106411237/8f99053d-3501-4d1d-86a2-f859c62c160d)

- Enabled on ETHERNET and FDDI interfaces by DEFAULT
- ROUTERS *dynamically discover* neighbors by SENDING / LISTENING for OSPF “Hello” messages using the multicast address 224.0.0.5
- A **DR (DESIGNATED ROUTER)** and **BDR (BACKUP DESIGNATION ROUTER)** must be elected on each subnet (only DR if there are no OSPF neighbors, ie: R1’s G1/0 INTERFACE)
- ROUTERS which aren’t the DR or BDR become a **DROther**

![image](https://github.com/psaumur/CCNA/assets/106411237/1ba5b6e1-dd4a-4277-8f33-f806e21302bc)

The DR / BDR election order of priority:

1) Highest OSPF INTERFACE PRIORITY

2) Highest OSPF ROUTER ID

“First Place” becomes the DR for the SUBNET

“Second Place” because the BDR

<aside>
💡 DEFAULT OSPF INTERFACE PRIORITY is “1” on ALL INTERFACES!

</aside>

The command to change the OSPF PRIORITY of an INTERFACE is :

<aside>
💡 R2(config-if)# ip ospf priority <priority number>

</aside>

![image](https://github.com/psaumur/CCNA/assets/106411237/cd98b06f-3730-4b2d-8dfe-a6387fdb66a1)

<aside>
💡 IF an OSPF PRIORITY is set to “0”, the ROUTER CANNOT be the DR / BDR for the SUBNET!

</aside>

The DR / DBR ELECTION is “non-preemptive”.

Once the DR / DBR are selected, they will keep their role until OSPF is:

- Reset
- Interface fails
- Is shut down
- etc.

![image](https://github.com/psaumur/CCNA/assets/106411237/e59e6217-0404-476d-9bcf-49e82c380b84)

![image](https://github.com/psaumur/CCNA/assets/106411237/82eb1f11-4aed-456b-b2b1-1679cae06743)

<aside>
💡 In the BROADCAST NETWORK TYPE, ROUTERS will only form a FULL OSPF ADJACENCY with the DR and the BDR of the SEGMENT!

</aside>

Therefore, ROUTERS only exchange LSAs with the DR and BDR.

DROthers will NOT exchange LSAs with each other.

ALL ROUTERS will still have the same LSDB but THIS reduces the amount of LSAs flooding the NETWORK

<aside>
💡 MESSAGES to the DR / BDR are MULTICAST to 224.0.0.6

</aside>

The DR and BDR will form a FULL ADJACENCY with ALL ROUTERS in the SUBNET

DROthers will form a FULL ADJACENCY ONLY with the DR / BDR !

![image](https://github.com/psaumur/CCNA/assets/106411237/61e1c230-3926-40ae-917a-55fcf76caf64)

---

OSPF POINT-TO-POINT NETWORK TYPE

![image](https://github.com/psaumur/CCNA/assets/106411237/51d7d486-a810-4a69-8be2-804f667fca03)

- ENABLED on **SERIAL** INTERFACES using the **PPP** and **HDLC** encapsulations, by DEFAULT
- ROUTERS dynamically discover neighbors by SENDING / LISTENING for OSPF “Hello” messages using the multicast address 224.0.0.5
- A DR and BDR are NOT elected
- These ENCAPSULATIONS are used for “Point-To-Point” connections
    - Therefore, there is no point in electing  a DR and DBR
    - The TWO ROUTERS will form a FULL ADJACENCY with each other

---

(ASIDE)

SERIAL INTERFACES

![image](https://github.com/psaumur/CCNA/assets/106411237/02f6f3a8-dcbb-46cd-bb2e-47ceb84d10cc)

- One side of SERIAL CONNECTION functions as DCE (Data Communications Equipment)
- The OTHER side functions as DTE (Data Terminal Equipment)
- ONLY the DCE side needs to specify the *clock rate* (speed) of the connection

ETHERNET INTERFACES use the “speed” command to configure the operating speed.

SERIAL INTERFACES use the “clock rate” command

![image](https://github.com/psaumur/CCNA/assets/106411237/c32af4a3-105c-451a-9641-0f7fc26e7f42)

If you change the ENCAPSULATION, it must MATCH on BOTH ENDS or the INTERFACE will go down.

![image](https://github.com/psaumur/CCNA/assets/106411237/8a448ef2-96f2-4371-bef1-520572ba5224)

R1 and R2 sharing the SAME Encapsulation Type 

![image](https://github.com/psaumur/CCNA/assets/106411237/6f934097-30fb-4605-935d-08a29e53a476)


SERIAL INTERFACES SUMMARY

- The DEFAULT encapsulation is HDLC
- You can configure PPP encapsulation with this command:
    
    <aside>
    💡 R1(config-if)# **encapsulation ppp**
    
    </aside>
    
- One side is DCE, other side is DTE
- Identify which side is DCE / DTE :
    
    <aside>
    💡 R1# **show controllers** *interface-id*
    
    </aside>
    
- You must configure the CLOCK RATE on the DCE side:
    
    <aside>
    💡 R1(config-if)# clock rate *bits-per-second*
    
    </aside>
    

---

![image](https://github.com/psaumur/CCNA/assets/106411237/bc5a756e-c65d-4585-ad3f-c0e29682c0eb)

![image](https://github.com/psaumur/CCNA/assets/106411237/232c8658-d129-49f4-9a37-76139ebe857e)

- You can configure the OSPF NETWORK TYPE on an INTERFACE with :

<aside>
💡 R1(config-if)# ip ospf network <network type>

</aside>

For example, if TWO ROUTES are directly connected with an ETHERNET link, there is no need for a DR / DBR. You can configure the POINT-TO-POINT NETWORK type in this case

NOTE: Not all NETWORK TYPES work on ALL LINK TYPES (for example, a serial link cannot use the BROADCAST NETWORK type)

![image](https://github.com/psaumur/CCNA/assets/106411237/8688e7ef-d166-4433-9f65-b918917f385f)

<aside>
💡 NON-BROADCAST NETWORK type Default Timers : Hello 30, Dead 120

</aside>

---

OSPF NEIGHBOUR / ADJACENCY REQUIREMENTS

1) AREA NUMBER MUST MATCH

2) INTERFACES must be in the SAME SUBNET

3) OSPF PROCESS must not be **SHUTDOWN**

![image](https://github.com/psaumur/CCNA/assets/106411237/80b626ac-f368-4d86-85f4-dc80e3be5259)

4) OSPF ROUTER ID must be unique

![image](https://github.com/psaumur/CCNA/assets/106411237/8f089c68-96e9-4cbf-a9c0-c93f74de4888)

5) HELLO and DEAD Timers must MATCH

6) AUTHENTICATION settings must MATCH

![image](https://github.com/psaumur/CCNA/assets/106411237/06cab926-a458-4978-b754-b2253ee74762)

*** SPECIAL REQUIREMENTS *** 

7) IP MTU settings must MATCH

- IP MTU : Maximum size of an IP Packet that can be sent from an INTERFACE
- If the settings DO NOT match, can still become OSPF Neighbors but OSPF WILL NOT operated properly

8) OSPF NETWORK TYPE must match

- will appear to be working but NEIGHBOR won’t appear in ROUTING information

---

OSPF LSA TYPES

- The OSPF LSDB is made up of LSAs
- There are 11 types of LSA but there are only 3 you should be aware of for the CCNA:
    - Type 1 (Router LSA)
    - Type 2 (Network LSA)
    - Type 5 (AS External LSA)

TYPE 1 (Router LSA)

- Every OSPF ROUTER generates this type of LSA
- It identifies the ROUTER using it’s ROUTER ID
- It also lists NETWORKS attached to the ROUTER’s OSPF-Activated INTERFACES

TYPE 2 (Network LSA)

- Generated by the DR of EACH “multi-access” NETWORK (ie: the BROADCAST network type)
- Lists the ROUTERS which are attached to the multi-access NETWORK

TYPE 5 (AS-External LSA)

- Generated by ASBRs to describe ROUTES to DESTINATIONS outside of the AS (OSPF Domain)

# 29. FIRST HOP REDUNDANCY PROTOCOLS

THE PURPOSE OF FHRPS

 
![image](https://github.com/psaumur/CCNA/assets/106411237/32c286ce-e042-4cda-9067-c232a210ec81)

What happens when the configured DEFAULT GATEWAY for network HOSTS goes down ?

What happens to the routed traffic?

How can we route our traffic to the functional GATEWAY at R2 (.253) ? 

This is what the FIRST HOP REDUNDANCY PROTOCOL is designed to fix

---

FIRST HOP REDUNDANCY PROTOCOL (FHRP)

- Computer networking protocol
- Designed to PROTECT the DEFAULT GATEWAY used on a SUBNET by allowing TWO or MORE ROUTERS to provide BACKUP for that ADDRESS
- In the event of a FAILURE of the ACTIVE ROUTER, the BACKUP ROUTER will take over the ADDRESS (usually within seconds)

---

HOW DOES FHRP WORK?

- TWO (or more) ROUTERS share a VIP (A Virtual IP ADDRESS)
- THIS VIP is used by HOSTS as the DEFAULY GATEWAY IP
- The ROUTERS communicate with each other by sending “Hello” messages
- One ROUTER becomes the ACTIVE ROUTER, the other(s) STANDBY
- When a HOST sends traffic to an ADDRESS outside of the NETWORK, it sends an ARP REQUEST (Broadcast Flood) to the VIP to find out it’s MAC ADDRESS
    - Spanning Tree prevents BROADCAST STORM due to Broadcast Flood
- The ACTIVE ROUTER sends the ARP REPLY back (it’s VIRTUAL MAC ADDRESS) to the HOST
- The HOST now sends traffic OUTSIDE of the NETWORK with:
    - Source IP (HOST IP)
    - Destination IP (External IP ADDRESS)
    - Source MAC (HOST MAC ADDRESS)
    - Destination MAC (GATEWAY VIP MAC ADDRESS)

![image](https://github.com/psaumur/CCNA/assets/106411237/2a1c5df8-d4fa-44fa-b850-a8fd6bb69388)

IF R1 goes down, R2 will switch from STANDY to ACTIVE after not receiving “Hello” messages from R1

![image](https://github.com/psaumur/CCNA/assets/106411237/5e54ee53-09bd-42a7-b89e-69892590913d)

The HOST ARP TABLE doesn’t need to change since the MAC ADDRESS of the VIP is already known and traffic flows externally via R2

R2 DOES need to update the SWITCHES with a GRATUITOUS ARP

- GRATUITOUS ARP is an ARP REPLY sent without being REQUESTED (no ARP REQUEST received)
- GRATUITOUS ARP uses BROADCAST (FFFF.FFFF.FFFF) - Normal ARP REPLY is Unicast

![image](https://github.com/psaumur/CCNA/assets/106411237/6a47dc71-544e-4e33-99cd-b6a8db90f56f)

![image](https://github.com/psaumur/CCNA/assets/106411237/6f36cdf9-d002-48d6-ae5b-6fb899431b46)

What happens is R1 comes back ONLINE again?

It becomes a STANDBY ROUTER

R2 remains the ACTIVE ROUTER

<aside>
💡 FPRPs are “non-preemptive”. The current ACTIVE ROUTER will not automatically give up its role, even if the former ACTIVE ROUTER returns.

*** You CAN change this setting to make R1 ‘preempt’ R2 and take back it’s ACTIVE role, automatically ***

</aside>

---

HSRP (HOT STANDBY ROUTER PROTOCOL)

- **Cisco proprietary**
- An ACTIVE and STANDBY ROUTER are elected
- There are TWO VERSIONS :
    - version 1
    - version 2 : *adds IPv6 support* and increases # of *groups* that can be configured

- Multicast IPv4 ADDRESSES :
    - **v1** : 224.0.0.2
    - **v2** : 224.0.0.102

- VIRTUAL MAC ADDRESSES :
    - **v1** : 0000.0c07.acXX (XX = HSRP GROUP NUMBER)
    - **v2** : 0000.0c9f.fXXX (XXX = HSRP GROUP NUMBER)

- In a situation with MULTIPLE SUBNETS / VLANS, you can configure a DIFFERENT ACTIVE ROUTER in EACH SUBNET / VLAN to LOAD BALANCE

![image](https://github.com/psaumur/CCNA/assets/106411237/a5795fa0-d57b-4037-8945-a39da7fb2d15)

---

VRRP (VIRTUAL ROUTER REDUNDANCY PROTOCOL)

- Open Standard
- A MASTER and BACKUP ROUTER are elected

- Multicast IPv4 ADDRESSES :
    - 224.0.0.18

- VIRTUAL MAC ADDRESSES :
    - 0000.5e00.01XX (XX = VRRP GROUP NUMBER)
        - for GROUP NUMBERS > 99, you need to convert the number to HEX
        - Example: 200 = “c8” in Hex so the MAC would be 0000.5e00.01c8

- In a situation with MULTIPLE SUBNETS / VLANS, you can configure a DIFFERENT MASTER ROUTER in EACH SUBNET / VLAN to LOAD BALANCE

![image](https://github.com/psaumur/CCNA/assets/106411237/4bd45dbc-fc51-4c45-818e-5274530accde)

---

GLBP (GATEWAY LOAD BALANCING PROTOCOL)

- Cisco Proprietary
- LOAD BALANCES among MULTIPLE ROUTERS within a SINGLE SUBNET
- An AVG (Active Virtual Gateway) is elected
- Up to FOUR AVFs (Active Virtual Forwarders) are assigned BY the AVG (the AVG can be an AVF, too)
- Each AVF acts as the DEFAULT GATEWAY for a portion of the HOSTS in the SUBNET

- Multicast IPv4 ADDRESSES :
    - 224.0.0.102

- VIRTUAL MAC ADDRESSES :
    - 0007.b400.XXYY (XX = GLBP GROUP NUMBER, YY = AVF NUMBER)

---

MEMORIZE THIS CHART and the differences between the FHRPs

![image](https://github.com/psaumur/CCNA/assets/106411237/a5b5ee87-4c92-4b3e-9b98-3d0c09a1732d)

---

BASIC HSRP CONFIGURATION

R1s configuration

![image](https://github.com/psaumur/CCNA/assets/106411237/028b13d4-b258-4551-96ae-068adb931356)

NOTE : group number has to match ALL ROUTERS being configured in a given SUBNET

![image](https://github.com/psaumur/CCNA/assets/106411237/d2e5eb5f-d105-4788-a869-d9e65f53eca7)

R2’s configuration

![image](https://github.com/psaumur/CCNA/assets/106411237/65b999f6-eed8-45c3-89fe-bff749f40f11)

NOTE : HSRP versions are not cross-compatible. All ROUTERS must use the same HSRP Version

Output of the “show standby” command

![image](https://github.com/psaumur/CCNA/assets/106411237/99107301-2619-4454-b104-8aed3780924d)

# 30. TCP and UDP (LAYER 4 PROTOCOLS)

BASICS OF LAYER 4

- Provides TRANSPARENT transfer of DATA between END HOSTS (Host To Host communication)

![image](https://github.com/psaumur/CCNA/assets/106411237/b0309c1e-a283-428b-9d8b-c9c1568e6a58)

- Provides (or DOESN’T provide) various SERVICES to APPLICATIONS:
    - Reliable DATA Transfer
    - Error Recovery
    - Data Sequencing
    - Flow Control
- Provides LAYER 4 ADDRESSING (PORT numbers) - NOT the physical interfaces / ports on network devices
    - IDENTIFY the APPLICATION LAYER protocol
    - Provides SESSION multiplexing

---

WHAT IS A SESSION ? 

- A SESSION is an EXCHANGE of DATA between TWO or MORE communicating DEVICES

![image](https://github.com/psaumur/CCNA/assets/106411237/2d8c6c74-24e5-4574-b454-bc694f056bec)

The FOLLOWING ranges have been designated by IANA (Internet Assigned Numbers Authority) 

- **Well-Known** Port Numbers : 0 - 1023
- **Registered** Port Numbers : 1024 - 49151
- **Ephemeral** / Private / Dynamic port numbers : 49152 - 65535

![image](https://github.com/psaumur/CCNA/assets/106411237/02d56940-33b6-40a8-8431-0a39c19bc66a)

---

TCP (TRANSMISSION CONTROL PROTOCOL)

- A CONNECTION-ORIENTED protocol
    - Before actually SENDING DATA to the DESTINATION HOST, the TWO HOSTS communicate to establish a CONNECTION. Once the CONNECTION is established, DATA exchange begins.

![image](https://github.com/psaumur/CCNA/assets/106411237/9fcb7294-da61-4fff-b483-c1da6a8d7b48)

![image](https://github.com/psaumur/CCNA/assets/106411237/1f5b0753-b625-463b-9d6f-79bf5b2454dc)

Establishing connections

![image](https://github.com/psaumur/CCNA/assets/106411237/877a8e35-2e2d-4cf4-af65-1a1834308ba9)

Terminating connections

![image](https://github.com/psaumur/CCNA/assets/106411237/3a0a9cff-8bc4-4c1f-a9b0-941807cf6f40)

- TCP provides RELIABLE communication
    - The DESTINATION HOST must acknowledge that it RECEIVED each TCP SEGMENT (Layer 4 PDU)
    - If a SEGMENT isn’t ACKNOWLEDGED, it is sent again
    

![image](https://github.com/psaumur/CCNA/assets/106411237/d8349049-7a5a-40a3-95fa-7ad86ec1049d)

- TCP provides SEQUENCING
    - SEQUENCE numbers in the TCP HEADER allow DESTINATION HOSTS to put SEGMENTS in the correct ORDER even if they arrive out of ORDER

![image](https://github.com/psaumur/CCNA/assets/106411237/a1df1c41-df4f-4211-ac56-144280a2d3bf)

- TCP provides FLOW CONTROL
    - The DESTINATION HOST can tell the SOURCE HOST to increase / decrease the RATE that DATA is sent

![image](https://github.com/psaumur/CCNA/assets/106411237/f5f3f467-5b1f-4a30-9ef7-8a5c0de65139)

![image](https://github.com/psaumur/CCNA/assets/106411237/fafc82c7-21a2-46cf-b82b-702b2d8c1d52)

---

UDP (USER DATAGRAM PROTOCOL)

![image](https://github.com/psaumur/CCNA/assets/106411237/773a7e94-50b1-4179-b2e6-0d45ec5c1b3d)

- UDP is NOT a CONNECTION-ORIENTED PROTOCOL
    - The SENDING HOST does NOT establish a CONNECTION with the DESTINATION HOST before sending DATA. The DATA is simply SENT

- UDP DOES NOT provide reliable COMMUNICATION
    - When UDP is used, ACKNOWLEDGEMENTS are NOT SENT for received SEGMENTS
    - If a SEGMENT is LOST, UDP has no mechanism to re-TRASMIT it
    - SEGMENTS are sent “best-effort”
    
- UDP DOES NOT provide SEQUENCING
    - There is NO SEQUENCE NUMBER FIELD in the UDP header
    - If SEGMENTS arrive out of order, UDP has no MECHANISM to put them back in ORDER
    
- UDP DOES NOT provide FLOW CONTROL
    - UDP has NO MECHANISM like TCP’s WINDOW SIZE to control the flow of DATA
    
- UDP DOES provide ERROR CHECKING (via CHECKSUM)

---

COMPARING TCP AND UDP

Number of Fields in their Headers

![image](https://github.com/psaumur/CCNA/assets/106411237/90fb3d62-5011-4970-9cf6-167cccfe3449)

- TCP provides MORE FEATURES than UDP but at a COST of ADDITIONAL OVERHEAD
- For applications that require RELIABLE communications (for example, downloading a file), TCP is PREFERRED
- For applications, like real-time voice and video, UDP is preferred
- There are SOME applications that use UDP, but provide RELIABILITY, etc. within the APPLICATION itself.
- Some applications use BOTH TCP and UDP, depending on the situation.

![image](https://github.com/psaumur/CCNA/assets/106411237/fcbef599-9277-4b06-8d59-2349ca70817a)

IMPORTANT PORT NUMBERS

![image](https://github.com/psaumur/CCNA/assets/106411237/9e1f0422-d027-4a06-a359-d47c5c39dba1)

# 31. IPv6 : PART 1

HEXIDECIMAL (Review)

![image](https://github.com/psaumur/CCNA/assets/106411237/df3e0c7f-5325-4c4c-9d88-197b588cdfe4)

![image](https://github.com/psaumur/CCNA/assets/106411237/a23caee6-492b-4226-ba9f-7b3e44578fd4)

![image](https://github.com/psaumur/CCNA/assets/106411237/1a7e0af8-4f19-483d-b75c-27fa452ce8e9)

What about the reverse (Hex to Binary) ??? 

![image](https://github.com/psaumur/CCNA/assets/106411237/ceced09e-175f-452d-87e8-5b10af7621a1)

---

WHY IPv6?

- The **MAIN REASON** is that there are simply not enough IPv4 addresses available
- There are 2^32 IPv4 Addresses available (4,294,967,296)
- When IPv4 was being designed 30 years ago, the creators had NO idea the Internet would be as large as today
- VLSM, Private IPv4 ADDRESSES, and NAT have been used to conserve the use of IPv4 ADDRESS SPACE.
    - These are short-term solutions, however.
- The LONG -TERM solution is IPv6

- IPv4 ADDRESS assignments are controlled by IANA (Internet Assigned Number Authority)
- IANA distributes IPv4 ADDRESS space to various RIRs (Regional Internet Registries), which then assign them to companies that need them.

![image](https://github.com/psaumur/CCNA/assets/106411237/98fdf256-dbbf-4884-825a-6124251da6a7)

- On September 24th, 2015, ARIN declared exhaustion of the ARIN IPv4 address pool
- On August 21st, 2020, LACNIC announced that it had made its final IPv4 allocation

---

BASICS OF IPv6

- An IPv6 ADDRESS is **128 bits (8 bytes)**

![image](https://github.com/psaumur/CCNA/assets/106411237/3e6fe314-c87f-4116-bf37-7f3cfd8e17b4)

- An IPv6 ADDRESS uses the / prefix number

SHORTENING (Abbreviating) IPv6 ADDRESSES

![image](https://github.com/psaumur/CCNA/assets/106411237/7796f62c-5daa-4e3c-a029-2c42e8abfc6c)

![image](https://github.com/psaumur/CCNA/assets/106411237/ee734193-9708-44a8-8702-c0d9d07afaad)

![image](https://github.com/psaumur/CCNA/assets/106411237/a19192b2-fcd9-4280-95c4-281ef08ffa5e)

![image](https://github.com/psaumur/CCNA/assets/106411237/07c413b6-1577-47c3-963c-4ccca8e20820)

![image](https://github.com/psaumur/CCNA/assets/106411237/ea5f5e40-1b4f-4fd8-942c-c17ca2535e35)

EXPANDING (Abbreviating) IPv6 ADDRESSES

![image](https://github.com/psaumur/CCNA/assets/106411237/934a089e-6ec1-4297-b0da-154b8240af35)

FINDING the IPv6 PREFIX (GLOBAL UNICAST ADDRESSES)

- Typically, an Enterprise requesting IPv6 ADDRESSES from their ISP will receive a /48 BLOCK
- Typically, IPv6 SUBNETS use a /64 PREFIX LENGTH
- That means an Enterprise has 16 bits to use to make SUBNETS
- The remaining 64 bits can be used for HOSTS

![image](https://github.com/psaumur/CCNA/assets/106411237/12448711-2636-4133-bed9-d655bedbd418)

![image](https://github.com/psaumur/CCNA/assets/106411237/fa872c5a-4d39-4519-9248-f4f552539bb8)

(Each digit is 4 bits / each 4 digit block is 16 bits)

**REMEMBER** : You can only remove the LEADING ZEROS !!!

2001 : 0DB8 : 8B00 : 0001 : FB89 : 017B : 0020 : 0011  /93

Because 93 lands in the middle of a 4 bit number, we need to convert the last digit to binary and borrow a “bit” from the first binary digit.

:: 017 [B] :: B = 0d11 = 0b1011 = 0b1000 (the first digit is borrowed, the remainder become 0)

![image](https://github.com/psaumur/CCNA/assets/106411237/1703e18d-da7a-4ee9-850e-d4e4a59ec72a)

![image](https://github.com/psaumur/CCNA/assets/106411237/c7e6fcec-ec8c-40df-86b6-72486e2a3165)

---

CONFIGURING IPv6 ADDRESSES

![image](https://github.com/psaumur/CCNA/assets/106411237/7ee88c71-617f-4bfc-8220-a4ef5bbe89e3)

This allows the ROUTER to perform IPv6 ROUTING

<aside>
💡 R1(config) #ipv6 unicast-routing

</aside>

Configuring an INTERFACE with an IPv6 Address

<aside>
💡 R1(config) #int g0/0
R1(config-if) #ipv6 address 2001:db8:0:0::1/64
R1(config) #no shutdown

</aside>

You can also type out the full address (if necessary)

![image](https://github.com/psaumur/CCNA/assets/106411237/c83977d3-678f-4922-9be2-f52c6a679d64)

NOTE ABBREVIATED IPv6 ADDRESSES SHOWN

LINK-LOCAL ADDRESSES are automatically added when creating an IPv6 INTERFACE (Covered in IPv6 - PART 2 Lecture)

# 32. IPv6 : PART 2

IPv6 ADDRESS CONFIGURATION (EUI-64)

- EUI stands for Extended Unique Identifier
- (Modified) EUI-64 is a method of converting a MAC address (48-bits) into a 64-bit INTERFACE identifier
- This INTERFACE identifier can then become the “HOST portion” of a /64 IPv6 ADDRESS

![image](https://github.com/psaumur/CCNA/assets/106411237/bee8f7bf-3877-4307-9ca7-863af19aae6c)

EUI-64 PRACTICE:
```
782B CBAC 0867 >>> 782B CB  ||  AC 0867

782B CBFF  FEAC 0867 

8 is the 7th bit so 1000 inverted becomes 1010 = A in hex

so the EUI-64 Interface Identifier is :  7A2B CBFF FEAC 0867
```

![image](https://github.com/psaumur/CCNA/assets/106411237/d4e90146-8c71-4c6c-b5aa-a9077bde2caf)

---
CONFIGURING IPv6 ADDRESSES with EUI-64

![image](https://github.com/psaumur/CCNA/assets/106411237/e6c6da0b-def4-4764-a0a1-3f64855f319f)

![image](https://github.com/psaumur/CCNA/assets/106411237/bff1b2bc-9944-451a-972a-f8b3bd5f76ea)

![image](https://github.com/psaumur/CCNA/assets/106411237/4c69d97a-a611-4a94-9e11-9016ec456819)

NOTE the “2001:DB8…” Address has “E” changed to “c”. This is the 7th bit getting flipped (1110 to 1100 = 12 = hex ‘C’)

---

WHY INVERT THE 7th BIT ? 

- MAC addresses can be divided into TWO TYPES:
    - UAA (Universally Administered Address)
        - Uniquely assigned to the device of the manufacturer
    - LAA (Locally Administered Address)
        - Manually assigned by an Admin (with the mac-address command on the INTERFACE) or protocol. Doesn’t have to be globally unique.
- You can INDENTIFY a UAA or LAA by the 7th bit of the MAC ADDRESS, called the U/L bit (Universal/Local bit)
    - U/L bit set to 0 = UAA
    - U/L bit set to 1 = LAA
- In the context of IPv6 addresses/EUI-64, the meaning of the U/L bit is reversed:
    - U/L bit set to 0 = The MAC address the EUI-64 INTERFACE ID was made from was an LAA
    - U/L bit set to 1 = The MAC address the EUI-64 INTERFACE ID was made from was a UAA

---

IPv6 ADDRESS TYPES

1) GLOBAL UNICAST ADDRESSES

- **Global Unicast** IPv6 ADDRESSES are PUBLIC ADDRESSES which can be used over the INTERNET
- Must REGISTER to use them.
- They are PUBLIC ADDRESSES so need to be GLOBALLY UNIQUE

💡 Originally defined as the 2000 :: /3 block
(2000:: to 3FFF : FFFF : FFFF : FFFF : FFFF : FFFF : FFFF : FFFF)

- NOW defined as ALL ADDRESSES which are not RESERVED for other purposes

Remember THESE THREE PARTS of a GLOBAL UNICAST ADDRESS

![image](https://github.com/psaumur/CCNA/assets/106411237/c5552f0e-eca2-4069-a656-611b5c196402)

---

2) UNIQUE LOCAL ADDRESSES 

- **Unique Local** IPv6 ADDRESSES are PRIVATE ADDRESSES which cannot be used over the internet
- You do NOT need to REGISTER to use them
- Can be used FREELY within INTERNAL NETWORKS
- Do NOT need to be GLOBALLY UNIQUE (*)
- CANNOT be ROUTED over the INTERNET

<aside>
💡 Uses the ADDRESS block FC00 ::/7
(FC00:: to FDFF : FFFF : FFFF : FFFF : FFFF : FFFF : FFFF : FFFF)

</aside>

- A later UPDATE required the 8th bit to be set to 1 so the FIRST TWO DIGITS must be FD

(*) The GLOBAL ID should be UNIQUE so that ADDRESSES don’t overlap when companies MERGE

![image](https://github.com/psaumur/CCNA/assets/106411237/6e6f8af9-ee53-4e0d-90ec-9e137b10c851)

---

3) LINK-LOCAL ADDRESSES

- **Link-Local** IPv6 ADDRESSES are AUTOMATICALLY generated on IPv6-enabled INTERFACES
- Use command `R1(config-if)# ipv6 enable` on an interface to enable IPv6 on an INTERFACE

<aside>
💡 Uses the ADDRESS block FE80::/10
(FE80:: to FEBF : FFFF : FFFF : FFFF : FFFF : FFFF : FFFF : FFFF)

</aside>

- The STANDARD states that the 54-bits AFTER FE80/10 should be ALL 0’s so you won’t see Link-Local ADDRESSES beginning with FE9, FEA, or FEB - ONLY FE8(!)
- The INTERFACE ID is generated using EUI-64 rules
- Link-Local means that these addresses are used for communication within a single link (SUBNET)
    - ROUTER will not route PACKETS with a Link-Local DESTINATION IPv6 ADDRESS
- Common uses of Link-Local Addresses:
    - Routing Protocol Peerings (OSPFv3 uses Link-Local Addresses for Neighbour Adjacencies)
    - NEXT-HOP ADDRESS for STATIC ROUTES
    - Neighbor Discovery Protocol (NDP, IPv6’s replacement for ARP) uses Link-Local ADDRESSES to function
    
    Network using Link-Local Addresses for “next-hop” routing
    
![image](https://github.com/psaumur/CCNA/assets/106411237/7d74c4fb-ef52-4436-8285-77ab571f2964)
    

---

4) MULTICAST ADDRESSES

- **Unicast Addresses** are one-to-one
    - ONE SOURCE to ONE DESTINATION
- ***Broadcast*** Addresses are one-to-all
    - ONE SOURCE to ALL DESTINATIONS (within the subnet)
- **Multicast** Addresses are one-to-many
    - ONE SOURCE to MULTIPLE DESTINATIONS (that have joined the specific ***multicast*** group)

<aside>
💡 IPv6 uses range FF00::/8 for multicast
(FF00:: to FFFF : FFFF : FFFF : FFFF : FFFF : FFFF : FFFF : FFFF)

</aside>

- **IPv6 doesn’t use Broadcast** (there IS NO “Broadcast Address” in IPv6!)

YOU MUST KNOW THE MULTICAST ADDRESS FOR EACH ROUTER TYPE

NOTE that the IPv6 and IPv4 Addresses share the same last digit

![image](https://github.com/psaumur/CCNA/assets/106411237/e5efcdd7-5d7d-4020-a179-07ba267bf5ab)

MULTICAST ADDRESS SCOPES

- IPv6 defines multiple MULTICAST ‘scopes’ which indicate how far the PACKET should be forwarded
- The ADDRESS in the previous slide all use the ‘link-local’ scope (FF02), which stays in the LOCAL SUBNET

**IPv6 Multicast Scope Types:**

- **Interface-Local (FF01)**
    - The PACKET doesn’t leave the LOCAL device
    - Can be used to SEND traffic to a SERVICE within the LOCAL device
    
- **Link-Local (FF02)**
    - The PACKET remains in the LOCAL SUBNET
    - ROUTERS will not route the PACKET between SUBNETS

- **Site-Local  (FF05)**
    - The PACKET can be forwarded by ROUTERS
    - Should be limited to a SINGLE PHYSICAL LOCATION (not forwarded over a WAN)
- **Organization-Local (FF08)**
    - Wider in scope than Site-Local (an entire company / ORGANIZATION)
- **Global (FF0E)**
    - No boundaries
    - Possible to be ROUTED over the INTERNET

![image](https://github.com/psaumur/CCNA/assets/106411237/5d5f2d6e-3e21-4ab7-bf8e-dec5d12b6eed)

5) ANYCAST ADDRESS

- **ANYCAST is a NEW feature of IPv6**
- ANYCAST is ‘one-to-one-of-many’
- Multiple ROUTERS are configured with the SAME IPv6 ADDRESS
    - They use a ROUTING PROTOCOL to advertise the address
    - When HOSTS sends PACKETS to that DESTINATION ADDRESS, ROUTERS will forward it to the NEAREST ROUTER configured with THAT IP ADDRESS (based on ROUTING METRIC)
- There is NO SPECIFIC ADDRESS range for ANYCAST ADDRESSES.
    - Use a regular UNICAST (Global Unicast, Unique Local) and specify THAT as an ANYCAST ADDRESS
    - `R1(config-if)# ipv6 address 2000:db8:1:1::99/128 anycast`

![image](https://github.com/psaumur/CCNA/assets/106411237/71729af9-6c02-49bd-b290-af7f5009bd6e)

6) OTHER IPv6 ADDRESSES

- The :: Address = The *unspecified* IPv6 ADDRESS
    - Can be used when a DEVICE doesn’t yet know its IPv6 ADDRESS
    - IPv6 DEFAULT ROUTES are configured to ::/0
    - IPv4 equivalent: 0.0.0.0
- The ::1 Address = The Loopback Address
    - Used to test the PROTOCOL STACK on the LOCAL DEVICE
    - Messages sent to THIS ADDRESS are processed within the LOCAL DEVICE but not SENT to other DEVICES
    - IPv4 equivalent : 127.0.0.0 /8  address range

# 33. IPv6 : PART 3

CORRECTION TO PRIOR LECTURES:

RFC Requirements for IPv6 Address Representation

- Leading 0s MUST be removed
    - This - 2001 : 0db8 : 0000 : 0001 : 0f2a : 4fff : fea3 : 00b1
    - Becomes - 2001 : db8 : 0 : 1 : f2a : 4fff : fea3 : b1
- :: MUST be used to shorten the longest string of all-0 quartets
    - If there is only ONE all-0 quartet, don’t use ‘::’
    - This - 2001 : 0000 : 0000 : 0000 : 0f2a : 0000 : 0000 : 00b1
    - Becomes - 2001 :: f2a : 0 : 0 : b1
- If there are two equal-length choices for the :: , use :: to the shorten the one on the LEFT
    - This - 2001 : 0db8 : 0000 : 0000 : 0f2a : 0000 : 0000 : 00b1
    - Becomes - 2001 : db8 :: f2a : 0 : 0 : b1
- Hexadecimal characters ‘a’, ‘b’, ‘c’, ‘d’, ‘e’, and ‘f’ MUST be written using lower-case, NOT upper case A B C D E F

---

IPv6 HEADER

![image](https://github.com/psaumur/CCNA/assets/106411237/5bba7262-60aa-4348-9b7a-55dc354f4ed3)

Length is ALWAYS 40 bytes (Fixed Header)

Version (4 bits)

- Indicates version of IP used
- Fixed value of ‘6’ (0b0110) to indicate IPv6

Traffic Class (8 bits)

- Used for QoS (Quality of Service) to indicate high-priority traffic
- Example: IP phone traffic, live video calls, etc.

Flow Label (20 bits)

- Identifies specific traffic “flows” (communication between Source and Destination)

Payload Length (16 bits)

- Indicates the LENGTH of the PAYLOAD (the encapsulation LAYER 4 SEGMENT) **in bytes**
- The length of the IPv6 header, itself, isn’t included, because it’s ALWAYS 40 bytes

Next Header (8 bits)

- Indicates the TYPE of the ‘next header’ (header of the encapsulated SEGMENT)
    - Example: TCP or UDP
- Same function as the IPv4 header’s ‘Protocol’ field

Hop Limit (8 bits)

- Value in this field decrements by 1 every time a ROUTER forwards it. If it reaches ‘0’, the PACKET is discarded (similar to IPv4 TTL field )

Source Address (128 bits)

- Packet’s SOURCE address

Destination Address (128 bits)

- Packet’s DESTINATION address

---

SOLICITED-NODE MULTICAST ADDRESS

- An IPv6 SOLICITED-NODE Multicast Address is calculated from a UNICAST ADDRESS

How to generate a SOLICITED-NODE Multicast Address

![image](https://github.com/psaumur/CCNA/assets/106411237/eef6815b-405b-485d-884d-ff08bbbf16d3)

Note the automatically joined group addresses for this IPv6 Interface

![image](https://github.com/psaumur/CCNA/assets/106411237/4f981645-7488-4f0c-8ec5-d7c1b878acba)

---

NEIGHBOR DISCOVERY PROTOCOL (NDP)

- NEIGHBOR DISCOVERY PROTOCOL (NDP) is a PROTOCOL used with IPv6
- It has various functions and one of those functions is to replace ARP, which is no longer used in IPv6
- The ARP-like function of NDP uses ICMPv6 and SOLICITED-MODE Multicast Addresses to learn the MAC ADDRESS of other HOSTS (ARP in IPv4 uses Broadcast Messages)

- TWO MESSAGES types are used:
    - 1) NEIGHBOR SOLICITATION (NS)
        - ICMPv6 Type 135
    
    - 2) NEIGHBOR ADVERTISEMENT (NA)
        - ICMPv6 Type 136

![image](https://github.com/psaumur/CCNA/assets/106411237/88b9dde5-bc94-49ce-ba4a-b38c47f4670d)

![image](https://github.com/psaumur/CCNA/assets/106411237/cc9010cb-eb67-4fcb-8c6a-7a0aa11c7057)

IPv6 NEIGHBOR TABLE

![image](https://github.com/psaumur/CCNA/assets/106411237/085bb9df-8015-4c2f-bfc8-2d6336436fe2)

- Another function of NDP allows HOSTS to automatically discover ROUTERS on the LOCAL NETWORK

- TWO MESSAGES are used for this process:
  
    - ROUTER SOLICITATION (RS)
        - ICMPv6 Type 133
        - Sent to Multicast Address `FF02::2` (All Routers)
        - Asks ALL ROUTERS on the Local Link to identify themselves
        - Sent when an INTERFACE is enabled / HOST is connected to the NETWORK
        
    - ROUTER ADVERTISEMENT (RA)
        - ICMPv6 Type 134
        - Sent to Multicast Address `FF02::1` (All Nodes)
        - The ROUTER announces its presence, as well as other information about the link
        - These messages are sent in response to RS messages
        - They are also sent periodically, even if the ROUTER hasn’t received an RS
        
    
![image](https://github.com/psaumur/CCNA/assets/106411237/f7861fda-e893-4fd1-b5c3-5deed57de2f0)
    

---

SLAAC

- Stands for **STATELESS ADDRESS AUTO-CONFIGURATION**
- HOSTS use the RS / RA messages to learn the IPv6 Prefix of the LOCAL LINK (ie: 2000:db8:: /64) and then automatically generate an IPv6 Address
- Using the `ipv6 address prefix / prefix-length eui-64` command, you need to manually enter the prefix
- Using the `ipv6 address autoconfig` command, you DON’T need to enter the prefix. The device uses NDP to learn the prefix used on the local link
- The device will use EUI-64 to generate the INTERFACE ID or it will be randomly generated (depending on the device / maker)

![image](https://github.com/psaumur/CCNA/assets/106411237/e1cc9b26-1a81-48fb-8538-77f97d456eff)

---

DUPLICATE ADDRESS DETECTION (DAD)

- One final point about NDP!
- Duplicate Address Detection (DAD) allows HOSTS to check if other devices on the Local Link are using the same IPv6 Address
- Any time an IPv6-enabled interface initializes (`no shutdown` command) or an IPv6 ADDRESS is configured on an INTERFACE (by any method: manual, SLAAC, etc.) it performs DAD
- DAD uses TWO MESSAGES you learned earlier : NS and NA
- The HOST will send an NS to its own IPv6 ADDRESS.
    - If it doesn’t get a reply, it KNOWS the ADDRESS is unique
    - If it DOES get a reply, it means ANOTHER HOST on the NETWORK is already using that ADDRESS

---

IPv6 STATIC ROUTING

- IPv6 ROUTING works the same as IPv4 ROUTING
- However, the TWO processes are separate on the ROUTER, and the TWO routing tables are separate, as well.
- IPv4 ROUTING is enabled BY DEFAULT
- IPv6 ROUTING is disabled BY DEFAULT
    - MUST BE ENABLED with the `ipv6 unicast-routing` command
- If IPv6 ROUTING is disabled, the ROUTER will be able to SEND and RECEIVE IPv6 traffic, but will not *route* IPv6 traffic (ie: will NOT FORWARD it between NETWORKS)

![image](https://github.com/psaumur/CCNA/assets/106411237/e082920f-3a76-438d-b43d-8eac968dcd55)

![image](https://github.com/psaumur/CCNA/assets/106411237/90acb6ca-2703-47d1-907f-1878490c78f6)

- A CONNECTED NETWORK ROUTE is automatically added for EACH CONNECTED NETWORK
- A LOCAL HOST ROUTE is automatically added for each ADDRESS configured on the ROUTER
- Routes for Link-Local ADDRESSES are not added to the ROUTING TABLE

![image](https://github.com/psaumur/CCNA/assets/106411237/d01849d3-c031-45a0-8e31-efd9dba61df6)

Everything is configured similar to normal static routes in IPv4

[AD] = Administrative Distance. You NEED this value in order to configure a STATIC ROUTE

DIRECTLY ATTACHED Static Route:

- Only the EXIT INTERFACE is specified
- `ipv6 route destination / prefix-length exit-interface`
- Example : `~~R1(config)# ipv6 route 2001:db8:0:3:: /64 g0/0~~`

<aside>
💡 In IPv6, you CANNOT use DIRECTLY ATTACHED Static Routes if the INTERFACE is an ETHERNET INTERFACE

</aside>

RECURSIVE Static Route:

- Only the Next-Hop is specified
- `ipv6 route destination / prefix-length next-hop`
- Example: `R1(config)# ipv6 route 2001:db8:0:3::/64 2001:db8:0:12::2`

FULLY SPECIFIED Static Route:

- Both the Exit Interface and Next Hop are specified
- `ipv6 route destination / prefix-length exit-interface next-hop`
- Example: `R1(config)# ipv6 route 2001:db8:0:3::/64 g0/0 2001:db8:0:12::2`

---

(NOTE THAT THESE ROUTES ARE ALL RECURSIVE : They specify the Next-Hop)

NETWORK ROUTE:

`R1(config)# ipv6 route 2001:db8:0::/64 2001:db8:0:12::2`

This is a route to R3/PC2 NETWORK via R2’s G0/0 INTERFACE

(We did this in Day 32’s Lab)

HOST ROUTE:

`R2(config)# ipv6 route 2001:db8:0:1::100/128 2001:db8:0:12::1`

`R2(config)# ipv6 route 2001:db8:0:3::100/128 2001:db8:0:23::2`

This is a route from R2 to PC1 and PC2 using the “next hop” ADDRESSES of R1 and R3 G0/0 INTERFACES

Note the /128 prefix. This is how SPECIFIC IPv6 ADDRESSES are written

DEFAULT ROUTE:

`R3(config)# ipv6 route ::/0 2001:db8:0:23::1`

::/0 is the IPv6 equivalent of 0.0.0.0/0 in IPv4

FLOATING STATIC ROUTES:

- Require you to increase the [AD] number HIGHER than the currently used NETWORK IGP AD value

LINK-LOCAL NEXT HOPS:

![image](https://github.com/psaumur/CCNA/assets/106411237/52cf09e2-2b37-4319-a2b9-15213524530c)

You HAVE to specify the INTERFACE name when using Link-Local Next-Hops

This is EXACTLY like a FULLY-SPECIFIED STATIC ROUTE

# 34. STANDARD ACCESS CONTROL LISTS (ACL)

WHAT ARE ACLs

- ACLs (Access Control Lists) have multiple uses
- In DAY 34 and DAY 35, we will focus on ACL’s from a security perspective
- ACLs function as a “packet filter” - instructing the ROUTER to ALLOW or DENY specific traffic
- ACLs can filter traffic based on:
    - SOURCE / DESTINATION IP ADDRESSES
    - SOURCE / DESTINATION LAYER 4 PORTS
    - etc.

---

HOW ACLs WORK

![image](https://github.com/psaumur/CCNA/assets/106411237/92d663ec-33a8-4ba4-b0a7-5d3942a9b67e)

<aside>
💡 REQUIREMENTS:

- Hosts in 192.168.1.0/24 should have ACCESS to the 10.0.1.0/24 NETWORK
- Hosts in 192.168.2.0/24 should not have ACCESS to the 10.0.10/24 NETWORK
</aside>

ACLs are configured GLOBALLY on the ROUTER (Global Config Mode)

- They are an ordered sequence of ACEs (Access Control Entries)

![image](https://github.com/psaumur/CCNA/assets/106411237/2eb0c042-21d0-4a40-ade3-9715bd2b3bcb)

- Configuring an ACL in Global Config Mode will not make the ACL take effect
- The ACL must be applied to an interface
    - ACLs are applied either INBOUND or OUTBOUND
- ACLs are made up of one or more ACEs
- When a ROUTER checks a PACKET against the ACL, it processes the ACEs in order, from top to bottom
- If the PACKET matches one of the ACEs in the ACL, the ROUTER takes the action and stops processing the ACL. All entries below the matching entry will be ignored

![image](https://github.com/psaumur/CCNA/assets/106411237/a4a86a8e-f73c-476b-b0e5-15bfb4f4748d)

![image](https://github.com/psaumur/CCNA/assets/106411237/6e4148e0-e908-4a44-9f23-358c9d7ade11)

---

IMPLICIT DENY

- What will happen if a PACKET doesn’t match any of the entries in an ACL ?
- There is an INPLICIT DENY at the end of ALL ACL’s
- The IMPLICIT DENY tells the ROUTER to DENY ALL TRAFFIC that doesn’t match ANY of the configured entries in the ACL

---

ACL TYPES

![image](https://github.com/psaumur/CCNA/assets/106411237/4856845e-80b2-45dc-b30c-cc3b170db69c)

---

STANDARD NUMBERED ACLs

- Match traffic based only on the SOURCE IP ADDRESS of the PACKET
- Numbered ACLs are identified with a number (ie: ACL 1, ACL 2, etc.)
- Different TYPES of ACLs have a different range of numbers that can be used
    
    <aside>
    💡 STANDARD ACLs can use 1-99 and 1300-1999
    
    </aside>
    

- The basic command to configure a STANDARD NUMBERED ACL
    - `R1(config)# access-list *number* {deny | permit} *ip wildcard-mask*`
    
    This is an example of denying a SPECIFIC host’s traffic
    
    REMEMBER : 0.0.0.0 wildcard is the same as 255.255.255.255 or a /32 host
    
    - Example : `R1(config)# access-list 1 deny 1.1.1.1 0.0.0.0`
    - Example : `R1(config)# access-list 1 deny 1.1.1.1`(identical to the above)
    - Example : `R1(config)# access-list 1 deny host 1.1.1.1`
    
    If you want to permit ANY traffic from ANY source
    
    - Example : `R1(config)# access-list 1 permit any`
    - Example : `R1(config)# access-list 1 permit 0.0.0.0 255.255.255.255`
    
    If you want to make a description for a specific ACL
    
    - Example : `R1(config)# access-list 1 remark ## BLOCK BOB FROM ACCOUNTING ##`

![image](https://github.com/psaumur/CCNA/assets/106411237/3e20e40c-6755-4638-9ef3-15fa747f93b6)

Order is important. Lower Numbers are processed FIRST

---
TO APPLY AN ACL TO AN INTERFACE

`R1(config-if)# ip access-group *number* {in | out}`

![image](https://github.com/psaumur/CCNA/assets/106411237/eed38afa-f067-4153-80bb-b07c52a21e53)

WHY WAS THIS RULE PLACED ON G0/2 OUT ? 

<aside>
💡 STANDARD ACLs should be applied as CLOSE to the DESTINATION as possible!

</aside>

---

STANDARD NAMED ACLs

- Standard ACLs match traffic based only on the SOURCE IP ADDRESS of the PACKET
- NAMED ACLs are identified with a NAME (ie: ‘BLOCK_BOB’)
- STANDARD NAMED ACLs are configured by entering ‘standard named ACL config mode’ then configuring EACH entry within that config mode
    - `R1(config)# ip access-list standard *acl-name*`
    - `R1(config-std-nacl)# [*entry-number*] {deny | permit} *ip wildcard-mask*`

![image](https://github.com/psaumur/CCNA/assets/106411237/94e9b58d-07f6-4ad6-9c92-b00c01ce311d)

![image](https://github.com/psaumur/CCNA/assets/106411237/a8a10f5f-8e5c-4e19-981f-862bf94b2788)

![image](https://github.com/psaumur/CCNA/assets/106411237/3b641f99-4c99-4d5f-a32b-1a626d1a02b4)

![image](https://github.com/psaumur/CCNA/assets/106411237/17a7d767-1052-4bc0-8a04-7278f16caeb6)

Here are the configurations for the above:

![image](https://github.com/psaumur/CCNA/assets/106411237/bbdcff70-1fd4-46a4-a4c2-5d5485fe5695)

Note, however, how the order is when viewing the ACLs 

![image](https://github.com/psaumur/CCNA/assets/106411237/74ad9dd4-d56f-4845-83b1-44366b4b94f6)

WHY THE REORDERING?

![image](https://github.com/psaumur/CCNA/assets/106411237/e5ed273d-1c24-4b78-884f-712e1cf6922a)

CISCOs PACKET TRACER does not reorder these, however.

# 35. EXTENDED ACCESS CONTROL LISTS (EACL)

ANOTHER WAY TO CONFIGURE NUMBERED ACLs

- In DAY 34, you learned that numbered ACLs are configured in Global Config mode:

![image](https://github.com/psaumur/CCNA/assets/106411237/d5bbb9d7-5499-43e0-9ac8-b173e5bb5c50)

- You learned that named ACLs are configured with subcommands in a separate config mode:

![image](https://github.com/psaumur/CCNA/assets/106411237/73104e31-0630-4b2a-a328-29adc5ceb418)

- However, in modern IOS you can also configure numbered ACLs in the exact same way as named ACLs:

![image](https://github.com/psaumur/CCNA/assets/106411237/724638f3-1044-4476-96de-cda39fb51315)

![image](https://github.com/psaumur/CCNA/assets/106411237/a72df84e-262b-467c-a87e-b70699033076)

---

ADVANTAGES OF NAMED ACL CONFIG MODE

- You can easily DELETE individual entries in the ACL with NO *entry-number*
- You can easily DELETE individual entries in the ACL with NO *sequence-number*

![image](https://github.com/psaumur/CCNA/assets/106411237/f7f85684-6300-495d-bde9-1e1ffcead85e)

This doesn’t work with NUMBERED access lists

![image](https://github.com/psaumur/CCNA/assets/106411237/8e27f6f1-794b-45be-ac67-20b3f563f551)

- You can insert NEW entries in-between other entries by specifying the SEQUENCE NUMBER

![image](https://github.com/psaumur/CCNA/assets/106411237/41fb1df8-b368-4349-b33a-ba0f8c768435)

---

RESEQUENCING ACLs

- There is a *resequencing* function that helps edit ACLs
- The command is  `R1(config)#ip access-list resequence *acl-id starting-seq-num increment*`

![image](https://github.com/psaumur/CCNA/assets/106411237/1c5e3f13-900a-4be4-99ba-db86b0128f57)

---

EXTENDED NUMBERS AND NAMED ACLs

- EXTENDED ACLs function mostly the same as STANDARD ACLs
- They can be NUMBERED or NAMED, just like STANDARD ACLs
    - NUMBERED ACLs use the following ranges: **100 - 199, 2000 - 2699**
- Processed from TOP to BOTTOM, just like STANDARD ACLs
- However, they can match traffic based on MORE PARAMETERS, so they are more PRECISE (and more complex) than STANDARD ACLs
- We will focus on matching based on these main parameters:
    - **LAYER 4 protocol / port**
    - **Source Address**
    - D**estination Address**

---

EXTENDED NUMBERED ACL

<aside>
💡 `R1(config)# access-list *number* [permit | deny] *protocol src-ip dest-ip*`

</aside>

EXTENDED NAMED ACL

<aside>
💡 `R1(config)# ip access-list extended {name | number}`

</aside>

<aside>
💡 `R1(config-ext-nacl)# {seq-num} {permit | deny} *protocol src-ip dest-ip*`

</aside>

---

MATCHING THE PROTOCOL

![image](https://github.com/psaumur/CCNA/assets/106411237/f6337620-5eb1-4ddc-837c-ae242a718f29)

IP Protocol Number is the number used in the IPv4 Header Protocol field

Examples: (1) ICMP, (6) TCP, (17) UDP, (88) EIGRP, (89) OSPF

MATCHING THE SOURCE / DESTINATION IP ADDRESS

![image](https://github.com/psaumur/CCNA/assets/106411237/bbb38418-3276-485b-ba6b-5c4c7097d56f)

This command:

<aside>
💡 `R1(config-ext-nacl)#deny tcp any 10.0.0.0 0.0.0.255`

</aside>

Deny ALL PACKETS that encapsulate a TCP segment from ANY source to DESTINATION 10.0.0.0/24

---

PRACTICE QUESTIONS:

1) ALLOW ALL TRAFFIC

`R1(config-ext-nacl)# permit ip any any` (ip is used for “all protocols”)

2) PREVENT 10.0.0.0/16 from SENDING UDP traffic to 192.168.1.1/32

`R1(config-ext-nacl)# deny udp 10.0.0.0 0.0.255.255 host 192.168.1.1`

3) PREVENT 172.16.1.1/32 from pinging hosts in 192.168.0.0/24

`R1(config-ext-nacl)# deny icmp host 172.16.1.1 192.168.0.0 0.0.0.255`

MATCHING THE TCP /  UDP PORT NUMBERS

- When matching TCP / UDP, you can optionally specify the SOURCE and/or DESTINATION PORT NUMBERS to match

![image](https://github.com/psaumur/CCNA/assets/106411237/c059d148-b685-49b2-81e0-518a6d66c25b)

eq = equal than

gt = greater than

lt = less than

neq = not equal to

range = range of ports

You can use either the PORT NUMBER or the specific TYPE (that has a KNOWN PORT NUMBER)

![image](https://github.com/psaumur/CCNA/assets/106411237/03dd80be-1f0f-41ac-ae1a-bdb851579bb4)

![image](https://github.com/psaumur/CCNA/assets/106411237/f7a11d7b-aeb6-4528-b5cc-62ff515fe33c)

---

PRACTICE QUESTIONS 2:

1) ALLOW TRAFFIC from 10.0.0.0/16 to access the server at 2.2.2.2/32 using HTTPS

`R1(config-ext-nacl)# permit tcp 10.0.0.0 0.0.255.255 host 2.2.2.2 eq 443`

2) PREVENT ALL HOSTS using SOURCE UDP Port Numbers from 20000 to 30000 from accessing the server at 3.3.3.3/32

`R1(config-ext-nacl)# deny udp any range 20000 30000 host 3.3.3.3`

3) ALLOW HOSTS in 172.16.1.0/24 using a TCP SOURCE Port greater than 9999 to access ALL TCP ports on server 4.4.4.4/32 EXCEPT port 23

`R1(config-ext-nacl)# permit tcp 172.16.1.0 0.0.0.255 gt 9999 host 4.4.4.4 neq 23`

EXAMPLE NETWORK

![image](https://github.com/psaumur/CCNA/assets/106411237/ddb40c27-b195-49fe-a12a-49e078166e30)

![image](https://github.com/psaumur/CCNA/assets/106411237/692f4a58-13d3-4c0a-8513-3dc76b014b65)

REQUIREMENTS:

- Hosts in 192.168.1.0/24 can’t use HTTPS to access SRV1
- Hosts in 192.168.2.0/24 can’t access 10.0.2.0/24
- NONE of the hosts in 192.168.1.0/24 or 192.168.2.0/24 can ping 10.0.1.0/24 OR 10.0.2.0/24

EXTENDED ACL #1 (Applied at R1 G0/1 INBOUND interface)

`R1(config)# ip access-list extended HTTP_SRV1`
`R1(config-ext-nacl)# deny tcp 192.168.1.0 0.0.0.255 host 10.0.1.100 eq 443`

`R1(config-ext-nacl)# permit ip any any`

`R1(config-ext-nacl)# int g0/1`

`R1(config-if)# ip access-group HTTP_SRV1 in`

EXTENDED ACL #2 (APPLIED at R1 G0/2 INBOUND interface)

`R1(config)# ip access-list extended BLOCK_10.0.2.0`

`R1(config-ext-nacl)# deny ip 192.168.2.0 0.0.0.255 10.0.2.0 0.0.0.255`

`R1(config-ext-nacl)# permit ip any any`

`R1(config-ext-nacl)# int g0/2`

`R1(config-if)# ip access-group BLOCK_10.0.2.0 in`

EXTENDED ACL #3 (APPLIED at R1 g0/0 OUTBOUND interface)

`R1(config)# ip access-list extended BLOCK_ICMP`

`R1(config-ext-nacl)# deny icmp 192.168.1.0 0.0.0.255 10.0.1.0 0.0.0.255`

`R1(config-ext-nacl)# deny icmp 192.168.1.0 0.0.0.255 10.0.2.0 0.0.0.255`

`R1(config-ext-nacl)# deny icmp 192.168.2.0 0.0.0.255 10.0.1.0 0.0.0.255`

`R1(config-ext-nacl)# permit ip any any`

`R1(config-ext-nacl)# int g0/0`

`R1(config-if)# ip access-group BLOCK_ICMP out`

What the EXTENDED ACLs look like

![image](https://github.com/psaumur/CCNA/assets/106411237/cda064f2-b1ce-45ee-a660-04cdceb3514b)

HOW TO SEE WHICH EXTENDED ACL’s ARE APPLIED TO AN INTERFACE

![image](https://github.com/psaumur/CCNA/assets/106411237/f596bca6-c06a-445e-84a3-8f8eb0c6baaf)

# 36. CDP and LLDP (Layer 2 Discovery Protocol)

INTRO TO LAYER 2 DISCOVERY PROTOCOLS

- LAYER 2 DISCOVERY PROTOCOL, such as CDP and LLDP share information WITH and DISCOVER information about NEIGHBORING (Connected) DEVICES

- The SHARED INFORMATION includes:
    - Hostname
    - IP Address
    - Device Type
    - etcetera.

- **CDP** is a Cisco Proprietary Protocol
- **LLDP** is an Industry Standard Protocol (IEEE 802.1AB)

- Because they SHARE INFORMATION about the DEVICES in the NETWORK, they can be considered a security risk and are often NOT used. It is up to the NETWORK ENGINEER / ADMIN to decide if they want to use them in the NETWORK or not.

![image](https://github.com/psaumur/CCNA/assets/106411237/65f39e9f-ae1a-42c6-8afb-5e79f939fe5d)

---

CISCO DISCOVERY PROTOCOL (CDP)

- CDP is a Cisco proprietary protocol
- It is enabled on Cisco devices (routers, switches, firewalls, IP Phones, etc) by DEFAULT

<aside>
💡 CDP Messages are periodically sent to Multicast MAC ADDRESS `0100.0CCC.CCCC`

</aside>


- When a DEVICE receives a CDP message, it PROCESSES and DISCARDS the message. It does NOT forward it to other devices.
- By DEFAULT, CDP Messages are sent once every **60 seconds**
- By DEFAULT, the CDP hold-time is **180 seconds.** If a message isn’t received from a neighbor for 180 seconds, the neighbor is REMOVED from the CDP Neighbor Table
- CDPv2 messages are sent by DEFAULT

![image](https://github.com/psaumur/CCNA/assets/106411237/8a0552be-dbc7-4c7b-b011-e32dff75a57e)

![image](https://github.com/psaumur/CCNA/assets/106411237/26e180ec-da08-44d2-bb55-325fdc0c234f)

---

CDP NEIGHBOR TABLES

![image](https://github.com/psaumur/CCNA/assets/106411237/00cd814e-0255-4fac-ac71-3e50054f813c)

“Device ID” = What devices were DISCOVERED by CDP

“Local Intrface” = What LOCAL device interface the neighbors are connected to

“Holdtime” = Hold-time countdown in seconds (0 = device removed from table)

“Capabilities” = Refers to Capability Codes table (located above output)

“Platform” = Displays the MODEL of the Neighbor Device

“Port ID” = Neighbor ports that LOCAL device is connected to

---

MORE DETAILED OUTPUT

![image](https://github.com/psaumur/CCNA/assets/106411237/cd4fbedb-c12f-4e1e-8582-8db16985121f)

“Version” = shows what version of Cisco’s IOS is running on the device

---

SHOW SPECIFIC CDP NEIGHBOR ENTRY

![image](https://github.com/psaumur/CCNA/assets/106411237/83ef9488-e82c-4453-ae6e-02575039d0f9)

---

CDP CONFIGURATION COMMANDS

![image](https://github.com/psaumur/CCNA/assets/106411237/393b2680-2304-4c8e-9180-88cc5fefbfd8)

- CDP is GLOBALLY ENABLED, by DEFAULT
- CDP is also ENABLED on each INTERFACE, by DEFAULT
- To ENABLE / DISABLE CDP globally: `R1(config)# [no] cdp run`
- To ENABLE / DISABLE CDP on specific interfaces : `R1(config-if)# [no] cdp enable`
- Configure the CDP timer: `R1(config)# cdp time *seconds*`
- Configure the CDP holdtime: `R1(config)# cdp holdtime *seconds*`
- ENABLE / DISABLE CDPv2: `R1(config)# [no] cdp advertise-v2`

 

---

LINK LAYER DISCOVERY PROTOCOL (LLDP)

- LLDP is an INDUSTRY STANDARD PROTOCOL (IEEE 802.1AB)
- It is usually DISABLED on Cisco devices, by DEFAULT, so it must be manually ENABLED
- A device can run CDP and LLDP at the same time

<aside>
💡 LLDP Messages are periodically sent to Multicast MAC ADDRESS `0180.c200.000E`

</aside>

- When a DEVICE receives an LLDP message, it PROCESSES and DISCARDS the message. It does NOT forward it to OTHER DEVICES
- By DEFAULT, LLDP Messages are sent once every **30 seconds**
- By DEFAULT, LLDP Holdtime is **120 seconds**
- LLDP has an additional timer called the ‘reinitialization delay’
    - If LLDP is ENABLED (Globally or on an INTERFACE), this TIMER will DELAY the actual initialization of LLDP (**2 seconds,** by DEFAULT)

---

LLDP CONFIGURATION COMMANDS

- LLDP is usually GLOBALLY DISABLED by DEFAULT
- LLDP is also DISABLED on each INTERFACE, by DEFAULT

- To ENABLE LLDP GLOBALLY : `R1(config)# lldp run`

- To ENABLE LLDP on specific INTERFACES (tx): `R1(config-if)# lldp transmit`
- To ENABLE LLDP on specific INTERFACES (rx): `R1(config-if)# lldp receive`

YOU NEED TO ENABLE BOTH TO SEND AND RECEIVE (Unless you want to only enable SEND or RECEIVE LLDP Messages)

 

- Configure the LLDP timer: `R1(config)# lldp timer *seconds*`
- Configure the LLDP holdtime: `R1(config)# lldp holdtime *seconds*`
- Configure the LLDP reinit timer: `R1(config)# lldp reinit *seconds*`

![image](https://github.com/psaumur/CCNA/assets/106411237/25afc5ad-4d82-4472-b282-31ed2a65eae7)

![image](https://github.com/psaumur/CCNA/assets/106411237/78fab926-9fda-4c83-91eb-eda4bf4ec005)

SHOW LLDP STATUS

![image](https://github.com/psaumur/CCNA/assets/106411237/32b11d7b-4050-422e-afd4-bec23e8db3a1)

SHOW ALL LLDP NEIGHBORS

![image](https://github.com/psaumur/CCNA/assets/106411237/85a46d24-5574-4400-bc03-6b0568294940)

SHOW LLDP NEIGHBORS in DETAIL

![image](https://github.com/psaumur/CCNA/assets/106411237/26751ca8-ed54-4e5c-9927-8c6eb0e2e3f7)

SHOW SPECIFIC LLDP DEVICE ENTRY

![image](https://github.com/psaumur/CCNA/assets/106411237/b5332838-d112-4556-bee0-c3716a3d4f89)

![image](https://github.com/psaumur/CCNA/assets/106411237/2dd16e33-75a9-4e11-91aa-b507ed490e9b)

# 37. NTP

WHY IS TIME IMPORTANT FOR NETWORK DEVICES?

- All DEVICES have an INTERNAL CLOCK (ROUTERS, SWITCHES, PCs, etc)
- In CISCO IOS, you can view the time with the `show clock` command

![image](https://github.com/psaumur/CCNA/assets/106411237/0afc355a-a982-4caa-a470-e09070e9c74f)

- If you use the `show clock detail` command, you can see the TIME SOURCE

![image](https://github.com/psaumur/CCNA/assets/106411237/a49cc147-ddba-405d-8e70-745ae7434e5a)

- The INTERNAL HARDWARE CLOCK of a DEVICE will “drift’ over time, so it’s NOT the ideal time source.
- From a CCNA perspective, the most important reason to have accurate time on a DEVICE is to have ACCURATE logs for troubleshooting

- **Syslog**, the protocol used to keep device logs, will be covered in a later video

Command: `show logging`

![image](https://github.com/psaumur/CCNA/assets/106411237/33632e20-a4e9-40fd-aba0-527498cfb886)

Note : R3’s time stamp is completely different than R2’s !!!

![image](https://github.com/psaumur/CCNA/assets/106411237/7d0464c2-1abe-460a-93fb-dd4368c905a7)

---

MANUAL TIME CONFIGURATION

- You can manually configure the TIME on the DEVICE with the `clock set` command

![image](https://github.com/psaumur/CCNA/assets/106411237/fa5d40c2-bccb-48e2-9f6b-c85ad721f37f)

- Although the HARDWARE CALENDAR (built-in clock) is the DEFAULT time-source, the HARDWARE CLOCK and SOFTWARE CLOCK are separate and can be configured separately.

---

HARDWARE CLOCK (CALENDAR) CONFIGURATION

- You can MANUALLY configure the HARDWARE CLOCK with the `calendar set` command

![image](https://github.com/psaumur/CCNA/assets/106411237/b72c898a-4746-49de-86db-c519964b3916)

- Typically, you will want to SYNCHRONIZE the ‘clock’ and ‘calendar’
- Use the command `clock update-calendar` to sync the calendar to the clock’s time
- Use the command `clock read-calendar` to sync the clock to the calendar’s time

![image](https://github.com/psaumur/CCNA/assets/106411237/c9d24bfd-25b1-4c5d-a426-f2a8a2db108c)

![image](https://github.com/psaumur/CCNA/assets/106411237/104a5e27-0d5f-40fc-aea8-dbcf46c3e195)

---

CONFIGURING THE TIME ZONE

- You can configure the time zone with the `clock timezone` command

![image](https://github.com/psaumur/CCNA/assets/106411237/d9ef5a95-a102-4306-bc3d-269fc5fd1d9e)

DAYLIGHT SAVING TIME (SUMMER TIME)

![image](https://github.com/psaumur/CCNA/assets/106411237/591491d1-a5bd-4f99-b518-02e722f41e1a)

![image](https://github.com/psaumur/CCNA/assets/106411237/3319f4c0-fb72-4486-b14c-4648c2be7338)

Full command :

`R1(config)# clock summer-time EDT recurring 2 Sunday March 02:00 1 Sunday November 02:00`

This covers the START of Daylight Savings and the end of Daylight Savings
---

SUMMARY OF COMMANDS

![image](https://github.com/psaumur/CCNA/assets/106411237/33557221-c045-4063-8ca0-9e8fb045ce52)

---

NTP BASICS

- Manually configuring the time on DEVICES is NOT Scalable
- The manually configured clocks will “drift”, resulting in inaccurate time
- NTP (Network Time Protocol) allows AUTOMATIC synchronization of TIME over a NETWORK
- NTP CLIENTS request the TIME from NTP SERVERS
- A DEVICE can be an NTP SERVER and an NTP CLIENT at the same time
- NTP allows accuracy of TIME with ~1 millisecond if the NTP SERVER is in the same LAN - OR within ~50 milliseconds if connecting to the NTP SERVER over a WAN / the INTERNET
- Some NTP SERVERS are ‘better’ than others. The ‘distance’ of an NTP SERVER from the original **reference clock** is called **stratum**

<aside>
💡 NTP uses UDP port 123 to communicate

</aside>

REFERENCE CLOCK

- A REFERENCE CLOCK is usually a VERY accurate time device like an ATOMIC CLOCK or GPS CLOCK
- REFERENCE CLOCKS are **stratum 0** within the NTP hierarchy
- NTP SERVERS directly connected to REFERENCE CLOCKS are **stratum 1**

![image](https://github.com/psaumur/CCNA/assets/106411237/003bf28a-03fe-49a8-954c-728f8e79dbd9)

(Peering with Devices is called …)

![image](https://github.com/psaumur/CCNA/assets/106411237/e2b91988-9be4-419b-b0b3-ad4ac32ae5cc)

- An NTP CLIENT can SYNC to MULTIPLE NTP SERVERS

![image](https://github.com/psaumur/CCNA/assets/106411237/32146173-fa80-4926-9524-ad66de3f9a6b)

---

NTP CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/6ee32d55-a33d-419c-9286-d1683f250d37)

![image](https://github.com/psaumur/CCNA/assets/106411237/453bd559-d88f-46c8-b4c9-cea958ef216d)

![image](https://github.com/psaumur/CCNA/assets/106411237/6adb6092-0290-4ae9-961d-55d25ec1d3c7)

Using key argument “prefer” makes a given server the PREFERRED SERVER

(To show configuration servers)

![image](https://github.com/psaumur/CCNA/assets/106411237/aabee138-5cb3-4316-8411-8da38d6dd2d5)

`sys.peer` = This is the SERVER that the current ROUTER (R1) is being synchronized to

`st` = Stratum Tier

(To show NTP Status)

![image](https://github.com/psaumur/CCNA/assets/106411237/4501f436-3e52-48c4-b22c-a733547b8b98)

`stratum 2` because it’s synchronizing from Google (stratum 1)

(To show NTP clock details)

![image](https://github.com/psaumur/CCNA/assets/106411237/bde14525-17e6-4d63-9d0b-b992c3dd7725)

This command configures the ROUTER to update the HARDWARE CLOCK (Calendar) with the time learned via NTP

`R1(config)# ntp update-calendar` 

The HARDWARE CLOCK tracks the DATE and TIME on the DEVICE - even if it restarts, power is lost, etc.

When the SYSTEM is restarted, the HARDWARE CLOCK is used to INITIALIZE the SOFTWARE CLOCK

---

CONFIGURE A LOOPBACK INTERFACE FOR AN NTP SERVER

![image](https://github.com/psaumur/CCNA/assets/106411237/21cac8d8-7c7f-41e1-8f0a-bfb6418c6085)

Why configure a LOOPBACK DEVICE on R1 for NTP ?

If one of R1’s ROUTER INTERFACES goes down, it will still be accessible via R3’s ROUTING path

![image](https://github.com/psaumur/CCNA/assets/106411237/9ead84f6-8645-489c-a30d-0b3c7ebf6ba1)

SET NTP SERVER for R2 using the LOOPBACK INTERFACE on R1

![image](https://github.com/psaumur/CCNA/assets/106411237/8a05e16e-cab9-429c-836e-e74a1007cbcb)

SETTING R3 NTP SOURCE SERVERS using R1 and R2

![image](https://github.com/psaumur/CCNA/assets/106411237/bcbd2426-1745-437a-9ebd-fe80dce6b527)

NOTE : R1 has PREFERENCE because it’s STRATUM TIER is HIGHER than R2s

---

CONFIGURING NTP SERVER MODE

![image](https://github.com/psaumur/CCNA/assets/106411237/038c5e31-587e-4a54-ae80-cc290a0ff805)

![image](https://github.com/psaumur/CCNA/assets/106411237/903a6aba-e99d-4ee6-a9c5-e077eed0592a)

![image](https://github.com/psaumur/CCNA/assets/106411237/0b5928d9-6594-4f3d-8663-8f4f19d3245b)

![image](https://github.com/psaumur/CCNA/assets/106411237/0aad6e81-5b7b-41ad-82b1-6c98690a9a4c)

![image](https://github.com/psaumur/CCNA/assets/106411237/e68f0ab9-25f5-4e65-8e80-f07b15878f69)

---

CONFIGURING NTP SYMMETRIC ACTIVE MODE

Command to configure NTP SYMMETRIC MODE 
`R2(config)#ntp peer <peer ip address>`

![image](https://github.com/psaumur/CCNA/assets/106411237/a0c27863-86d7-40e4-a935-6c73fce39439)

![image](https://github.com/psaumur/CCNA/assets/106411237/d430e372-8480-4378-92e4-5e5ca06f2ac1)

---

CONFIGURE NTP AUTHENTICATION

- NTP AUTHENTICATION can be configured, although it is OPTIONAL
- It allows NTP CLIENTS to ensure they only sync to the intended SERVERS
- To CONFIGURE NTP AUTHENTICATION:
    - `ntp authenticate` (Enables NTP AUTHENTICATION)
    - `ntp authenticate-key *key-number* md5 *key*` (Create the NTP AUTHENTICATION Key(s))
    - `ntp trusted-key *key-number`* (Specify the Trusted Key(s))
    - `ntp server *ip-address* key *key-number`* (Specify which key to use for the server)

 

EXAMPLE CONFIGURATIONS

![image](https://github.com/psaumur/CCNA/assets/106411237/d8f54d79-8975-4dfe-b0c0-e4e2b44f7b31)

---

NTP COMMAND REVIEW

![image](https://github.com/psaumur/CCNA/assets/106411237/2888ef4e-f53a-4ca3-ad34-0b04742edfd9)

# 38. DNS (Domain Name System)

THE PURPOSE OF DNS

- DNS is used to *resolve* human-readable names (google.com) to IP ADDRESSES
- Machines such as PCs don’t use names, they use ADDRESSES (ie: IPv4/IPv6)
- Names are much easier for us to use and remember than IP ADDRESSES
    - What is the IP ADDRESS of [youtube.com](http://youtube.com) ?
- When you type ‘youtube.com` into a web browser, your device will ask a DNS SERVER for the IP ADDRESS of [youtube.com](http://youtube.com)
- The DNS SERVER(S) your DEVICE uses can be manually configured or learned via DHCP

---

BASIC FUNCTIONS OF DNS

![image](https://github.com/psaumur/CCNA/assets/106411237/059c6fa4-674c-47ce-a08e-0714b21cb39e)

Command `ipconfig /all` (Show local IP configuration on current DEVICE)

![image](https://github.com/psaumur/CCNA/assets/106411237/b43b1d98-b510-4d05-be96-f706a3d090d1)

![image](https://github.com/psaumur/CCNA/assets/106411237/7f56b6f1-12c6-4096-9f73-28c9f8cfd570)

Command `nslookup` (Shows IP information for a given DNS entry)

![image](https://github.com/psaumur/CCNA/assets/106411237/71e5cd97-528c-435f-86d3-29d6ad2808b6)

WIRESHARK CAPTURE of above  COMMANDS

![image](https://github.com/psaumur/CCNA/assets/106411237/9d9cd65c-8a8b-45b3-8914-28a53013618f)

![image](https://github.com/psaumur/CCNA/assets/106411237/469431b3-e981-47cf-994d-642f737e79a0)

Command `ipconfig /displaydns` (Displays DNS cache)

![image](https://github.com/psaumur/CCNA/assets/106411237/da36bc07-d834-4c5e-b7ab-71da025b912f)

Command `ipconfig /flushdns` (Clears DNS cache)

![image](https://github.com/psaumur/CCNA/assets/106411237/f8608c2f-840c-477d-9284-7060838f1f3e)

HOSTS Files

WINDOWS HOSTS location

![image](https://github.com/psaumur/CCNA/assets/106411237/771b6bd4-abe4-41b7-afc2-3984ccc23407)

![image](https://github.com/psaumur/CCNA/assets/106411237/ff56876a-3b80-482f-b73b-caa86e5d972f)

---

CONFIGURING DNS IN CISCO IOS

- For HOSTS in a NETWORK to use DNS, you don’t need to configure DNS on the ROUTERS.
    - They will simply FORWARD the DNS messages like any other packets
- However, a CISCO ROUTER can be configured as a DNS SERVER, although it’s rare
    - If an INTERNAL DNS SERVER is used, usually it’s a WINDOWS or LINUX SERVER
- A CISCO ROUTER can also be configured as a DNS CLIENT

Command `ip dns server` and `ip host <hostname> <ip address>`

![image](https://github.com/psaumur/CCNA/assets/106411237/f65a4118-ae59-4db5-8fc4-c83d39c3072d)

![image](https://github.com/psaumur/CCNA/assets/106411237/59743697-6347-41de-9359-ca7ef327af01)

![image](https://github.com/psaumur/CCNA/assets/106411237/8e9c34c4-1a53-4ce4-a268-8a6d801d45e9)

Command `show hosts`

![image](https://github.com/psaumur/CCNA/assets/106411237/306aa507-1523-43e5-ac48-251e8a75b5f8)

Command `ip name-server` and `ip domain lookup`

![image](https://github.com/psaumur/CCNA/assets/106411237/cf0deb90-f8be-4f11-9373-2b7ef4715baf)

---

COMMAND REVIEW:

![image](https://github.com/psaumur/CCNA/assets/106411237/6c3e7873-04c4-407e-a851-cb74a9f78eb9)

# 39. DHCP (Dynamic Host Configuration Protocol)

THE PURPOSE OF DHCP

- DHCP is used to allow HOSTS to automatically / dynamically learn various aspects of their NETWORK configuration; without MANUAL / STATIC configuration
- It is an ESSENTIAL part of modern NETWORKS
    - When you connect a phone / laptop to WiFi, do you ask your NETWORK admin which IP ADDRESS, SUBNET MASK, DEFAULT GATEWAY, etc the phone / laptop should use ?
- Typically used for CLIENT devices (workstations, phones, etc)
- DEVICES (such as ROUTERS, SERVERS, etc) are usually MANUALLY configured
- In small NETWORKS (such as Home NETWORKS), the ROUTER typically acts as the DHCP SERVER for HOSTS in the LAN
- In LARGE NETWORKS, the DHCP SERVER is usually a Windows / Linux SERVER

---

BASIC FUNCTIONS OF DHCP

![image](https://github.com/psaumur/CCNA/assets/106411237/81b1e260-d669-4944-aa7b-5b7e6a505233)

![image](https://github.com/psaumur/CCNA/assets/106411237/8e7ff968-f47f-4877-88ec-451a9828905e)

![image](https://github.com/psaumur/CCNA/assets/106411237/ca9253f6-3e97-42d8-9293-7b271488be78)

![image](https://github.com/psaumur/CCNA/assets/106411237/b4659586-9e8b-482e-a492-fab9f979aa40)

![image](https://github.com/psaumur/CCNA/assets/106411237/bd292766-0a22-4c0a-ac96-0262ba03d720)

Note: ALL the IPs are the same because this is Jeremy’s Home ROUTER (it provides all these services)

Command `ipconfig /release`

![image](https://github.com/psaumur/CCNA/assets/106411237/13c9528b-8ecb-43e3-a3be-9993c03e1fa5)

![image](https://github.com/psaumur/CCNA/assets/106411237/46821c80-1fa1-435c-b71f-f2a81a2a415a)

Wireshark capture of the `ipconfig /release` mechanism

![image](https://github.com/psaumur/CCNA/assets/106411237/f9eb66a1-9c7e-4b5c-9393-9005f51ad172)

![image](https://github.com/psaumur/CCNA/assets/106411237/16e2b443-6ab6-49c4-bfde-2083c7b2185e)

---

Command `ipconfig /renew`

![image](https://github.com/psaumur/CCNA/assets/106411237/de06e7a3-b011-48eb-a5c6-8a6295258fbc)

Renewing Process has FOUR messages:

![image](https://github.com/psaumur/CCNA/assets/106411237/94febcd6-cd2b-4f6d-97db-69e33b1c1c4d)

1) DHCP DISCOVER

- Are there any DHCP Servers in this NETWORK? I need an IP ADDRESS ?

![image](https://github.com/psaumur/CCNA/assets/106411237/70f7fc01-3222-4fec-8bd3-8b96cfbc086f)

NOTE the use of DHCP Reserved Ports 67 and 68

2) DHCP OFFER:

- How about THIS IP ADDRESS ?

![image](https://github.com/psaumur/CCNA/assets/106411237/0f6e38bc-5eb0-4538-b0d1-e5795ee3af3a)

- The DHCP OFFER message can be either BROADCAST or UNICAST
- NOTE OPTIONS at the bottom : Message Type, Server ID, Lease Time, Subnet, etc.

3) DHCP REQUEST

- I want to use the IP ADDRESS that was offered

![image](https://github.com/psaumur/CCNA/assets/106411237/3023a977-2477-42ec-8890-283ef326bad1)

4) DHCP ACK

- Okay! You may use THAT ADDRESS

![image](https://github.com/psaumur/CCNA/assets/106411237/543c77e8-326b-45c6-a149-2f3668dac3ff)

---
DHCP RENEW PROCESS SUMMARY

![image](https://github.com/psaumur/CCNA/assets/106411237/a2f5cc4e-c949-4a8d-a985-29c6631c635e)

---

DHCP RELAY

- Some NETWORK engineers might choose to configure each ROUTER to act as the DHCP SERVER for its connected LANS
- However, large enterprises often choose to use a CENTRALIZED DHCP SERVER
- If the SERVER is centralized, it won’t receive the DHCP CLIENTS’ Broadcast DHCP messages
- To FIX this, you can configure a ROUTER to act as a DHCP RELAY AGENT
- The ROUTER will forward the clients’ Broadcast DHCP messages to the remote DHCP SERVER as a Unicast messages

![image](https://github.com/psaumur/CCNA/assets/106411237/3c0b188e-a120-499e-b089-18740d0d4559)

![image](https://github.com/psaumur/CCNA/assets/106411237/04c380f4-e1b4-46f3-89ab-1c89f16eed7a)

---

CONFIGURING DHCP IN CISCO IOS

Commands for configuring DHCP SERVERS in Cisco IOS

![image](https://github.com/psaumur/CCNA/assets/106411237/5cac378b-2769-4da2-bd46-1bd93dd5d144)

Command `show ip dhcp binding`

![image](https://github.com/psaumur/CCNA/assets/106411237/2cb89226-c24f-4cac-86f0-5cfb5ba16575)

![image](https://github.com/psaumur/CCNA/assets/106411237/4e10257e-2ca8-466f-96fc-f4a02ab319a4)

---

DHCP RELAY AGENT CONFIGURATION IN IOS

![image](https://github.com/psaumur/CCNA/assets/106411237/d1e1df72-85ef-4323-87f4-26cf14132bda)

RELAY AGENT MUST HAVE CONNECTIVITY WITH DHCP SERVER

---

DHCP CLIENT CONFIGURATION IN IOS

![image](https://github.com/psaumur/CCNA/assets/106411237/353e553c-b4a5-4f18-818f-3d7a395491b3)

---

COMMANDS SUMMARY

![image](https://github.com/psaumur/CCNA/assets/106411237/41e4ab84-7d5d-42e6-93d7-4b982976dd16)

# 40. SNMP (Simple Network Management Protocol)

SNMP OVERVIEW

- SNMP is an INDUSTRY-STANDARD FRAMEWORK and PROTOCOL that was originally released in 1988

These RFCs make up SNMPv1 (Do not need to memorize)

```
RFC 1065 - Structure and identification of management information for TCP/IP based internets
RFC 1066 - Management information base for network management of TCP/IP based internets
RFC 1067 - A simple network management protocol
```

- Don’t let the ‘Simple’ in the name fool you !
- SNMP can be used to monitor the STATUS of DEVICES, make CONFIGURATION CHANGES, etc.
- There are TWO MAIN TYPES of DEVICES in SNMP:
    - MANAGED DEVICES
        - These are the DEVICES being managed using SNMP
            - Ex: ROUTERS, SWITCHES
    - NETWORK MANAGEMENT STATION (NMS)
        - The DEVICE / DEVICES managing the MANAGED DEVICES
        - THIS is the SNMP ‘SERVER’

---

SMNP OPERATIONS

![image](https://github.com/psaumur/CCNA/assets/106411237/bfa13793-5bc7-4344-8592-f38ef3a64784)

---

SMNP COMPONENTS

OVERVIEW

![image](https://github.com/psaumur/CCNA/assets/106411237/632a83c5-27c8-4adc-8b08-079030c5f52c)

NMS

![image](https://github.com/psaumur/CCNA/assets/106411237/aa59534d-01d5-404c-bdf6-e0fd92cf9d98)

MANAGED DEVICES

![image](https://github.com/psaumur/CCNA/assets/106411237/656e27b1-86a4-42c7-a1a1-94309aa19610)

SNMP OIDs

- SNMP Object IDs are ORGANIZED in a HIERARCHICAL STRUCTURE

![image](https://github.com/psaumur/CCNA/assets/106411237/79180299-7d9a-4607-a592-7e7d8d090cd1)

---

SNMP VERSIONS

- Many versions of SNMP have been proposed/developed, however, only three major versions have achieved wide-spread use:

- **SNMPv1**
    - The ORIGINAL version of SNMP
- **SNMPv2c**
    - Allows the NMS to retrieve LARGE AMOUNTS of information in a SINGLE REQUEST, so it is more efficient
    - ‘c’ refers to the ‘community strings’ used as PASSWORDS in SNMPv1, removed from SNMPv2, and then added BACK for SNMPv2
- **SNMPv3**
    - A much more SECURE version of SNMP that supports STRONG ENCRYPTION and AUTHENTICATION.
        
        <aside>
        💡 WHENEVER POSSIBLE, this version should be used!
        
        </aside>
        

---

SNMP MESSAGES

![image](https://github.com/psaumur/CCNA/assets/106411237/25b15c81-931a-41a6-8033-dff07bfb5f15)

1) SNMP READ

![image](https://github.com/psaumur/CCNA/assets/106411237/e7d671f6-f2b0-468a-95a2-6678a52945c4)

2) SMNP WRITE

![image](https://github.com/psaumur/CCNA/assets/106411237/d8679ff7-5103-4e01-8f2e-25bb1bd25734)


3) SNMP NOTIFICATION

![image](https://github.com/psaumur/CCNA/assets/106411237/fe9266fc-12b8-41d3-8d8f-95f3f7b52ef6)


SNMP AGENT listens for MESSAGES on UDP Port 161

SNMP MANAGER listens for MESSAGES on UDP Port 162

![image](https://github.com/psaumur/CCNA/assets/106411237/23e6fd0a-ed1e-441b-b7b0-457a4e55f645)

---

SNMPv2c CONFIGURATION (Basic)

![image](https://github.com/psaumur/CCNA/assets/106411237/caf4624e-9ca2-4c8e-82fe-53db2499a38f)

WHAT HAPPENS WITH R1’s G0/1 INTERFACE GOES DOWN?

![image](https://github.com/psaumur/CCNA/assets/106411237/96341ab3-1ed3-4dd4-903c-fa57ab1f83be)

NOTE:

UDP message sent to Destination Port 162 (SNMP Manager)

“version” is set to v2c

community is “Jeremy1” (Read Only - no Set messages)

snmpV2-trap : trap message sent due to interface G0/1 going down

variable-bindings : contains the OID sent to identify the issue.

---

SNMP SUMMARY

- SNMP helps MANAGE DEVICES over a NETWORK
- MANAGED DEVICES are the devices being managed using SNMP (such as ROUTERS, SWITCHES, FIREWALLS)
- NETWORK MANAGEMENT STATIONS (NMS) are the SNMP “servers” that manage the devices
    - NMS receives notifications from Managed Devices
    - NMS changes settings on Managed Devices
    - NMS checks status of Managed Devices
    
- Variables, such as Interface Status, Temperature, Traffic Load, Hostname, etc are STORED in the MANAGMENT INFORMATION BASE (MIB) and identified using Object IDs (OIDs)

Main SNMP versions : SNMPv1, SNMPv2c, SNMPv3

```
SNMP MESSAGES : 
* Get / GetNext / GetBulk
* Set
* Trap
* Inform
* Response
```

# 41. SYSLOG

SYSLOG OVERVIEW

- SYSLOG is an INDUSTRY-STANDARD PROTOCOL for message logging
- On NETWORK DEVICES, SYSLOG can be used to LOG EVENTS
    - Changes in INTERFACE status (UP / DOWN)
    - Changes in OSFP NEIGHBOUR STATUS (UP / DOWN)
    - System Restarts
    - etc…
- The messages can be displayed in the CLI, saved in the DEVICE’S RAM or sent to an external SYSLOG SERVER

 ![image](https://github.com/psaumur/CCNA/assets/106411237/44a405e5-6cb1-41e3-b408-470afcaccd7e)

- Logs are essential when troubleshooting issues, examining the cause of incidents, etc.
- SYSLOG and SNMP are both used for MONITORING and TROUBLESHOOTING of DEVICES. They are complementary, but their functionalities are different

---

SYSLOG MESSAGE FORMAT

`seq: time stamp: %facility-severity-MNEMONIC:description`

<aside>
💡 These TWO FIELDS may or may not be displayed, depending on the DEVICE’S configuration

</aside>

`seq` = A SEQUENCE NUMBER indicating the order / sequence of messages

`time stamp` = A TIMESTAMP indicating the time the message was generated

`facility` = A VALUE that indicates which process on the DEVICE generated the message

`severity` = A NUMBER that indicates the severity of a logged event.

Official RFC for SYSLOG severity levels

<aside>
💡 LEVELS and KEYWORDS need to be MEMORIZED for the CCNA

</aside>

![image](https://github.com/psaumur/CCNA/assets/106411237/9ce46c98-a2b8-462b-ac6f-9bf13bfb3a99)

<aside>
💡 MEMORIZATION MNEMONIC : 
(E)very (A)wesome (C)isco (E)ngineer (W)ill (N)eed (I)ce cream (D)aily

</aside>

`MNEMONIC` = A SHORT CODE for the message, indicating what happened

`description` = Detailed information about the EVENT being reported

![image](https://github.com/psaumur/CCNA/assets/106411237/35413630-9194-4e63-8600-5847153e210e)

SYSLOG LOGGING LOCATIONS

- **CONSOLE LINE**
    - SYSLOG messages will be displayed in the CLI when connected to the DEVICE via the CONSOLE port. By DEFAULT, all messages (Level 0-7) are displayed
- **BUFFER**
    - Syslog messages will be saved to RAM. By default, ALL messages (Level 0-7) are displayed
- **VTY LINES**
    - SYSLOG messages will be displayed in the CLI when connected to the DEVICE via Telnet/SSH (coming in a later video). Disabled by default.

- **EXTERNAL SERVER**
    - You can configure the DEVICE to send SYSLOG messages to an external server

** SYSLOG SERVERS will listen for messages on UDP PORT 514 **

---

SYSLOG CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/a5321bcf-d149-4a3d-82a2-197426cf484a)

`level` works from the chosen level and upward toward Level 0 (EMERGENCY)

`level` or `keyword` from the Severity Table works when choosing a level

TERMINAL MONITOR

- Even if `logging monitor level` is enabled, by default SYSLOG messages will not be displayed when connected via Telnet or SSH
- For the messages to be displayed, you must use the following command:
    - `R1# terminal monitor`
- The command must be used **every time you connect to the DEVICE via Telnet or SSH**

LOGGING SYNCHRONOUS

- By default, logging messages displayed in the CLI while you are in the middle of typing a command will result in something like this:

![image](https://github.com/psaumur/CCNA/assets/106411237/bf0ed51a-c8b4-4c96-806a-ba90f829edd0)

- To prevent this, you should use `logging synchronous` on the appropriate *line*

![image](https://github.com/psaumur/CCNA/assets/106411237/350b34e5-8c87-417a-9e8d-fee7d3e57814)

- This will cause a new line to be printed if your typing is interrupted by a message

![image](https://github.com/psaumur/CCNA/assets/106411237/09acecd5-b25b-4585-80da-950d69e284ad)

SERVICE TIMESTAMPS and SERVICE SEQUENCE-NUMBERS

![image](https://github.com/psaumur/CCNA/assets/106411237/e1f9a979-eb27-47a7-af19-6496c74a4476)

---

SYSLOG versus SNMP

- SYSLOG and SNMP are both used for MONITORING and TROUBLESHOOTING of DEVICES. They are COMPLIMENTARY, but their FUNCTIONALITIES are different.

- SYSLOG
    - Used for MESSAGE LOGGING
    - Events that occur within the system are categorized based on FACILITY / SEVERITY and LOGGED
    - Used for SYSTEM MANAGEMENT, ANALYSIS, and TROUBLESHOOTING
    - Messages are sent from the DEVICES to the SERVER.
        - The SERVER can’t actively pull information from the DEVICES (like SNMP ‘get’) or modify variables (like SNMP ‘set’)
- SNMP
    - Used to retrieve and organize information about the SNMP managed DEVICES
        - IP ADDRESSES
        - Current INTERFACE status
        - Temperature
        - CPU Usage
        - etc…
    - SNMP SERVERS can use `Get` to query the CLIENTS and `Set` to MODIFY variables on the CLIENTS

# 42. SSH (Secure Shell)

CONSOLE PORT SECURITY

- By DEFAULT, no password us needed to access the CLI of a CISCO IOS DEVICE via the CONSOLE PORT
- You can CONFIGURE a PASSWORD on the *console line*
    - A USER will have to enter a PASSWORD to ACCESS the CLI via the CONSOLE PORT

![image](https://github.com/psaumur/CCNA/assets/106411237/9609b0af-0fb1-4563-89e4-82b58b29325e)

- Alternatively, you can configure the CONSOLE LINE to require USERS to LOGIN using one of the configured USERNAMES on the DEVICE

![image](https://github.com/psaumur/CCNA/assets/106411237/04588b3a-3640-41af-b19e-41768f63b2bc)

---

LAYER 2 SWITCH MANAGEMENT IP

- LAYER 2 SWITCHES do not perform PACKET ROUTING and build a ROUTING TABLE. They are NOT IP ROUTING aware
- However, you CAN assign an IP ADDRESS to an SVI to allow REMOTE CONNECTIONS to the CLI of the SWITCH (using Telnet or SSH)

![image](https://github.com/psaumur/CCNA/assets/106411237/64a9e983-f353-4670-8a99-1e22129eb661)

---

TELNET

- TELNET (Teletype Network) is a PROTOCOL used to REMOTELY ACCESS the CLI of a REMOTE HOST
- TELNET was developed in 1969
- TELNET has been largely REPLACE by SSH, which is MORE Secure
- TELNET sends data in PLAIN TEXT. NO ENCRYPTION(!)

<aside>
💡 TELNET SERVERS listen for TELNET traffic on TCP PORT 23

</aside>

![image](https://github.com/psaumur/CCNA/assets/106411237/9dffe7fb-4fa4-4ee9-90bf-d27461bb5190)

---

VERIFY TELNET CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/e077b5fd-3130-4fb0-9b17-d28bdef665df)

---

SSH

- SSH (Secure Shell) was developed in 1995 to REPLACE LESS SECURE PROTOCOLS, like TELNET
- SSHv2, a major revision of SSHv1, was released in 2006
- If a DEVICE supports both v1 and v2, it is said to run ‘version 1.99’
- Provides SECURITY features; such as DATA ENCRYPTION and AUTHENTICATION

CHECK SSH SUPPORT

![image](https://github.com/psaumur/CCNA/assets/106411237/441c38b7-4b79-4c80-8eca-0463960124b6)

RSA KEYS

- To ENABLE and use SSH, you must first generate an RSA PUBLIC and PRIVATE KEY PAIR
- The KEYS are used for DATA ENCRYPTION / DECRYPTION, AUTHENTICATION, etc.

![image](https://github.com/psaumur/CCNA/assets/106411237/73bd5a86-32da-4ec6-b385-fe5425a72808)

VTY LINES

![image](https://github.com/psaumur/CCNA/assets/106411237/04e9072f-ccde-476d-a84d-3034e0b39d19)

---

SUMMARY ABOUT SSH CONFIGURATIONS

![image](https://github.com/psaumur/CCNA/assets/106411237/bb6d358f-e742-434b-835c-5c7cd762abdb)

![image](https://github.com/psaumur/CCNA/assets/106411237/bb2e760b-90c3-42a7-93f6-0ccc7e472d00)

# 43. FTP and TFTP

THE PURPOSE OF FTP / TFTP

- FTP (File Transfer Protocol) and TFTP (Trivial File Transfer Protocol) are INDUSTRY STANDARD PROTOCOLS used to TRANSFER FILES over a NETWORK
- They BOTH use a CLIENT-SERVER model
    - CLIENTS can use FTP / TFTP to COPY files FROM a SERVER
    - CLIENTS can use FTP / TFTP to COPY files TO a SERVER
- As a NETWORK ENGINEER, the most common use for FTP / TFTP is in the process of UPGRADING the OPERATING SYSTEM of a NETWORK DEVICE
- You can use FTP / TFTP to DOWNLOAD the newer version of IOS from a SERVER and then REBOOT the DEVICE with the new IOS image

![image](https://github.com/psaumur/CCNA/assets/106411237/c3f8288f-cc21-476b-ab36-685fa843f947)

---

TFTP and FTP FUNCTIONS AND DIFFERENCES

TFTP

- TFTP first standardized in 1981
- Named “Trivial” because it’s SIMPLE and has only basic features compared to FTP
    - Only allows a CLIENT to COPY FILES to / from a SERVER
- Was released after FTP, but not a REPLACEMENT for FTP.
    - It’s another tool to use when LIGHTWEIGHT SIMPLICITY is more important than FUNCTIONALITY
- NO AUTHENTICATION (Username / Password) so SERVERS will respond to ALL FTP REQUESTS
- NO ENCRYPTION. All DATA is sent PLAIN TEXT
- Best used in a CONTROLLED environment to transfer SMALL FILES quickly
- TFTP SERVERS listen on UDP PORT 69
- UDP is CONNECTIONLESS and doesn’t provided RELIABILITY with RETRANSMISSIONS
- However, TFTP has SIMILAR built-in FEATURES within the PROTOCOL itself

TFTP RELIABILITY

- Every TFTP DATA message is ACKNOWLEDGED
    - If the CLIENT is transferring a FILE TO the SERVER, the SERVER will send ACK messages
    - If the SERVER is transferring a FILE TO the CLIENT, the CLIENT will send ACK messages
- TIMERS are used, and if an EXPECTED message isn’t received in time, the waiting DEVICE will RESEND its previous message.

![image](https://github.com/psaumur/CCNA/assets/106411237/6b8f914e-0d8f-4cfd-bbbb-3552b5cebb3e)

TFTP “CONNECTIONS”

![image](https://github.com/psaumur/CCNA/assets/106411237/d6634813-5132-4fd8-a712-7bc7b4ea21db)

TFTP TID (Not in the CCNA exam)

- When the CLIENT sends the FIRST message to the SERVER, the DESTINATION PORT is UDP 69 and the SOURCE PORT is a random EPHEMERAL PORT
- This “random port” is called a “TRANSFER IDENTIFIER” (TID) and identifies the DATA TRANSFER
- The SERVER then also selects a RANDOM TID to use as a SOURCE PORT when it replies, NOT UDP 69
- When the CLIENT sends the NEXT message, the DESTINATION PORT will be the SERVER’S TID, NOT UDP 69

UDP PORT 69 (TFTP) is only used at the initial request message

![image](https://github.com/psaumur/CCNA/assets/106411237/5976c631-4cba-4449-a2b4-912f90cb66e1)

--- 

FTP

- FTP was first standardized in 1971
- FTP uses TCP PORTS 20 and 21
- USERNAMES and PASSWORDS are used for AUTHENTICATION, however there is NO ENCRYPTION
- For GREATER security, FTPS (FTP over SSL / TLS) can be used (Upgrade to FTP)
- SSH File Transfer Protocol (SFTP) can also be used for GREATER security (New Protocol)
- FTP is MORE complex than TFTP and ALLOWS not only FILE TRANSFERS but CLIENTS can also:
    - Navigate FILE DIRECTORIES
    - ADD / REMOVE FILES
    - LIST FILES
    - etc…
- The CLIENT sends FTP *commands* to the SERVER to perform these functions

FTP CONTROL CONNECTIONS

- FTP uses TWO TYPES of connections:
    - An FTP CONTROL connection (TCP 21) is established and used to send FTP commands and replies
    - When FILES or DATA are to be transferred, separate FTP DATA (TCP 20) connections are established and terminated as needed

![image](https://github.com/psaumur/CCNA/assets/106411237/8ff1d9a5-785b-4fb4-86a4-766c1107812f)

ACTIVE MODE FTP DATA CONNECTIONS

- The DEFAULT method of establishing FTP DATA connections is ACTIVE MODE in which the SERVER initiates the TCP connection.

![image](https://github.com/psaumur/CCNA/assets/106411237/49909dbc-1ed5-425b-8958-03fcaf5b9eab)

- In FTP PASSIVE MODE, the CLIENT initiates the DATA connection.
    - This is often necessary when the CLIENT is behind a FIREWALL, which could BLOCK the INCOMING CONNECTION from the SERVER

![image](https://github.com/psaumur/CCNA/assets/106411237/5872df1c-b97f-4f61-b0da-6a06e7f69f1a)

FTP VERSUS TFTP

![image](https://github.com/psaumur/CCNA/assets/106411237/e7c11655-61be-40f0-943c-8c51998dc2e2)

---

IOS FILE SYSTEMS

- A FILE SYSTEM is a way of controlling how DATA is STORED and RETRIEVED
- You can VIEW the FILE SYSTEM of a Cisco IOS DEVICE with `show file systems`

![image](https://github.com/psaumur/CCNA/assets/106411237/eb6e12b6-3c34-4e05-93cb-e4368764da74)

---

USING FTP / TFTP IN IOS

- You can VIEW the current version of IOS with `show version`

![image](https://github.com/psaumur/CCNA/assets/106411237/746859c5-d89d-42f5-b198-d0cba7f3682d)

- You can VIEW the contents of flash with `show flash`

![image](https://github.com/psaumur/CCNA/assets/106411237/d131b08c-572d-46b3-8910-0d423b85dc94)

---

COPYING FILES WITH TFTP

STEP 1

![image](https://github.com/psaumur/CCNA/assets/106411237/f0ce7ea9-115e-4db8-9baf-55ee1bf0d548)

STEP 2

![image](https://github.com/psaumur/CCNA/assets/106411237/9be3610d-3e22-476f-ab90-117ba7d93cf0)

STEP 3

![image](https://github.com/psaumur/CCNA/assets/106411237/604528f7-af5d-44a4-a877-c9d82d7910d1)

---

COPYING FILES WITH FTP

STEP 1

![image](https://github.com/psaumur/CCNA/assets/106411237/0e9c1dc5-0dce-4cbb-b584-0509c2119f63)

STEP 2 and 3 identical to TFTP above

---

COMMAND SUMMARY

![image](https://github.com/psaumur/CCNA/assets/106411237/e5f525cd-6e98-4501-9e7c-1c1f4af1d23e)

# 44. NAT (STATIC): PART 1

PRIVATE IPv4 ADDRESSES (RFC 1918)

- IPv4 doesn’t provide enough ADDRESSES for all DEVICES that need an IP ADDRESS in the modern world
- The long-term solution is to switch to IPv6
- There are THREE MAIN short-term solutions:
    - CIDR
    - PRIVATE IPv4 ADDRESS
    - NAT
- RFC 1918 specifies the following IPv4 ADDRESS RANGES as PRIVATE:
    
    ```
    10.0.0.0 /8       (10.0.0.0 to 10.255.255.255)             CLASS A 
    172.16.0.0 /12    (172.16.0.0 to 172.31.255.255)           CLASS B
    192.168.0.0 /16   (192.168.0.0 to 192.168.255.255)         CLASS C
    ```
    
- You are free to use these ADDRESSES in your NETWORKS. They don’t have to be GLOBALLY UNIQUE

![image](https://github.com/psaumur/CCNA/assets/106411237/c774460a-0479-40ed-ac62-1e9820960943)

---

INTRO TO NAT

- NETWORK ADDRESS TRANSLATION (NAT) is used to modify the SOURCE and / or DESTINATION IP ADDRESSES of packets
- There are various reasons to use NAT, but the MOST common reason is to ALLOW HOSTS with PRIVATE IP ADDRESSES to communicate with other HOSTS over the INTERNET
- For the CCNA you have to understand SOURCE NAT and how to configure it on CISCO ROUTERS

![image](https://github.com/psaumur/CCNA/assets/106411237/11cbc222-4b2d-4283-9a8f-86cfff2e109d)

---

STATIC NAT

- STATIC NAT involves statically configuring ONE-TO-ONE MAPPINGS of PRIVATE IP ADDRESSES to PUBLIC ADDRESSES

![image](https://github.com/psaumur/CCNA/assets/106411237/40867b28-66ff-4182-be97-8495a4c2de23)

![image](https://github.com/psaumur/CCNA/assets/106411237/b77177cc-f6e3-434f-87e0-fb5d0fe14c90)

![image](https://github.com/psaumur/CCNA/assets/106411237/daac56f4-5af8-482c-9d1d-63a0fb3bdcb1)

PRIVATE IP CANNOT BE MAPPED TO THE SAME GLOBAL IP

THE SECOND MAPPING WILL BE REJECTED

![image](https://github.com/psaumur/CCNA/assets/106411237/6dceb3c2-39d6-4299-b08d-90cbddb8d6b3)

---

STATIC NAT CONFIGURATIONS

![image](https://github.com/psaumur/CCNA/assets/106411237/1b0d6780-56d8-4ea0-870b-abb65d3a6e66)

![image](https://github.com/psaumur/CCNA/assets/106411237/add755f6-2d2c-4fe8-aae1-6d1aeecb6ea2)

Command `clear ip nat translation`

![image](https://github.com/psaumur/CCNA/assets/106411237/4266d928-0970-4386-82d7-159cc2b02df6)

Command `show ip nat statistics`

![image](https://github.com/psaumur/CCNA/assets/106411237/2e70576f-3879-4ba6-8ffa-307fd0c243c9)

---

COMMAND REVIEW

![image](https://github.com/psaumur/CCNA/assets/106411237/061f4c43-e755-41e8-b8b4-9e31e0723a19)

# 45. NAT (DYNAMIC): PART 2

MORE ABOUT STATIC NAT

- STATIC NAT involves statically configuring one-to-one mappings of PRIVATE IP ADDRESSES to PUBLIC IP ADDRESSES
- When traffic from the INTERNAL HOST is sent to the OUTSIDE NETWORK, the ROUTER will translate the SOURCE ADDRESS

![image](https://github.com/psaumur/CCNA/assets/106411237/60ba15dd-ee70-4bd9-b9a7-febf3ebbcd10)

- HOWEVER, this one-to-one mapping also allows EXTERNAL HOSTS to access the INTERNAL HOST via INSIDE GLOBAL ADDRESS

![image](https://github.com/psaumur/CCNA/assets/106411237/09de8e06-249c-4185-9d09-ca5fc1435f5a)

---

DYNAMIC NAT

- In DYNAMIC NAT, the ROUTER dynamically maps INSIDE LOCAL ADDRESSES to INSIDE GLOBAL ADDRESSES, as needed
- An ACL is used to identify WHICH traffic should be translated
    - If the SOURCE IP is PERMITTED; the SOURCE IP will be translated
    - If the SOURCE IP is DENIED; the SOURCE IP will NOT be translated
        
        <aside>
        💡 However, Packet Traffic will NOT be dropped
        
        </aside>
        
- A NAT POOL is used to define the available INSIDE GLOBAL ADDRESS

![image](https://github.com/psaumur/CCNA/assets/106411237/98fe2d7d-345c-4d6b-9772-4b152f9bd7a3)

  

- Although they are dynamically assigned, the mappings are still one-to-one (one INSIDE LOCAL IP ADDRESS per INSIDE GLOBAL IP ADDRESS)
- If there are NOT enough INSIDE GLOBAL IP ADDRESSES available (=ALL are being used), it is called ‘NAT POOL EXHAUSTION’
    - If a PACKET from another INSIDE HOST arrives and needs NAT but there are no AVAILABLE ADDRESSES, the ROUTER will drop the PACKET
    - The HOST will be unable to access OUTSIDE NETWORKS until one of the INSIDE GLOBAL IP ADDRESSES becomes available
    - DYNAMIC NAT entries will time out automatically if not used, or you can clear them manually

NAT POOL EXHAUSTION

![image](https://github.com/psaumur/CCNA/assets/106411237/59c01575-b42f-475b-9502-2f9ed490ca8d)

192.168.0.167 TIMES OUT and 192.168.0.98 is assigned it’s TRANSLATED SOURCE IP

![image](https://github.com/psaumur/CCNA/assets/106411237/59e68f3b-8acc-4d7e-8d8e-f930dec3be5f)

DYNAMIC NAT CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/6694689a-4880-497c-a1f6-838003810f0c)

`show ip nat translations`

![image](https://github.com/psaumur/CCNA/assets/106411237/5b656147-f61c-4313-9a7e-34bec3ae6fbf)

![image](https://github.com/psaumur/CCNA/assets/106411237/04951fde-f130-43f8-b2ce-05eba6382329)

![image](https://github.com/psaumur/CCNA/assets/106411237/99bb39f3-2ea7-44d2-929e-223755726882)

---

DYNAMIC PAT (NAT OVERLOAD)

- PAT (NAT OVERLOAD) translates BOTH the IP ADDRESS and the PORT NUMBER (if necessary)
- By using a unique PORT NUMBER for each communication flow, a single PUBLIC IP ADDRESS can be used by many different INTERNAL HOSTS
    - PORT NUMBERS are 16 bits = over 65,000 available port numbers
- The ROUTER will keep track of which INSIDE LOCAL ADDRESS is using which INSIDE GLOBAL ADDRESS and PORT

![image](https://github.com/psaumur/CCNA/assets/106411237/8f720b58-9700-4908-bd8d-a1846191854b)

PAT CONFIGURATION (POOL)

![image](https://github.com/psaumur/CCNA/assets/106411237/2a1acc30-658c-4479-9984-9c620b5e6ce3)

`show ip nat translations`

![image](https://github.com/psaumur/CCNA/assets/106411237/088db6f4-a695-4765-b435-2f20a5e16c9e)

PAT CONFIGURATION (INTERFACE)

![image](https://github.com/psaumur/CCNA/assets/106411237/8a3990ff-c58e-44a9-928d-e534f0cff690)

![image](https://github.com/psaumur/CCNA/assets/106411237/557d0217-80d2-4423-ba6a-041703568e13)

`show ip nat translations`

![image](https://github.com/psaumur/CCNA/assets/106411237/cae56ec7-38b5-4053-beda-ff670083718e)

---

COMMAND REVIEW

![image](https://github.com/psaumur/CCNA/assets/106411237/fe0655bb-4020-4ddc-bec4-b2fb198e2314)

# 46. QoS (Voice VLANs) : PART 1

IP PHONES / VOICE LANS

- Traditional phones operate over the *public switched telephone network* (PSTN)
    - Sometimes, this is called POTS (Plain Old Telephone System)
- IP PHONES use VoIP (Voice Over IP) technologies to enable phone calls over an IP NETWORK, such as the INTERNET
- IP PHONES are connected to a SWITCH, just like any other end HOST

IP PHONES

- Have an internal 3-PORT SWITCH
    - 1 PORT is the “UPLINK” to the EXTERNAL SWITCH
    - 1 PORT is the “DOWNLINK” to the PC
    - 1 PORT connects internally to the PHONE itself

![image](https://github.com/psaumur/CCNA/assets/106411237/0bba51c0-af57-49e4-ae29-fca2a1079a34)

- This allows the PC and the IP PHONE to share a single SWITCH PORT. Traffic from the PC passes through the IP PHONE to the SWITCH
- It is RECOMMENDED to separate “VOICE” traffic (from IP PHONE) and “DATA TRAFFIC” (from the PC) by placing them into SEPARATE VLANS (!)
    - This can be accomplished using a VOICE VLAN
    - Traffic from the PC will be UNTAGGED - but traffic from the PHONE will be tagged with a VLAN ID

![image](https://github.com/psaumur/CCNA/assets/106411237/12a1bfa5-036a-4eb6-b165-23fc8209a1f8)

![image](https://github.com/psaumur/CCNA/assets/106411237/b7c5b7e6-fa79-4405-b72f-b609ab56f216)

![image](https://github.com/psaumur/CCNA/assets/106411237/fc26e9dd-e19e-43cc-9f2a-4022b47f98b4)

---

POWER OVER ETHERNET (PoE)

- PoE allows Power Sourcing Equipment (PSE) to provide POWER to Powered Devices (PD) over an ETHERNET cable
- Typically, the PSE is a SWITCH and the PDs are IP PHONES, IP CAMERAS, WIRELESS ACCESS POINTS, etc.
- The PSE receives AC POWER from the outlet, converts it to DC POWER, and supplies that DC POWER to the PDs

![image](https://github.com/psaumur/CCNA/assets/106411237/4229e398-a50e-487c-adf3-66b235ea9189)

- TOO much electrical current can damage electrical DEVICES
- PoE has a process to determine if a CONNECTED DEVICE needs power and how much it needs.
    - When a DEVICE is connected to a PoE-Enabled PORT, the PSE (SWITCH) sends LOW POWER SIGNALS, monitors the response, and determines how much power the PD needs
    - If the DEVICE needs POWER, the PSE supplies the POWER to allow the PD to boot
    - The PSE continues to monitor the PD and SUPPLY the required amount of POWER (but not too much!)
- *POWER POLICING* can be configured to prevent a PD from taking TOO much POWER
    - 'power inline police' configures power policing with the default settings:  disable the PORT and send a SYSLOG message if a PD draws too much power
        - Equivalent to 'power inline police action err-disable'
        - The INTERFACE will be put in an ‘error-disabled’ state and can be re-enabled with 'shutdown' followed by 'no shutdown'
    
    ![image](https://github.com/psaumur/CCNA/assets/106411237/59914c0d-2c0e-4952-a4af-1f7ada02002d)
    -  'power inline police action log' does NOT shut down the INTERFACE if the PD draws too much power. It WILL restart the INTERFACE and send a SYSLOG message
    
    ![image](https://github.com/psaumur/CCNA/assets/106411237/9717fb1e-9129-41f9-90bb-613c2bdee460)
    
    ![image](https://github.com/psaumur/CCNA/assets/106411237/8fe2eb15-49be-4f63-9f6f-79c0d5fe052f)
    

---

INTRO TO QUALITY OF SERVICE (QoS)

- VOICE traffic and DATA traffic used to use entirely separate NETWORKS
    - VOICE TRAFFIC used the PSTN
    - DATA TRAFFIC used the IP NETWORK (Enterprise WAN, Internet, etc)
- QoS wasn’t necessary as the different kinds of TRAFFIC didn’t compete for BANDWIDTH

![image](https://github.com/psaumur/CCNA/assets/106411237/8a21a767-5a93-42bd-a8d4-52453f8a7341)

- Modern NETWORKS are typically *converged networks* in which IP PHONES, VIDEO TRAFFIC, REGULAR TRAFFIC, etc. all share the same IP NETWORK
- This enables COST SAVINGS as well as more ADVANCED FEATURES for VOICE and VIDEO TRAFFIC (Example : Collaboration Software like Cisco WebEx, MS Teams, etc)
- HOWEVER, the different kinds of TRAFFIC now have to compete for BANDWIDTH
- **QoS** is a set of TOOLS used by NETWORK DEVICES to apply different TREATMENT to different PACKETS

![image](https://github.com/psaumur/CCNA/assets/106411237/8909efdb-bbbd-4f50-b412-7abe12a3bcef)

QUALITY OF SERVICE (QoS)

- QoS is used to manage the following characteristics of NETWORK TRAFFIC
    - BANDWIDTH
        - Overall CAPACITY of the LINK (measured in *bits per second*)
        - QoS TOOLS allow you to RESERVE a certain amount of a link’s BANDWIDTH for specific kinds of traffic
    - DELAY
        - One-Way Delay = Time it takes traffic to go from SOURCE to DESTINATION
        - Two-Way Delay = Time it takes traffic to go from SOURCE to DESTINATION and return
        
![image](https://github.com/psaumur/CCNA/assets/106411237/29ed6306-a6aa-46ba-af2f-5ebcd383d1d7)
        
    
    - JITTER
        - The variation in ONE-WAY DELAY between PACKETS SENT by the same APPLICATION
        - IP PHONES have a ‘jitter buffer’ to provide a FIXED DELAY to audio PACKETS
    - LOSS
        - The % of PACKETS sent that DO NOT reach their DESTINATION
        - Can be caused by FAULTY CABLES
        - Can also be caused when a DEVICE’S PACKET QUEUES get full and the DEVICE starts discarding PACKETS
    
- The FOLLOWING STANDARDS are recommended for ACCEPTABLE INTERACTIVE AUDIO quality:
    - ONE-WAY DELAY : 150 milliseconds or less
    - JITTER : 30 milliseconds or less
    - LOSS : 1% or less
    
- If these STANDARDS are not met, there could be a noticeable reduction in the QUALITY of the phone call
    
    

QoS QUEUING

- If a NETWORK DEVICE receives messages FASTER than it can FORWARD them out of the appropriate INTERFACE, the MESSAGES are placed in the QUEUE
- By default, the QUEUED MESSAGES will be FORWARDED in a FIRST IN FIRST OUT (FIFO) manner
    - Message will be SENT in the ORDER they are RECEIVED
- If the QUEUE is FULL, new PACKETS will be DROPPED
- The is called *tail drop*

![image](https://github.com/psaumur/CCNA/assets/106411237/15de2fcd-5711-4014-8185-9975b2ce8a0d)

- TAIL DROP is harmful because it can lead to TCP GLOBAL SYNCHRONIZATION

![image](https://github.com/psaumur/CCNA/assets/106411237/1d22afa7-91aa-4e86-9c5f-ad9506dcb44c)

- When the QUEUE fills UP and TAIL DROP occurs, ALL TCP HOSTS sending traffic will SLOW DOWN the rate at which they SEND TRAFFIC
- They will ALL then INCREASE the RATE at which they send TRAFFIC, which rapidly leads to MORE CONGESTION, dropped PACKETS, and the process REPEATS…

![image](https://github.com/psaumur/CCNA/assets/106411237/b75c2cac-043c-4df6-a1d6-f26d9110630a)

- A SOLUTION to prevent TAIL DROP and TCP GLOBAL SYNCHRONIZATION is RANDOM EARLY DETECTION (RED)

- When the amount of TRAFFIC in the QUEUE reaches a certain THRESHOLD, the DEVICE will start RANDOMLY dropping PACKETS from select TCP FLOWS
- Those TCP FLOWS that dropped PACKETS will reduce the RATE at which TRAFFIC is sent, but you will avoid TCP GLOBAL SYNCHRONIZATION, in which ALL TCP FLOWS reduce and then increase the rate of transmission at the same time, in waves.
- In STANDARD RED, all kinds of TRAFFIC are treated the SAME
- WEIGHTED RANDOM EARLY DETECTION (WRED) - an improved version of RED, allows you control which PACKETS are dropped depending on the TRAFFIC CLASS

** TRAFFIC CLASSES and details about how QoS works will be covered in DAY 47 **

# 47. QoS (Quality of Service) : PART 2

CLASSIFICATION / MARKING

- The purpose of QoS is to give certain kinds of NETWORK TRAFFIC priority over other during congestion
- CLASSIFICATION organizes network TRAFFIC (PACKETS) into TRAFFIC CLASSES (CATEGORIES)
- CLASSIFICATION is fundamental to QoS.
    - To give PRIORITY to certain types of TRAFFIC, you have to IDENTIFY which types of TRAFFIC to give PRIORITY to.
- There are MANY methods of CLASSIFYING TRAFFIC
    - An ACL : TRAFFIC which is permitted by the ACL will be given certain TREATMENT, other TRAFFIC will not
    - NBAR (Network Based Application Recognition) performs a *DEEP PACKET INSPECTION,* looking beyond the LAYER 3 and LAYER 4 information up to LAYER 7 to identify the specific kinds of TRAFFIC
    - In the LAYER 2 and LAYER 3 HEADERS there are specific FIELDS used for this purpose
- The PCP (PRIORITY CODE POINT) FIELD of the 802.1Q Tag (in the ETHERNET HEADER) can be used to identify HIGH / LOW PRIORITY TRAFFIC
    - ** ONLY when there is a dot1q tag!
- The DSCP (DIFFERENTIATED SERVICES CODE POINT) FIELD of the IP HEADER can also be used to identify HIGH / LOW PRIORITY TRAFFIC

---

PCP / CoS

![image](https://github.com/psaumur/CCNA/assets/106411237/2d2037b6-6992-4758-a1cb-5df0f939b153)

- PCP is also known as CoS (CLASS OF SERVICE)
- It’s use is defined by IEEE 802.1p
- 3 bits = 8 possible values (2^3 = 8)

![image](https://github.com/psaumur/CCNA/assets/106411237/af191e31-082d-43c0-ab76-225d4dd2e354)

- PCP VALUE 0:
    - “BEST EFFORT” DELIVERY means there is no guarantee that data is delivered or that it meets ANY QoS Standard. This is REGULAR TRAFFIC - NOT HIGH PRIORITY

- PCP VALUE 3 and 5:
    - IP PHONES MARK call signaling TRAFFIC (used to establish calls) as PCP3
        - They MARK the actual VOICE TRAFFIC as PCP5

- Because PCP is found in the dot1q header, it can only be used over the following connections:
    - TRUNK LINKS
    - ACCESS LINKS with a VOICE VLAN
    
- In the diagram below, TRAFFIC between R1 and R2, or between R2 and EXTERNAL DESTINATIONS will not have a dot1q tag. So, traffic over those links PCP cannot be marked with a PCP value.

![image](https://github.com/psaumur/CCNA/assets/106411237/07a1cbb3-d034-4a9b-accc-59e7f738452f)

---

THE IP ToS BYTE

![image](https://github.com/psaumur/CCNA/assets/106411237/3323ff23-96a5-45f4-abde-893d72a4021f)

![image](https://github.com/psaumur/CCNA/assets/106411237/ffec398b-7b0a-47a1-9758-a7a14daf6aa0)

(6 bits for DSCP and 2 bits for ECN)

---

IP PRECEDENCE (OLD)

![image](https://github.com/psaumur/CCNA/assets/106411237/1b0ca3ca-fc8d-4225-9368-64c8ff9587da)

- Standard IPP markings are similar to PCP:
    - 6 and 7 are reserved to ‘network control traffic’ (ie: OSPF Messages between ROUTERS)
    - 5 = VOICE
    - 4 = VIDEO
    - 3 = VOICE SIGNALLING
    - 0 = BEST EFFORT
- With 6 and 7 reserved, 6 possible values remain
- Although 6 values is sufficient for many NETWORKS, the QoS REQUIREMENTS of some NETWORKS demand more flexibility

---

DSCP (CURRENT)

![image](https://github.com/psaumur/CCNA/assets/106411237/48a63948-81b9-43d5-a108-34525a381533)

- RFC 2474 (1998) defines the DSCP field, and other ‘DiffServ’ RFCs elaborate on its use
- With IPP updated to DSCP, new STANDARD MARKINGS had to be decided on
    - By having generally agreed upon STANDARD MARKINGS for DIFFERENT KINDS of TRAFFIC:
        - QoS DESIGN and IMPLEMENTATION is simplified.
        - QoS works better between ISPs and ENTERPRISES
        - etc.

- You should be AWARE of the FOLLOWING STANDARD MARKINGS:
    - DEFAULT FORWARDING (DF) - Best Effort TRAFFIC
    - EXPEDITED FORWARDING (EF) - Low Loss / Latency / Jitter TRAFFIC (usually voice)
    - ASSURED FORWARDING (AF) - A set of 12 STANDARD VALUES
    - CLASS SELECTOR (CS) - A set of 8 STANDARD VALUES, provides backward compatibility with IPP

---

DF / EF

DEFAULT FORWARDING (DF)

![image](https://github.com/psaumur/CCNA/assets/106411237/26f6bc76-6b33-40f0-9327-022b4816d280)

- Used for BEST EFFORT TRAFFIC
- The DSCP marking for DF is 0

EXPEDITED FORWARDING (EF)

![image](https://github.com/psaumur/CCNA/assets/106411237/12cf77c0-f139-494c-ab8b-d765a73a92f4)

- EF is used for TRAFFIC that requires Low Loss / Latency / Jitter
- The DSCP marking for EF is 46

---

ASSURED FORWARDING (AF)

- Defines FOUR TRAFFIC CLASSES
- ALL PACKETS in a CLASS have the same PRIORITY
- Within each CLASS, there are THREE LEVELS of DROP PRECEDENCE
    - HIGHER DROP PRECEDENCE = More likely to DROP the PACKET during CONGESTION
    

![image](https://github.com/psaumur/CCNA/assets/106411237/407ab29c-678d-4a38-8e8e-2a6f904b4d94)

EXAMPLES:

![image](https://github.com/psaumur/CCNA/assets/106411237/d6b2dac7-fefc-409b-8136-f34df165dd23)

![image](https://github.com/psaumur/CCNA/assets/106411237/6543afb5-9aba-4d91-9d61-233c2c67958d)

![image](https://github.com/psaumur/CCNA/assets/106411237/fae89ed7-7229-4632-b3de-5415a36ad267)

![image](https://github.com/psaumur/CCNA/assets/106411237/a7440ed0-70d8-48c2-b83d-dcb4e169fade)

![image](https://github.com/psaumur/CCNA/assets/106411237/0d2d9ba8-fecc-47a8-9cee-02ae5a7a30e9)

![image](https://github.com/psaumur/CCNA/assets/106411237/05fa1552-e305-4e2d-b6aa-db0c8cbed3f7)

![image](https://github.com/psaumur/CCNA/assets/106411237/be10edd7-a4e3-4df6-a94f-b9e1b1c9e304)

- AF41 gets the BEST TREATMENT (Highest Priority / Lowest Drop)
- AF13 gets the WORST TREATMENT (Lowest Priority / Highest Drop)

---

CLASS SELECTOR (CS)

- Defines EIGHT DSCP values for backward compatibility with IPP
- The THREE BITS that were added for DSCP are set to 0, and the original IPP bits are used to make 8 values

![image](https://github.com/psaumur/CCNA/assets/106411237/d7619e44-1ffd-4613-bbad-f2ff19ff6d2a)

---

RFC 4954

- RFC 4954 was developed with help of Cisco to bring ALL of these VALUES together and STANDARDIZE their use

- The RFC offers MANY specific recommendations, but here are a few KEY ones:
    - VOICE TRAFFIC : EF
    - INTERACTIVE VIDEO : AF4x
    - STREAMING VIDEO : AF3x
    - HIGH PRIORITY DATA : AF2x
    - BEST EFFORT : DF

---

TRUST BOUNDARIES

- The TRUST BOUNDARY of a NETWORK defines where the DEVICE TRUST / DON’T TRUST the QoS MARKINGS of received messages
- If the MARKINGS are TRUSTED:
    - DEVICE will forward the message without changing the MARKINGS
- If the MARKINGS are NOT TRUSTED:
    - DEVICE will change the MARKINGS according to configured POLICY

![image](https://github.com/psaumur/CCNA/assets/106411237/cdcdc302-9dbe-4dd8-9184-72d1f501bc1a)

- If an IP PHONE is connected to the SWITCH PORT, it is RECOMMENDED to move the TRUST BOUNDARY to the IP PHONES
- This is done via CONFIGURATION on the SWITCH PORT connected to the IP PHONE
- If a user MARKS their PC’s TRAFFIC with a HIGH PRIORITY, the MARKING will be CHANGED (not trusted)

![image](https://github.com/psaumur/CCNA/assets/106411237/606ad681-fad4-4f23-96bf-bd7dde91eaf4)

---

QUEUING / CONGESTION MANAGEMENT

- When a NETWORK DEVICE receives TRAFFIC at a FASTER PACE than it can FORWARD out of the appropriate INTERACE, PACKETS are placed in that INTERFACE’S QUEUE as they wait to be FORWARDED
- When a QUEUE becomes FULL, PACKETS that don’t FIT in the QUEUE are dropped (Tail Drop)
- RED and WRED DROP PACKETS early to avoid TAIL DROP

![image](https://github.com/psaumur/CCNA/assets/106411237/5dbfd417-097c-4107-a5e1-b5476f423b15)

- An essential part of QoS is the use of MULTIPLE QUEUES
    - This is where CLASSIFICATION plays a role.
    - DEVICE can match TRAFFIC based on various factors (like DSCP MARKINGS in the IP HEADER) and then place it in the appropriate QUEUE

- HOWEVER, the DEVICE is only able to forward one FRAME out of an INTERFACE at once SO a *SCHEDULER*, is used to decide which QUEUE TRAFFIC is FORWARDED from the next
    - *PRIORITZATION* allows the SCHEDULER to give certain QUEUES more PRIORITY than others

![image](https://github.com/psaumur/CCNA/assets/106411237/56bfe184-5bdf-4b8f-8851-756766456bf9)

- A COMMON scheduling method is *WEIGHTED ROUND-ROBIN*
    - ROUND-ROBIN:
        - PACKETS taken from each QUEUE in order, cyclically
    - WEIGHTED:
        - More DATA taken from HIGH PRORITY QUEUES each time the SCHEDULER reaches that QUEUE

---

- CBWFQ (CLASS BASED WEIGHED FAIR QUEUING)
    - Popular method of SCHEDULING
    - Uses WEIGHTED ROUND-ROBIN SCHEDULER while guaranteeing each QUEUE a certain PERCENTAGE of the INTERFACE’S bandwidth during CONGESTION
    

![image](https://github.com/psaumur/CCNA/assets/106411237/eee24cef-c67a-42de-9fa0-9351cab56354)

- ROUND-ROBIN SCHEDULING is NOT IDEAL for VOICE / VIDEO TRAFFIC
    - Even if VOICE / VIDEO TRAFFIC receives a guaranteed MINIMUM amount of BANDWIDTH, ROUND-ROBIN can add DELAY and JITTER because even the HIGH PRIORITY QUEUES have to wait their turn in the SCHEDULER

---

- LLQ (LOW LATENCY QUEUING)
    - Designates ONE (or more) QUEUES as *strict priority queues*
    - This means that if there is TRAFFIC in the QUEUE, the SCHEDULER will ALWAYS take the next PACKET from that QUEUE until it is EMPTY
    - This is VERY EFFECTIVE for reducing the DELAY and JITTER of VOICE / VIDEO TRAFFIC
    - HOWEVER, LLQ has a DOWNSIDE of potentially starving other QUEUES if there is always TRAFFIC in the DESIGNATED *STRICT PRIORITY QUEUE*
        - POLICING can control the AMOUNT of TRAFFIC allowed in the *STRICT PRIORITY QUEUE* so that it can’t take all of the link’s BANDWIDTH
    

![image](https://github.com/psaumur/CCNA/assets/106411237/2b544243-3a2e-4721-bf1f-4636ec4085a7)

 

---

SHAPING / POLICING

- TRAFFIC SHAPING and POLICING are both used to control the RATE of TRAFFIC
- SHAPING
    - Buffers TRAFFIC in a QUEUE if the TRAFFIC RATE goes over the CONFIGURED RATE

- POLICING
    - DROPS TRAFFIC if the TRAFFIC RATE goes over the CONFIGURED RATE
        - POLICING also has the option of RE-MARKING the TRAFFIC, instead of DROPPING
    - “BURST” TRAFFIC over the CONFIGURED RATE is allowed for a short period of time
    - This accommodates DATA APPLICATIONS which typically are “bursty” in nature (ie: not constant stream)
    - The amount of BURST TRAFFIC allowed is configurable
    
- In BOTH cases, CLASSIFICATION can be used to ALLOW for different RATES for different KINDS of TRAFFIC
- WHY would you want to LIMIT the RATE that TRAFFIC is SENT / RECEIVED ?

![image](https://github.com/psaumur/CCNA/assets/106411237/09771d78-4570-4300-97e1-adba77fe28b4)

# 48. SECURITY FUNDAMENTALS

KEY SECURITY CONCEPTS

WHY SECURITY?

What is the purpose / goal of SECURITY in an ENTERPRISE ?

- The principles of the CIA TRIAD form the FOUNDATION of SECURITY:
    - CONFIDENTIALITY
        - Only AUTHORIZED USERS should be able to ACCESS DATA
        - Some INFORMATION / DATA is PUBLIC and can be accessed by ANYONE
        - Some INFORMATION / DATA is SECRET and should be only be accessed by SPECIFIC people
    - INTEGRITY
        - DATA should not be tampered with (modified) by unauthorized USERS
        - DATA should be CORRECT and AUTHENTIC
    - AVAILABILITY
        - The NETWORK / SECURITY should be OPERATIONAL and ACCESSIBLE to AUTHORIZED USERS

ATTACKERS can threaten the CONFIDENTIALITY, INTEGRITY, and AVAILBILITY of an enterprise’s SYSTEMS and INFORMATION

---

VULNERABILITY, EXPLOIT, THREAT, MITIGATION

- A VULNERABILITY is any potential weakness that can compromise the CIA of a SYSTEM / INFO
    - A potential weakness isn’t a problem in its own
- AN EXPLOIT is something that can potentially be used to exploit the vulnerability
    - Something than can *potentially* be used as an exploit isn’t a problem on it’s own.

- A THREAT is the potential of a VULNERABILITY to be EXPLOITED
    - A hacker EXPLOITING a VULNERABILITY in your system is a THREAT

- A MITIGATION TECHNIQUE is something that can protect against threats
    - Should be implemented everywhere a VULNERABILITY can be EXPLOITED:
        - Client Devices
        - Servers, Switches, Routers, Firewalls
        - etc.

<aside>
💡 NO SYSTEM IS PERFECTLY SECURE!

</aside>

---

COMMON ATTACKS

- DoS (Denial of Service) Attacks
- Spoofing Attacks
- Reflection / Amplification Attacks
- Man-in-the-Middle Attacks
- Reconnaissance Attacks
- Malware
- Social Engineering Attacks
- Password-Related Attacks

DoS (Denial of Service) Attacks

- DoS attacks threaten the AVAILABILITY of the SYSTEM
- One common DoS attack is the TCP SYN Flood
    - TCP Three-Way Handshake : SYN | SYN-ACK | ACK
    - The ATTACKER sends countless TCP SYN messages to the TARGET
    - The TARGET sends a SYN-ACK message in response to each SYN it receives
    - The ATTACKER never replies with the final ACK of the TCP Three-Way Handshake
    - The incomplete connections fill up the TARGET’S TCP connection table
    - The ATTACKER continues sending SYN messages
    - The TARGET is no longer able to make legitimate TCP connections

![image](https://github.com/psaumur/CCNA/assets/106411237/5b04eea4-c53a-48b7-9683-952c9b27c9db)

- In a DDoS (Distributed Denial of Service) Attack, the ATTACKER infects many computers with MALWARE and uses them to initiate a Denial-of-Service Attack.
- This group of infected computers is called a BOTNET

Example : A TCP SYN Flood Attack

![image](https://github.com/psaumur/CCNA/assets/106411237/fc394c8d-33f4-4fd4-84a0-3e49caa9c158)

---

SPOOFING ATTACKS

- To SPOOF an ADDRESS is to use a FAKE SOURCE ADDRESS (IP or MAC)
- Numerous attacks involve spoofing; it’s not a SINGLE kind of attack
- An example is a DHCP EXHAUSTION attack
- An ATTACKER uses spoofed MAC ADDRESSES to flood DHCP Discover messages
- The TARGET server’s DHCP POOL becomes full, resulting in a Denial-of-Service to other DEVICES

![image](https://github.com/psaumur/CCNA/assets/106411237/c539c50b-1be0-42f9-8ce3-fbeb47ea2034)

---

REFLECTION / AMPLIFICATION ATTACKS

- In a REFLECTION attack, the ATTACKER sends traffic to a *reflector*, and spoofs the SOURCE of the PACKET using the TARGET’S IP ADDRESS
- The *reflector* (ie: a DNS Server) sends the reply to the TARGET’S IP ADDRESS
- If the amount of traffic sent to the TARGET is large enough, this can result in a Denial-of-Service

- A REFLECTION attack becomes an AMPLIFICATION attack when the amount of traffic sent by the ATTACKER is small but it triggers a LARGE amount of traffic to be sent from the *reflector* to the TARGET

![image](https://github.com/psaumur/CCNA/assets/106411237/34ca977d-9884-4aeb-b99a-9f3677ba17fa)

---

MAN-IN-THE-MIDDLE ATTACKS

- In a MAN-IN-THE-MIDDLE attack, the ATTACKER places himself between the SOURCE and DESTINATION to eavesdrop on communications, or to modify traffic before it reaches the DESTINATION
- A common example is ARP SPOOFING, also known as ARP POISONING
- A HOST sends an ARP REQUEST, asking for the MAC ADDRESS of another DEVICE
- The TARGET of the request sends an ARP REPLY, informing the requester of it’s MAC ADDRESS
- The ATTACKER waits and sends another ARP REPLY after it’s legitimate replier

![image](https://github.com/psaumur/CCNA/assets/106411237/86cee6cd-845a-4732-bfec-4cfe18101322)

- In PC1’s ARP table, the entry for 10.0.0.1 will have the ATTACKER’S MAC ADDRESS
- When PC1 tries to send traffic to SRV1, it will be forwarded to the ATTACKER instead
- The ATTACKER can inspect the messages, and then forward them on to SRV1
- The ATTACKER can also modify the messages before forwarding them to SRV1
- This compromises the CONFIDENTIALITY and INTEGRITY of communication between PC1 and SRV1

![image](https://github.com/psaumur/CCNA/assets/106411237/07ebfebd-0686-436a-8990-853e3fee4377)

---

RECONNAISSANCE ATTACKS

- RECONNAISSANCE ATTACKS are not attacks themselves but they are used to gather information about a TARGET which can be used for a future attack
- This is often publicly available information
- IE: nslookup to learn the IP ADDRESS of a site

![image](https://github.com/psaumur/CCNA/assets/106411237/6e63b09d-a768-4cb3-ac06-87ad41d45c38)

- Or a WHOIS query to learn email addresses, phone numbers, physical addresses, etc.

https://lookup.icann.org/lookup

---

MALWARE

- MALWARE (MALICIOUS SOFTWARE) refers to a variety of harmful programs that can infect a computer
- VIRUSES infect other software (a ‘host program’)
    - The VIRUS spreads as the software is shared by USERS. Typically, they CORRUPT or MODIFY files on the TARGET computer
- WORMS do not require a host program. They are standalone malware and they are able to spread on their own, without user interaction. They spread of WORMS can congest the NETWORK but the ‘payload’ of a WORM can cause additional harm to TARGET DEVICES

- TROJAN HORSES are harmful software that is disguised as LEGITIMATE software. They are spread through user interaction such as opening email attachments, downloading a file from the Internet.

The above MALWARE types can exploit various VULNERABILITIES to threaten any of the CIA of a TARGET DEVICE

** There are MANY types of MALWARE

---

SOCIAL ENGINEERING ATTACKS

- SOCIAL ENGINEERING ATTACKS target the most vulnerable part of ANY system - PEOPLE!
- They involve psychological manipulation to make the TARGET reveal confidential information or perform some action

- PHISHING typically involves fraudulent emails that appear to come from a legitimate business (Amazon, bank, credit card company, etc) and contain links to a fraudulent website that seems legitimate. Users are told to login to the fraudulent website, providing their login credentials to the attacker.
    - SPEAR PHISHING is a more targeted form of phishing, ie: aimed at employees of a certain company
    - WHALING is a phishing targeted at high-profile individuals, ie: a company president
- VISHING (Voice Phishing) is phishing performed over a phone

- SMISHING (SMS Phishing) is phishing using SMS text messages

- WATERING HOLE attacks compromise sites that the TARGET victim frequently visits. If a malicious link is placed on a website the TARGET trusts, they might not hesitate to click it
- TAILGATING attack involves entering restricted, secured areas by simply walking in behind an authorized person as they enter. Often the TARGET will hold the door open for the ATTACKER to be polite, assuming the ATTACKER is also authorized to enter.

---

PASSWORD-RELATED ATTACKS

- Most systems use a USERNAME / PASSWORD combination to AUTHENTICATE users
- The USERNAME is often simple / easy to guess (for example the user’s email address) and the strength and secrecy of the password is relied on to provide the necessary security
- ATTACKERS can learn a user’s passwords via multiple methods:
    - Guessing
    - DICTIONARY ATTACK :
        - A program runs through a ‘dictionary’ or list of common words / passwords to find the TARGET’S password
    - BRUTE FORCE ATTACK :
        - A program tries every possible combination of letters, numbers, and special characters to find the TARGET’S password

- STRONG PASSWORDS should contain:
    - At LEAST 8 characters (preferably more)
    - A mixture of UPPERCASE and LOWERCASE letters
    - A mixture of LETTERS and NUMBERS
    - One of more SPECIAL CHARACTERS (# @ ! ? etc.)
    - Should be CHANGED REGULARLY

---

PASSWORDS / MULTI-FACTOR AUTHENTICATION (MFA)

- MULTI-FACTOR AUTHENTICATION involves providing more than just a USERNAME / PASSWORD to prove your identity
- It usually involves providing TWO of the following ( = Two-Factor Authentication) :
    - SOMETHING YOU KNOW
        - A USERNAME / PASSWORD combination, a PIN, etc.
        
    - SOMETHING YOU HAVE
        - Pressing a notification that appears on your phone, a badge that is scanned, etc.
    
    - SOMETHING YOU ARE
        - Biometrics such as a face scan, palm scan, fingerprint scan, retina scan, etc.

- Requiring multiple factors of AUTHENTICATION greatly increases the security. Even if the ATTACKER learns the TARGET’S PASSWORD (SOMETHING YOU KNOW), they won’t be able to login to the TARGET’S account

---

DIGITAL CERTIFICATES

- DIGITAL CERTIFICATES are another form of AUTHENTICATION used to prove the identity of the holder of the certificate
- They are used for websites to verify that the website being accessed is legitimate
- Entities that want a certificate to prove their identity send a CSR (CERTIFICATE SIGNING REQUEST) to a CA (CERTIFICATE AUTHORITY) which will generate and sign the certificate

---

CONTROLLING AND MONITORING USERS WITH AAA

- AAA (Triple-A) stands for AUTHENTICATION, AUTHORIZATION, and ACCOUNTING
- It is a framework for controlling and monitor users of a computer system (ie: a network)

- AUTHENTICATION
    - Process of verifying a user’s identity
    - Logging in = AUTHENTICATION
- AUTHORIZATION
    - Process of granting the user the appropriate access and permissions
    - Granting the user access to some files / services, restricting access to other files / services = AUTHORIZATION

- ACCOUNTING
    - Process of recording the user’s activities on the system
    - Logging when a user makes a change to a file = ACCOUNTING

- Enterprises typically use a AAA server to provide AAA services
    - ISE (Identity Services Engine) is Cisco’s AAA server

- AAA Servers usually support the following TWO AAA Protocols:
    - RADIUS :  Open Standard Protocol
        - Uses UDP PORTS 1812 and 1813
        
    - TACACS+ : Cisco Proprietary Protocol
        - Uses TCP PORT 49

<aside>
💡 FOR THE CCNA, KNOW THE DIFFERENCES BETWEEN AUTHENTICATION, AUTHORIZATION, and ACCOUNTING

</aside>

---

SECURITY PROGRAM ELEMENTS

- USER AWARENESS PROGRAMS are designed to make employees aware of potential security threats and risks
- USER TRAINING PROGRAMS are formal than USER AWARENESS PROGRAMS
- PHYSICAL ACCESS CONTROL protect equipment and data from potential attackers by only allowing authorized users into the protected areas such as NETWORK CLOSETS or DATA CENTER FLOORS

# 49. PORT SECURITY

INTRO TO PORT SECURITY

- PORT SECURITY is a security feature of Cisco SWITCHES
- It allows you to control WHICH SOURCE MAC ADDRESS(ES) are allowed to enter the SWITCHPORT
- If an unauthorized SOURCE MAC ADDRESS enters the PORT, an ACTION will be TAKEN
    - The DEFAULT action is to place the INTERFACE in an “err-disabled” state

![image](https://github.com/psaumur/CCNA/assets/106411237/92f4ce9b-8fb4-4d57-b200-f41c7d5236ee)

- When you enable PORT SECURITY on an INTERFACE with the DEFAULT settings, one MAC ADDRESS is allowed
    - You can configure the ALLOWED MAC ADDRESS manually
    - If you DO NOT configure it manually, the SWITCH will allow the first SOURCE MAC ADDRESS that enters the INTERFACE
- You can CHANGE the MAXIMUM number of MAC ADDRESSES allowed
- A COMBINATION of manually configured MAC ADDRESSES and DYNAMICALLY LEARNED ADDRESSES is possible

![image](https://github.com/psaumur/CCNA/assets/106411237/0b6e8053-6819-4e02-ae28-4699a5c9c92d)

---

WHY USE PORT SECURITY?

- PORT SECURITY allows NETWORK admins to control which DEVICES are allowed to access the NETWORK
- However, MAC ADDRESS SPOOFING is a simple task
    - It is easy to configure a DEVICE to send FRAMES with a different SOURCE MAC ADDRESS
- Rather than manually specifying the MAC ADDRESSES allowed on each PORT, PORT SECURITY’S ability to limit the number of MAC ADDRESSES allowed on an INTERFACE is more useful
- Think of the DHCP STARVATION ATTACK (DAY 48 LAB video)
    - The ATTACKER spoofed thousands of fake MAC ADDRESSES
    - The DHCP SERVER assigned IP ADDRESSES to these fake MAC ADDRESSES, exhausting the DHCP POOL
    - The SWITCH’S MAC ADDRESS table can also become full due to such an attack
- Limiting the NUMBER of MAC ADDRESSES on an INTERFACE can protect against those attacks

ENABLING PORT SECURITY

![image](https://github.com/psaumur/CCNA/assets/106411237/b00765c2-f3a1-45be-8ed4-0a8dab68e43e)

`show port-security interface`

![image](https://github.com/psaumur/CCNA/assets/106411237/787959b1-ffad-451d-ac65-11ea9a99db2d)

![image](https://github.com/psaumur/CCNA/assets/106411237/9a6dd39d-130e-411b-be46-ecfe93420813)

![image](https://github.com/psaumur/CCNA/assets/106411237/f071f447-a6ef-4ee6-8a40-2bde94030993)

RE-ENABLING AN INTERFACE (MANUALLY)

![image](https://github.com/psaumur/CCNA/assets/106411237/706736d4-ee7c-42b2-b424-6cc30eb50905)

RE-ENABLING AN INTERFACE (ERR-DISABLE RECOVERY)

![image](https://github.com/psaumur/CCNA/assets/106411237/6eb0d808-a989-4261-9b39-1ac9e1bf1460)

![image](https://github.com/psaumur/CCNA/assets/106411237/41d54ef0-7391-473e-9b51-87f44b9e3f3c)

---

VIOLATION MODES

- There are THREE DIFFERENT VIOLATION MODES that determine what the SWITCH will do if an unauthorized FRAME enters an INTERFACE configured with PORT SECURITY
    - SHUTDOWN
        - Effectively shuts down the PORT by placing it in an ‘err-disabled` state
        - Generates a SYSLOG and / or SNMP message when the INTERFACE is ‘disabled’
        - The VIOLATION counter is set to 1 when the INTERFACE is ‘disabled’
    - RESTRICT
        - The SWITCH discards traffic from unauthorized MAC ADDRESSES
        - The INTERFACE is NOT disabled
        - Generates a SYSLOG and / or SNMP message each time an unauthorized MAC is detected
        - The VIOLATION counter is incremented by 1 for each unauthorized FRAME
    
    - PROTECT
        - The SWITCH discards traffic from unauthorized MAC ADDRESSES
        - The INTERFACE is NOT disabled
        - It does NOT generate a SYSLOG / SNMP message for unauthorized traffic
        - It does NOT increment the VIOLATION counter
    
---

VIOLATION MODE - RESTRICT

![image](https://github.com/psaumur/CCNA/assets/106411237/819f00b9-9694-442d-8459-8018f4277e45)


VIOLATION MODE - PROTECT

![image](https://github.com/psaumur/CCNA/assets/106411237/20d17f97-056e-4e76-8566-bb49c10bb9e1)

---

SECURE MAC ADDRESS AGING

![image](https://github.com/psaumur/CCNA/assets/106411237/4454fedf-f942-4b0d-9b6f-074765de653d)

- By DEFAULT, SECURE MAC ADDRESSES will not ‘age out’ (Aging Time : 0 mins)
    - Can be configured with `switchport port-security aging time *minutes*`

- The DEFAULT Aging Type is ABSOLUTE
    - ABSOLUTE
        - After the SECURE MAC ADDRESS is learned, the AGING TIMER starts and the MAC is removed after the TIMER expires, even if the SWITCH continues receiving FRAMES from that SOURCE MAC ADDRESS.
    - INACTIVITY
        - After the SECURE MAC ADDRESS is learned, the AGING TIMER starts but is RESET every time a FRAME from that SOURCE MAC ADDRESS is received on the INTERFACE
            - Aging type is configured with:  `switchport port-security aging type {absolute | inactivity}`
- Secure Static MAC AGING (address configured with `switchport port-security mac-address x.x.x`) is DISABLED by DEFAULT

![image](https://github.com/psaumur/CCNA/assets/106411237/93f11517-9d97-4e52-89ad-a0e590bca702)

---

STICKY SECURE MAC ADDRESSES 

- ‘STICKY’ SECURE MAC ADDRESS learning can be enabled with the following command:
    - `SW(config-if)# switchport port-security mac-address sticky`

- When enabled, dynamically-learned SECURE MAC ADDRESSES will be added to the running configuration, like this:
    - `switchport port-security mac-address sticky *mac-address*`

- The ‘STICKY’ SECURE MAC ADDRESSES will NEVER age out
    - You need to SAVE the `running-config` to `startup-config` to make them TRULY permanent (or else they will not be kept if the SWITCH restarts)
- When you issue the `switchport port-security mac-address sticky` command, all current dynamically-learned secure MAC addresses will be converted to STICKY SECURE MAC ADDRESSES
- If you issue the `no switchport port-security mac-address sticky` command, all current STICKY SECURE MAC ADDRESSES will be converted to regular dynamically-learned SECURE MAC ADDRESSES

![image](https://github.com/psaumur/CCNA/assets/106411237/10d591f9-334c-4e3b-889e-16030c36c445)

---

MAC ADDRESS TABLE

- SECURE MAC ADDRESSES will be added to the MAC ADDRESS TABLE like any other MAC ADDRESS
    - STICKY and STATIC SECURE MAC ADDRESSES will have a type of STATIC
    - Dynamically-Learned SECURE MAC ADDRESSES will have a type of DYNAMIC
    - You can view all SECURE MAC ADDRESSES with `show mac address-table secure`
    

![image](https://github.com/psaumur/CCNA/assets/106411237/c9123729-541c-4363-ba19-d8e49f75c6c5)

---

COMMAND REVIEW

![image](https://github.com/psaumur/CCNA/assets/106411237/716ce91d-d1bb-4f12-a8fd-226b65f22569)

# 50. DHCP SNOOPING (LAYER 2)

WHAT IS DHCP SNOOPING?

- DHCP SNOOPING is a security feature of SWITCHES that is used to filter DHCP messages received on UNTRUSTED PORTS
- DHCP SNOOPING only filters DHCP MESSAGES.
    - Non-DHCP MESSAGES are not affected
- All PORTS are UNTRUSTED, by DEFAULT
    - Usually UPLINK PORTS are configured as TRUSTED PORTS, and DOWNLINK PORTS remain UNTRUSTED
    

![image](https://github.com/psaumur/CCNA/assets/106411237/9ed71d09-d94c-4fc9-ad87-1b31acfdd132)

![image](https://github.com/psaumur/CCNA/assets/106411237/9d7d23a6-9d54-4234-a07e-a5caea136c94)

---

ATTACKS ON DHCP

DHCP STARVATION

- An example of a DHCP-based ATTACK is a DHCP STARVATION ATTACK
- An ATTACKER uses spoofed MAC ADDRESSES to flood DHCP DISCOVER messages
- The TARGET server’s DHCP POOL becomes full, resulting in a DoS to other DEVICES

![image](https://github.com/psaumur/CCNA/assets/106411237/33dfbb8b-2b78-4700-b4ab-0dd95fc03eed)

DHCP POISONING (Man-in-the-Middle)

- Similar to ARP POISONING, DHCP POISONING can be used to perform a Man-in-the-Middle ATTACK
- A *spurious DHCP SERVER* replies to CLIENTS’ DHCP Discover messages and assigns them IP ADDRESSES but makes the CLIENTS use the *spurious SERVER’S IP* as a DEFAULT GATEWAY

** CLIENTS usually accept the first DHCP OFFER message they receive

- This will cause the CLIENT to send TRAFFIC to the ATTACKER instead of the legitimate DEFAULT GATEWAY
- The ATTACKER can then examine / modify the TRAFFIC before forwarding it to the legitimate DEFAULT GATEWAY

![image](https://github.com/psaumur/CCNA/assets/106411237/d0cd7a5c-9ff4-4ab7-bec6-4edec4ea2646)

![image](https://github.com/psaumur/CCNA/assets/106411237/1573bcb7-6fa8-46d7-8cb8-46e30bac559d)

---

DHCP MESSAGES

- When DHCP SNOOPING filters messages, it differentiates between DHCP SERVER messages and DHCP CLIENT messages

- Messages sent by DHCP SERVERS:
    - OFFER
    - ACK
    - NAK = Opposite of ACK - used to DECLINE a CLIENT’S REQUEST
- Messages sent by DHCP CLIENTS:
    - DISCOVER
    - REQUEST
    - RELEASE = Used to tell the SERVER that the CLIENT no longer needs its IP ADDRESS
    - DECLINE = Used to DECLINE the IP ADDRESS offered by a DHCP SERVER

---

HOW DOES IT WORK?

- If a DHCP MESSAGE is received on a TRUSTED PORT, forward it as normal without inspection
- If a DHCP MESSAGE is received on an UNTRUSTED PORT, inspect it and act as follows:
    - If it is a DHCP SERVER message, discard it
    - If it as a DHCP CLIENT message, perform the following checks:
        - DISCOVER / REQUEST messages :
            - Check if the FRAME’S SOURCE MAC ADDRESS and the DHCP MESSAGE’S CHADDR FIELDS match.
                - MATCH = FORWARD
                - MISMATCH = DISCARD
        - RELEASE / DECLINE messages:
            - Check if the PACKET’S SOURCE IP ADDRESS and the receiving INTERFACE match the entry in the *DHCP SNOOPING BINDING TABLE*
                - MATCH = FORWARD
                - MISMATCH = DISCARD
    
- When a CLIENT successfully leases an IP ADDRESS from a SERVER, create a new entry in the *DHCP SNOOPING BINDING TABLE*

---

DHCP SNOOPING CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/729466dc-9432-47d2-8799-652fa064b058)

SWITCH 2’s CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/8d6cacb8-ffd8-4cf0-bd96-fe9978377989)

SWITCH 1’s CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/bb11e4fd-a340-4dd3-a6f5-3cd280fc5a13)

DHCP SNOOPING RATE-LIMITING

- DHCP SNOOPING can limit the RATE at which DHCP messages are allowed to enter an INTERFACE
- If the RATE of DHCP messages crosses the configured LIMIT, the INTERFACE is `err-disabled`
- Like with PORT SECURITY, the interface can be manually re-enabled, or automatically re-enabled with `errdisable recovery`

![image](https://github.com/psaumur/CCNA/assets/106411237/6586df19-5a58-4ca3-a316-bd0aeb2ce67c)

- You wouldn’t set the limit rate to 1 since it’s so low, it would shut the port immediately but this shows how RATE-LIMITING works

`errdisable recovery cause dhcp-rate-limit`

![image](https://github.com/psaumur/CCNA/assets/106411237/83c324aa-baa0-4ae1-82ac-157e503e048a)

DHCP OPTION 82 (INFORMATION OPTION)

- OPTION 82, also known as a ‘DHCP RELAY AGENT INFOMRATION OPTION’ is one of MANY DHCP OPTIONS
- It provides additional information about which DHCP RELAY AGENT received the CLIENT’S message, on which INTERFACE, in which VLAN, etc.
- DHCP RELAY AGENTS can add OPTION 82 to message they forward to the remote DHCP SERVER
- With DHCP SNOOPING enabled, by default Cisco SWITCHES will add OPTION 82 to DHCP messages they receive from CLIENTS, even if the SWITCH isn’t acting as a DHCP RELAY AGENT
- By DEFAULT, Cisco SWITCHES will drop DHCP MESSAGES with OPTION 82 that are received on an UNTRUSTED PORT

![image](https://github.com/psaumur/CCNA/assets/106411237/2efc6edd-21fd-4c1a-bb11-9c1f761e1d32)

THIS command disables OPTION 82 for SW1 but NOT SW2 

![image](https://github.com/psaumur/CCNA/assets/106411237/84f1c3f2-9ad1-4367-97f3-95dab053b30c)

TRAFFIC gets passed to R1 and is DROPPED because of “inconsistent relay information” (packet contains OPTION 82 but wasn’t dropped by SW2)

![image](https://github.com/psaumur/CCNA/assets/106411237/5c4b547e-c588-4d62-8098-76902199a131)

By ENABLING OPTION 82 on both SWITCHES…

![image](https://github.com/psaumur/CCNA/assets/106411237/dda50cf6-ae86-47ec-9b4f-104669697f64)

PC1’s DHCP DISCOVER message gets passed, through SW1 and SW2, to R1.
R1 responds with an DHCP OFFER message, as normal

![image](https://github.com/psaumur/CCNA/assets/106411237/7e59cc5a-bf8e-482d-848d-5bfa0540c74b)

---

COMMAND SUMMARY

![image](https://github.com/psaumur/CCNA/assets/106411237/308e32fa-52bd-4ee4-9356-f14e65416e17)

# 51. DYNAMIC ARP INSPECTION

WHAT IS DYNAMIC ARP INSPECTION (DAI) ?

ARP REVIEW

- ARP is used to learn the MAC ADDRESS of another DEVICE with a known IP ADDRESS
    - For example, a PC will use ARP to learn the MAC ADDRESS of its DEFAULT GATEWAY to communicate with external NETWORKS
- Typically, it is a TWO MESSAGE EXCHANGE :  ARP REQUEST and ARP REPLY

GRATUITOUS ARP

- A GRATUITOUS ARP MESSAGE is an ARP REPLY that is sent without receiving an ARP REQUEST
- It is SENT to the BROADCAST MAC ADDRESS
- It allows other DEVICES to learn the MAC ADDRESS of the sending DEVICE without having to send ARP REQUESTS.
- Some DEVICES automatically send GARP MESSAGES when an INTERFACE is enabled, IP ADDRESS is changed, MAC address is changed, etc.

DYNAMIC ARP INSPECTION

- DAI is a SECURITY FEATURE of SWITCHES that is used to filter ARP MESSAGES received on  *UNTRUSTED PORTS*
- DAI only filters ARP MESSAGES. Non-ARP MESSAGES are NOT affected
- All PORTS are *UNTRUSTED*, by DEFAULT
    - Typically, all PORTS connected to other NETWORK DEVICES (SWITCHES, ROUTERS) should be configured as TRUSTED, while INTERFACES connected to END HOSTS should remain UNTRUSTED

![image](https://github.com/psaumur/CCNA/assets/106411237/02da32ef-654c-4755-abcd-ea8230df4029)

![image](https://github.com/psaumur/CCNA/assets/106411237/29744383-746e-47be-8220-ba1a641a7a11)

![image](https://github.com/psaumur/CCNA/assets/106411237/6848c2b5-e866-4023-9ad9-c18f63aa6bb5)

---

ARP POISONING (MAN IN THE MIDDLE)

- Similar to DHCP POISONING, ARP POISONING involved an ATTACKER manipulating TARGET’S ARP TABLES so TRAFFIC is sent to the ATTACKER
- To do this, the ATTACKER can send GRATUITOUS ARP MESSAGES using another DEVICE’S IP ADDRESS
- Other DEVICES in the NETWORK will receive the GARP and update their ARP TABLES, causing them to send TRAFFIC to the ATTACKER instead of the legitimate DESTINATION

![image](https://github.com/psaumur/CCNA/assets/106411237/aae80c8f-2673-4c04-a206-9b646f5c1f08)

DYNAMIC ARP INSPECTION OPERATIONS

- DAI inspects the SENDER MAC and SENDER IP fields of ARP MESSAGES received on UNTRUSTED PORTS and checks that there is a matching entry in the DHCP SNOOPING BINDING TABLE
    - If there is a MATCH, the ARP MESSAGE is FORWARDED
    - If there is NO MATCH, the ARP MESSAGE is DISCARDED

![image](https://github.com/psaumur/CCNA/assets/106411237/060f3d3a-b2fd-46a1-8b3c-7a6839985c87)

- DAI doesn’t inspect messages received on TRUSTED PORTS. They are FORWARDED as normal.

- ARP ACLs can be manually configured to map IP ADDRESSES / MAC ADDRESSES for DAI to check
    - Useful for HOSTS that don’t use DHCP
    
- DAI can be configured to perform more in-depth checks also - but these are optional

- Like DHCP SNOOPING, DAI also supports RATE-LIMITING to prevent ATTACKERS from overwhelming the SWITCH with ARP MESSAGES
    - DHCP SNOOPING and DAI both require work from the SWITCH’S CPU
    - Even if the ATTACKER’S messages are BLOCKED, they can OVERLOAD the SWITCH CPU with ARP MESSAGES

---

DYNAMIC ARP INSPECTION CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/4a91bd7b-626a-4d64-b69a-308d65bbdda4)

![image](https://github.com/psaumur/CCNA/assets/106411237/774765fa-4918-4cd9-bb64-57130968c359)

Command : `show ip arp inspection interfaces`

![image](https://github.com/psaumur/CCNA/assets/106411237/e64a568e-e5c6-442b-98f7-4fe829ff7519)

DAI RATE LIMITING

![image](https://github.com/psaumur/CCNA/assets/106411237/6400e059-2c8c-4369-827d-7774fddd57eb)

DAI OPTIONAL CHECKS

![image](https://github.com/psaumur/CCNA/assets/106411237/0e6b780a-16ef-466a-bfd3-8dd2cdace4ad)

![image](https://github.com/psaumur/CCNA/assets/106411237/1f109b81-9c9b-4acd-9557-0b652ba29b8d)

![image](https://github.com/psaumur/CCNA/assets/106411237/dd78740a-4f41-43aa-8ed2-3fa574acc0f9)

ARP ACLs (Beyond Scope of CCNA)

CREATE AN ARP ACL FOR SRV1

![image](https://github.com/psaumur/CCNA/assets/106411237/cf121a75-45b2-4e2d-a35f-320e3f5491fa)

AFTER APPLYING IT TO SWITCH 2, SRV1 is able to send ARP REQUEST to R1

![image](https://github.com/psaumur/CCNA/assets/106411237/582feed0-1915-4f59-b3b9-9db37854c6e1)

Command: `show ip arp inspection`

Shows a summary of the DAI configuration and statistics

![image](https://github.com/psaumur/CCNA/assets/106411237/684e694a-5b0a-4f85-b135-b288a8c4c6ec)

---

COMMAND REVIEW

![image](https://github.com/psaumur/CCNA/assets/106411237/4cb7dc28-b09d-4a98-8d43-aca2cdf6180b)

# 52. LAN ARCHITECTURES

- You have studied various NETWORK technologies: ROUTING, SWITCHING, STP, ETHERCHANNEL, OSPF, FHRPs, SWITCH SECURITY FEATURES, etc.
    - Now, let’s look at some BASIC NETWORK DESIGN / ARCHITECTURE
- There are standard “BEST PRACTICES” for NETWORK DESIGN
    - However there are a few UNIVERSAL “CORRECT ANSWERS”
    - The answer to MOST general questions about NETWORK DESIGN is “IT DEPENDS”
- In the early stages of your NETWORKING career, you probably won’t be asked to DESIGN NETWORKS yourself
- However, to understand the NETWORKS you will be CONFIGURING and TROUBLESHOOTING, it’s important to know some BASICS of NETWORK DESIGN

---

COMMON TERMINOLOGIES

- STAR
    - When several DEVICES all connect to ONE CENTRAL DEVICE, we can draw them in a “STAR” shape like below, so this is often called a “STAR TOPOLOGY”

![image](https://github.com/psaumur/CCNA/assets/106411237/8aeb545d-3cc0-44bf-a01e-b7e5d47deaf2)

- FULL MESH
    - When each DEVICE is connected to each OTHER DEVICE

![image](https://github.com/psaumur/CCNA/assets/106411237/cb2d12af-cf17-4ffe-a637-148014d20753)

- PARTIAL MESH
    - When SOME DEVICES are connected to each other but not ALL

![image](https://github.com/psaumur/CCNA/assets/106411237/01ed7fe5-317b-45c7-8baa-0cc74e502433)

---

2-TIER AND 3-TIER LAN ARCHITECTURE

- The TWO-TIER LAN DESIGN consists of TWO Hierarchical Layers:
    - ACCESS LAYER
    - DISTRIBUTION LAYER
- Also called a “COLLAPSED CORE” DESIGN because it omits a layer that is found in the THREE TIER DESIGN : THE CORE LAYER
- ACCESS LAYER
    - The LAYER that END HOSTS connect to (PCs, Printers, Cameras, etc)
    - Typically, ACCESS LAYER SWITCHES have lots of PORTS for END HOSTS to connect to
    - QoS MARKING is typically done here
    - Security Services like PORT SECURITY, DAI, etc are typically performed here
    - SWITCHPORTS might be PoE-Enabled for Wireless APs, IP Phones, etc.
- DISTRIBUTION LAYER
    - Aggregates connections from the ACCESS LAYER SWITCHES
    - Typically is the border between LAYER 2 and LAYER 3
    - Connects to services such as Internet, WAN, etc
    - Sometimes called AGGREGATION LAYER

![image](https://github.com/psaumur/CCNA/assets/106411237/4592f4d8-5550-4428-923c-c805d2ca476f)

![image](https://github.com/psaumur/CCNA/assets/106411237/4fa26aec-536a-4ad8-8f39-e94dacc4cb3c)

![image](https://github.com/psaumur/CCNA/assets/106411237/72018e4f-113e-4921-8dc4-05079c590ee1)

![image](https://github.com/psaumur/CCNA/assets/106411237/c8326214-80e0-4702-a1c3-6dd2fbafb6e9)

---

THREE-TIER CAMPUS LAN DESIGN

- In large NETWORKS with many DISTRIBUTION LAYER SWITCHES (for example in separate buildings), the number of connections required between DISTRIBUTION LAYER SWITCHES grows rapidly

![image](https://github.com/psaumur/CCNA/assets/106411237/8b94c8e9-813b-40e0-bcd1-b27d73da31e8)

- To help SCALE large LAN NETWORKS, you can add a CORE LAYER.

** Cisco recommends adding a CORE LAYER if there are more than THREE DISTRIBUTION LAYERS in a single location

![image](https://github.com/psaumur/CCNA/assets/106411237/d5c1a677-38ff-425f-b91a-65a8fa37c377)

- The THREE-TIER LAN DESIGN consists of THREE HIERARCHICAL LAYERS:
    - ACCESS LAYER
    - DISTRIBUTION LAYER
    - CORE LAYER

- CORE LAYER:
    - Connects DISTRIBUTION LAYERS together in large LAN NETWORKS
    - The focus is SPEED (”FAST TRANSPORT”)
    - CPU-INTENSIVE OPERATIONS, such as SECURITY, QoS Markings / Classification, etc. should be avoided at this LAYER
    - Connections are all LAYER 3. NO SPANNING-TREE!
    - Should maintain connectivity throughout the LAN even if DEVICES FAIL
    
![image](https://github.com/psaumur/CCNA/assets/106411237/633cee0a-8952-4b27-91a3-8653bb8e353c)
    

---

SPINE-LEAF ARCHITECTURE (DATA CENTER)

- CISCO ACI ARCHITECTURE (Application Centric Infrastructure) uses this architecture
- DATA CENTERS are dedicated spaces / buildings used to STORE COMPUTER SYSTEMS such as SERVERS and NETWORK DEVICES
- Traditional DATA CENTER designs used a THREE-TIER ARCHITECTURE (ACCESS-DISTRIBUTION-CORE) like we just covered
- This worked well when most TRAFFIC in the DATA CENTER was NORTH-SOUTH

![image](https://github.com/psaumur/CCNA/assets/106411237/7e2ff784-d16f-4606-a186-c73223bf5582)

- With the precedence of VIRTUAL SERVERS, applications are often deployed in a DISTRIBUTED manner (across multiple physical SERVERS) which increases the amount of EAST-WEST TRAFFIC in the DATA CENTER
- The traditional THREE-TIER ARCHITECTURE led to bottlenecks in the BANDWIDTH as well as VARIABILITY in the SERVER-TO-SERVER latency depending on the PATH the TRAFFIC takes
- To SOLVE this, SPINE-LEAF ARCHITECTURE (also called CLOS ARCHITECTURE) has become prominent in DATA CENTERS

RULES FOR SPINE-LEAF ARCHITECTURE

- Every LEAF SWITCH is connected to every SPINE SWITCH
- Every SPINE SWITCH is connected to every LEAF SWITCH
- LEAF SWITCHES do NOT connect to other LEAF SWITCHES
- SPINE SWITCHES do NOT connect to other SPINE SWITCHES
- END HOSTS (Servers, etc) ONLY connect to LEAF SWITCHES

![image](https://github.com/psaumur/CCNA/assets/106411237/73cbe190-f589-4307-8ce4-e3de8af2f1d5)

- The PATH taken by TRAFFIC is randomly chosen to balance the TRAFFIC LOAD among the SPINE SWITCHES
- Each SERVER is separated by the same number of “HOPS” (except those connected to the same LEAF) providing CONSISTENT LATENCY for EAST-WEST TRAFFIC

---

SOHO (SMALL OFFICE / HOME OFFICE)

- SMALL OFFICE / HOME OFFICE (SOHO) refers to the office of a small company, or a small home office with few DEVICES
    - Doesn’t have to be an actual home “office”; if your home has a NETWORK connected to the INTERNET it is considered a SOHO NETWORK

- SOHO NETWORKS don’t have complex needs, so all NETWORKING functions are typically provided by a SINGLE DEVICE, often called a “HOME ROUTER” or “WIRELESS ROUTER”
- The one DEVICE can serve as a:
    - ROUTER
    - SWITCH
    - FIREWALL
    - WIRELESS ACCESS POINT
    - MODEM

![image](https://github.com/psaumur/CCNA/assets/106411237/c9edf179-f333-4fec-9e95-ee291b5eb84c)

![image](https://github.com/psaumur/CCNA/assets/106411237/7d606552-8939-41c1-ad85-13face1d27f5)

# 53.  WAN ARCHITECTURES

INTRODUCTION TO WANS

- WAN stands for WIDE AREA NETWORK
- A WAN is a NETWORK that extends over a large geographic area
- WANs are used to connect geographically separate LANs
- Although the Internet can be considered a WAN, the term “WAN” is typically used to refer to an enterprise’s private connections that connect their offices, data centers, and other sites together
- Over public/shared networks like the Internet, VPNs (Virtual Private Networks) can be used to create private WAN connections
- There have been many different WAN technologies over the years. Depending on the location, some will be available and some will not be
- Technologies which are considered “legacy” (old) in one country, might still be used in other countries

---

WAN OVER DEDICATED CONNECTION (LEASED LINE)

HUB-and-SPOKE topology

![image](https://github.com/psaumur/CCNA/assets/106411237/57575fad-883d-4999-a56d-a77fa1542976)

![image](https://github.com/psaumur/CCNA/assets/106411237/cfc23064-a133-445a-b854-e044828eca7d)

WAN CONNECTION VIA ETHERNET (FIBER)

![image](https://github.com/psaumur/CCNA/assets/106411237/022ccdbd-7ce9-41fd-9f99-9e9c6dcb9f76)

WAN OVER SHARED INFRASTRUCTURE (INTERNET VPN)

![image](https://github.com/psaumur/CCNA/assets/106411237/38eff264-7ed4-43fd-943b-47e9e1ce995e)

---

LEASED LINES

- A LEASED LINE is a dedicated physical link, typically connecting two sites
- LEASED LINES use serial connections (PPP or HDLC encapsulation)
- There are various standards that provide different speeds and different standards are available in different countries.
- Due to the HIGHER cost, HIGHER installation lead time, and SLOWER speeds of LEASED LINES, Ethernet WAN technologies are becoming MORE popular

![image](https://github.com/psaumur/CCNA/assets/106411237/77dd5503-8b29-4919-8747-6dd80eec28fa)

MPLS VPNs

- MPLS stands for “Multi Protocol Label Switching”
- Similar to the Internet, service providers’ MPLS NETWORKS are shared infrastructure because many customer enterprises connect to and share the same infrastructure to make WAN connections
- However, the “label switching” in the name of MPLS allows VPNs to be created over the MPLS infrastructure through the use of LABELS
- IMPORTANT terms:
    - CE ROUTER = Customer Edge ROUTER
    - PE ROUTER = Provider Edge ROUTER
    - P ROUTER = Provider Core ROUTER

![image](https://github.com/psaumur/CCNA/assets/106411237/166bff5b-d977-48dc-9a74-b9a523b91e1b)

- When the PE ROUTERS receive FRAMES from the CE ROUTERS, they add a LABEL to the FRAME
- These LABELS are used to make forwarding decisions within the SERVICE PROVIDER NETWORK - NOT the DESTINATION IP
- The CE ROUTERS do NOT USE MPLS, it is only used by the PE/P ROUTERS
- When using a LAYER 3 MPLS VPN, the CE and PE ROUTERS peer using OSPF, for example, to share ROUTING information

EXAMPLE: 

OFFICE A’s CE will peer with one PE

OFFICE B’s CE will peer with the other PE

OFFICE A’s CE will learn about OFFICE B’s ROUTES via this OSPF peering

OFFICE B’s CE will learn about OFFICE A’s ROUTES as well

![image](https://github.com/psaumur/CCNA/assets/106411237/2b3d8d6e-3501-4d54-a6f8-5a05c9140d24)

- When using a LAYER 2 MPLS VPN, the CE and PE ROUTERS do NOT form PEERINGS
- The SERVICE PROVIDER NETWORK is entirely *transparent* to the CE ROUTERS
- In effect, it is like the TWO CE ROUTERS are directly connected.
    - Their WAN INTERFACES will be in the SAME SUBNET
- If a ROUTING protocol is used, the TWO CE ROUTERS will peer directly with each other

CE ROUTERS connected via LAYER 2 MPLS VPN

![image](https://github.com/psaumur/CCNA/assets/106411237/b0b19dfd-e417-40ce-ac36-ce0ace8484cc)

![image](https://github.com/psaumur/CCNA/assets/106411237/cc5c9508-a2b0-4fe7-9c83-6c03e7d2d861)

---

MPLS 

- Many different technologies can be used to connect to a SERVICE PROVIDER’s MPLS NETWORK for WAN Service

![image](https://github.com/psaumur/CCNA/assets/106411237/c6e6e60d-2a96-415e-82a2-a090c38a68a3)

INTERNET CONNECTIVITY

- There are countless ways for an enterprise to connect to the INTERNET
- For example, PRIVATE WAN technologies such as LEASED LINES and MPLS VPNs can be used to connect to a SERVICE PROVIDER’s INTERNET infrastructure
- In addition, technologies such as CATV and DSL commonly used by consumers (Home Internet Access) can also be used by an enterprise
- These days for both enterprise and consumer INTERNET access, FIBER OPTIC ETHERNET connections are growing in popularity due to high speeds they provide over long distances
- Let’s briefly look at TWO INTERNET access technologies mentioned above:
    - CABLE (CATV)
    - DSL

---

DIGITAL SUBSCRIBER LINE (DSL)

- DSL provides INTERNET connectivity to customers over phone lines and can share the same phone line that is already installed in most homes
- A DSL MODEM (Modulator / Demodulator) is required to convert DATA into a format suitable to be sent over the phone lines
    - The MODEM might be a separate DEVICE or it might be incorporated in to a “HOME ROUTER”

![image](https://github.com/psaumur/CCNA/assets/106411237/a708b6b4-6de5-4a72-8c77-13f569f4c2d5)

CABLE INTERNET

- CABLE INTERNET provides INTERNET ACCESS via the same CATV (Cable Television) lines used for TV service
- Like DLS, a CABLE MODEM is required to convert DATA into a format suitable to be sent over the CATV CABLES.
    - Like a DSL MODEM, this can be a separate device or built into the HOME ROUTER

![image](https://github.com/psaumur/CCNA/assets/106411237/a33bb999-83bc-49a8-ad37-e7ca91fcb954)

---

REDUNDANT INTERNET CONNECTIONS

![image](https://github.com/psaumur/CCNA/assets/106411237/af770f82-a55c-4af5-af7b-5708b39833c4)

---

INTERNET VPNs

- PRIVATE WAN SERVICES such as LEASED LINES and MPLS provide security because each customer’s TRAFFIC is separated by using dedicated physical connections (LEASED LINE) or by MPLS TAGS
- When using the INTERNET as a WAN to connect SITES together, there is no built-in security by DEFAULT
- To provide secure communications over the Internet, VPNs (Virtual Private Networks) are used
- We will cover two kinds of Internet VPNs:
    - SITE-TO-SITE VPNS using IPSec
    - REMOTE-ACCESS VPNs using TLS

SITE-TO-SITE VPNs (IPSec)

- A “SITE-TO-SITE” VPN is a VPN between two DEVICES and is used to connect TWO SITES together over the INTERNET
- A VPN “TUNNEL” is created between the TWO DEVICES by ENCAPSULATING the original IP PACKET with a VPN HEADER and a new IP HEADER
    - When using IPSec, the original PACKET is encrypted before its ENCAPSULATED with the new HEADER

![image](https://github.com/psaumur/CCNA/assets/106411237/b17c6149-90b2-4bc7-beb7-c53698d588a0)

![image](https://github.com/psaumur/CCNA/assets/106411237/d41295a9-af54-4cd5-acc8-4b60c39c40c2)

PROCESS SUMMARY:

1) The SENDING DEVICE combines the original PACKET and SESSION KEY (ENCRYPTION KEY) and runs them through an ENCRYPTION FORMULA

2) The SENDING DEVICE encapsulates the ENCRYPTED PACKET with a VPN HEADER and a new IP HEADER

3) The SENDING DEVICE sends the NEW PACKET to the DEVICE on the other side of the TUNNEL

4) The RECEIVING DEVICE decrypts the DATA to get the original PACKET and then forwards the original PACKET to it’s DESTINATION

- In a “SITE-TO-SITE” VPN, a TUNNEL is formed only between TWO TUNNEL ENDPOINTS (for example, the TWO ROUTERS connected to the INTERNET)
- All OTHER DEVICES in each site DO NOT need to create a VPN for themselves. They can send unencrypted DATA to their site’s ROUTER, which will ENCRYPT it and FORWARD it in the TUNNEL as described above.

---

LIMITATIONS OF STANDARD IPSec

1) IPSec doesn’t support BROADCAST or MULTICAST TRAFFIC, only UNICAST.

- This means that ROUTING PROTOCOLS such as OSPF cannot be used over the TUNNELS because they rely on MULTICAST TRAFFIC
    - This can be SOLVED with “GRE over IPSec”

2) Configuring a full mesh of TUNNELS between many sites is a labor-intensive task

Let’s look at each of the above SOLUTIONS

---

GRE over IPSec

- GRE (GENERIC ROUTING ENCAPSULATION) creates TUNNELS like IPSec, however it does not ENCRYPT the original PACKET, so it is NOT SECURE
- However, it has the advantage of being able to encapsulate a WIDE variety of a LAYER 3 PROTOCOLS as well as BROADCAST and MULTICAST messages
- To get the FLEXIBILITY of GRE with the SECURITY of IPSec, “GRE over IPSec” can be used
- The original PACKET will be ENCAPSULATED by a GRE HEADER and a new IP HEADER, and then the GRE PACKET will be ENCRYPTED and ENCAPSULATED within an IPSec VPN HEADER and a NEW IP HEADER

![image](https://github.com/psaumur/CCNA/assets/106411237/09c7da0c-debe-453e-822c-b97c0b8658ef)

![image](https://github.com/psaumur/CCNA/assets/106411237/3dfd6b86-28bb-489d-931b-5cc74669c1ac)

![image](https://github.com/psaumur/CCNA/assets/106411237/939ce5af-5ffc-44da-96fc-def2ca99ecae)

---

DMVPN

- DMVPN (Dynamic Multipoint VPN) is a Cisco-Developed solution that allows ROUTERS to dynamically create a FULL MESH of IPSec TUNNELS without having to manually configure every SINGLE TUNNEL

1) CONFIGURE IPSec TUNNELS to a HUB SITE

![image](https://github.com/psaumur/CCNA/assets/106411237/00c33e7f-2b28-4a33-908d-7aceff1e4092)

2) The HUB ROUTER gives each ROUTER information about HOW to form an IPSec TUNNEL with the OTHER ROUTERS

![image](https://github.com/psaumur/CCNA/assets/106411237/7a621160-10d4-4e14-868b-3c23f6bb0a64)

DMVPN provides the configuration simplicity of HUB-AND-SPOKE (each SPOKE ROUTER only needs one TUNNEL configured) and the EFFICIENCY of DIRECT SPOKE-TO-SPOKE communication (SPOKE ROUTERS can communicate directly without TRAFFIC passing through the HUB)

---

REMOTE-ACCESS VPNs

- Whereas SITE-TO-SITE VPNs are used to make a POINT-TO-POINT connection between TWO SITES over the INTERNET, REMOTE-ACCESS VPNs are used to allow END DEVICES (PCs, Mobile Phone) to ACCESS the company’s internal resources securely over the INTERNET
- REMOTE-ACCESS VPNs typically use TLS (TRANSPORT LAYER SECURITY)
    - TLS is also what provides security for HTTPS (HTTP SECURE)
    - TLS was formerly known as SSL (Secure Socket Layer) and developed by Netscape, but it was renamed to TLS when it was standardized by the IETF
- VPN client software  (for example Cisco AnyConnect) is installed on END DEVICES (for example company-provided laptops that employees use to work from home)
- These END DEVICES then form SECURE TUNNELS to one of the company’s ROUTERS / FIREWALLS acting as a TLS SERVER
- This allows the END USERS to securely access RESOURCES on the company’s INTERNAL NETWORK without being directly connected to the company NETWORK

![image](https://github.com/psaumur/CCNA/assets/106411237/f4a77cb7-9d42-4daa-9a25-630c0fb260cf)

---

SITE-TO-SITE versus REMOTE-ACCESS VPN

- SITE-TO-SITE VPNs typically use IPSec
- REMOTE-ACCESS VPNs typically use TLS
- SITE-TO-SITE VPNs provide SERVICE to many DEVICES within the SITES they are connecting
- REMOTE-ACCESS VPNs provide SERVICE to the ONE END DEVICE the VPN CLIENT SOFTWARE is installed on

- SITE-TO-SITE VPNs are typically used to permanently connect TWO SITES over the INTERNET
- REMOTE-ACCESS VPNs are typically used to provide ON-DEMAND ACCESS for END DEVICES that want to securely ACCESS company resources while connected to a NETWORK which is not SECURE

---

LAB COMMANDS

Create the Tunnel interface

`R1(config)#int tunnel <tunnel number>`

This changes the mode to the Tunnel Interface

The exit interface for the tunnel

`tunnel source <interface>` 

IP of the Tunnel Destination Interface

`tunnel destination <destination ip address>`

Set the IP of the Source Tunnel Interface (from step 1)

`ip address <tunnel IP> <netmask>`

Configure a Default Route to the Service Provider Network

`R1(config)#ip route 0.0.0.0 0.0.0.0 <next hop interface>`

This will now bring the Tunnel Interface Administratively Up / Up

================================================

Now you need to set up the TUNNEL ROUTERS as OSPF Neighbors for the Service Provider Network so they can share routes

`R1(config)router ospf <ospf process ID>`

This switches to the OSPF Router configuration mode

`network <tunnel interface IP> <wildcard mask> area <area #>`

Since the tunnel is a single HOST, you would use 0.0.0.0 for the Wildcard Mask

`network <router gateway IP> <wildcard mask> area <area #>`

Since the router gateway is also a single HOST, you would use 0.0.0.0 for the Wildcard Mask

`passive-interface <router gateway IP interface>`

This removes the Router Gateway from broadcasting over OSPF

# 54. VIRTUALIZATION AND CLOUD: PART 1

VIRTUAL SERVERS

- Although Cisco is more known for their networking DEVICES (ROUTERS, SWITCHES, FIREWALLS), they also offer HARDWARE SERVERS such as UCS (Unified Computing System)
- The largest vendors of HARDWARE SERVERS include Dell, EMC, HPE, and IBM

---

SERVERS BEFORE VIRTUALIZATION

![image](https://github.com/psaumur/CCNA/assets/106411237/365cde17-88c6-4149-91f2-d67c79590aec)

- Before VIRTUALIZATION, there was a one-to-one relationship between a PHYSICAL SERVER and OPERATION SYSTEM
- In that OPERATING SYSTEM, apps providing SERVICES (such as a WEB SERVER, EMAIL SERVER, etc) would run
- One PHYSICAL SERVER would be used for the WEB SERVER, one for the EMAIL SERVER, one for the DATABASE SERVER, etc.
- This is inefficient for multiple reasons:
    - Each PHYSICAL SERVER is expensive and takes up space, power, etc.
    - The RESOURCES on each PHYSICAL SERVER (CPU, RAM, STORAGE, NIC) are typically under-utilized

---

VIRTUALIZATION (TYPE 1 HYPERVISOR)

![image](https://github.com/psaumur/CCNA/assets/106411237/62a40737-7451-4b38-a5bd-abd9367cbd40)

- VIRTUALIZATION allows us to break the one-to-one relationships of HARDWARE to OS, allowing multiple OS’s to run on a single PHYSICAL SERVER
- Each INSTANCE is called a VM (Virtual Machine)
- A HYPERVISOR is used to manage and allocate the HARDWARE RESOURCES (CPU, RAM, etc.) to each VM
- Another name for a HYPERVISOR is VMM (Virtual Machine Monitor)
- The type of HYPERVISOR which runs directly on top of hardware is called a TYPE 1 HYPERVISOR
    - Examples include : VMware ESXi, Microsoft Hyper-V, etc.
- TYPE 1 HYPERVISORS are also called *bare-metal hypervisors* because they run directly on the hardware (metal).
    - Another term is *native hypervisor*
- This is the type of HYPERVISOR used in data center environments

---

VIRTUALIZATION (TYPE 2 HYPERVISOR)

![image](https://github.com/psaumur/CCNA/assets/106411237/25a29935-a56d-4ffe-b9e4-15c5c50bca46)

- TYPE 2 HYPERVISORS run as a program on an OS like a regular computer program
    - Examples: VMware Workstation, Oracle Virtualbox, etc
- The OS running directly on the hardware is called the HOST OS
- The OS running in a VM is called a GUEST OS
- Another name for a TYPE 2 HYPERVISOR is *hosted hypervisor*
- Although TYPE 2 HYPERVISORS are rarely used in data center environments, they are common on personal-use devices (for example, if a MAC/Linux user needs to run an app that is only supported on Windows, or vice-versa)

---

WHY VIRTUALIZATION?

- PARTITIONING :
    - Run multiple OS’s on ONE PHYSICAL MACHINE
    - Divide system resources between VIRTUAL MACHINES
    
- ISOLATION :
    - Provide FAULT and SECURITY ISOLATION at the hardware level
    - Preserve performance with advanced resource controls
- ENCAPSULATION :
    - Save the entire state of a virtual machine to files
    - Move and copy virtual machines as easily as moving and copying files

- HARDWARE INDEPENDENCE :
    - Provision or migrate any virtual machine to any physical server

![image](https://github.com/psaumur/CCNA/assets/106411237/f0f5f886-7924-46fc-addf-6916f0d2b2c9)

---

VIRTUAL NETWORKS

![image](https://github.com/psaumur/CCNA/assets/106411237/7bf3f22c-a7b8-41bf-bc1e-8c128a41f20f)

- VMs are connected to each other and the EXTERNAL NETWORK via a VIRTUAL SWITCH running on the HYPERVISOR
- Just like a regular PHYSICAL SWITCH, the vSWITCH’s INTERFACES can operate as ACCESS PORTS or TRUNK PORTS and use VLANs to separate the VMs at LAYER 2
- INTERFACES on the vSWITCH connect to the PHYSICAL NIC (or NICs) of the SERVER to communicate with the EXTERNAL NETWORK

---

INTRO TO CLOUD COMPUTING

- Traditional IT infrastructure deployments were some combination of the following:
    - ON-PREMISES
        - All SERVERS, NETWORK DEVICES, and other infrastructure are located on company property
        - All equipment is purchased and owned by the company using it
        - The company is responsible for the necessary space, power, and cooling
    
    - CO-LOCATION
        - Data centers that rent out space for customers to put their infrastructure (SERVERS, NETWORK DEVICES)
        - The data center provides the space, electricity, and cooling
        - The SERVERS, NETWORK DEVICES, etc are still the responsibility of the end customer, although they are not located on the customer’s premises
- CLOUD SERVICE provide an alternative that is hugely popular and is continuing to grow
    - Most people associate “CLOUD” with PUBLIC CLOUD PROVIDERS such as AWS
        - Although this is the most common USE of CLOUD SERVICES, it’s not the only one

---

CLOUD SERVICES

- The American NIST (National Institute of Standards and Technology) defined cloud computing in SP (Special Publication) 800-145

![image](https://github.com/psaumur/CCNA/assets/106411237/746a4f38-01b9-49cf-8dd9-5522b4cabf7b)

- To understand what the CLOUD is, let’s look at the following outlined in SP 800-145:
    - FIVE ESSENTIAL CHARACTERISTICS
    - THREE SERVICE MODELS
    - FOUR DEPLOYMENT MODELS

---

THE FIVE ESSENTIAL CHARACTERISTICS OF CLOUD

- ON-DEMAND SELF-SERVICE
    - The CUSTOMER is able to use the SERVICE (or stop the SERVICE) freely (via a web portal) without direct communication to the SERVICE PROVIDER

- BROAD NETWORK ACCESS
    - The SERVICE is available through standard NETWORK connections (ie: the Internet or PRIVATE WAN) and can be access through many kinds of DEVICES
- RESOURCE POOLING
    - A POOL of RESOURCES is provided by the SERVICE PROVIDER and when a CUSTOMER requests a SERVICE (for example creates a new VM), the RESOURCES to fulfill that request are allocated from the shared POOL
- RAPID ELASTICITY
    - CUSTOMERS can quickly expand the SERVICE they use in the CLOUD (for example: add new VMs, expand STORAGE, etc) from a POOL of RESOURCES that appear to be infinite. Likewise, they can quickly reduce their SERVICES when not needed
- MEASURED SERVICE
    - The CLOUD SERVICE PROVIDER measures the CUSTOMER’s usage of CLOUD RESOURCES and the CUSTOMER can measure their own use as well. CUSTOMERS are charged based on usage (for example: X Dollars per Gigabyte of STORAGE per day)

---

THE THREE SERVICE MODELS OF THE CLOUD

![image](https://github.com/psaumur/CCNA/assets/106411237/a3f0e08a-3207-4a69-aa81-d4142d6735a3)

- In CLOUD COMPUTING, everything is provided on a “SERVICE” model
- For example: rather than the END USER buying a PHYSICAL SERVER, mounting it on a rack, installing the hypervisor, creating the VM, etc. the SERVICE PROVIDER offers all of this as a SERVICE
- There are a variety of SERVICES referred to as “___________ as a SERVICE” or “__aaS”
- The THREE SERVICE MODELS of CLOUD COMPUTING are:
    
    SOFTWARE as a SERVICE (SaaS) - Example : MS Office 365
    
![image](https://github.com/psaumur/CCNA/assets/106411237/5bcfedb7-3ab6-462a-a089-09884d220ab7)
    
    PLATFORM as a SERVICE (PaaS) - Examples : AWS Lambda and Google App Engine 
    
![image](https://github.com/psaumur/CCNA/assets/106411237/e3886b6b-4ed8-4358-ba47-e2f50378c53d)
    
    INFRASTRUCTURE as a SERVICE (Iaas) - Examples: Amazon EC2 and Google Compute Engine
    
![image](https://github.com/psaumur/CCNA/assets/106411237/f8144a61-0d7f-4928-9e47-73fb969e0b4a)
    

---

DEPLOYMENT MODELS

- Most people assume that “CLOUD” means PUBLIC CLOUD PROVIDERS like AWS, AZURE, and GCP
- Although “PUBLIC CLOUD” is the most common deployment model, it’s not the ONLY one
- The FOUR DEPLOYMENT MODELS of CLOUD COMPUTING are:

- PRIVATE CLOUD

![image](https://github.com/psaumur/CCNA/assets/106411237/b8953a31-3861-41ef-99df-62a49b97610a)

- PRIVATE CLOUDS are generally only used by large enterprises
- Although the CLOUD is PRIVATE, it may be owned by a THIRD PARTY
    - For example: AWS provides PRIVATE CLOUD SERVICES for the American DoD
- PRIVATE CLOUDS may be ON or OFF PREMISES
    - Many people assume “CLOUD” and “ON-PREM” are two different things but that is not always the case
- The same kind of SERVICES offered are the same as in PUBLIC CLOUDS (SaaS, PaaS, IaaS) but the infrastructure is reserved for a SINGLE ORGANIZATION

- COMMUNITY CLOUD

![image](https://github.com/psaumur/CCNA/assets/106411237/1c9008e9-205b-4ca8-8236-fc0b02c3addc)

- Least common CLOUD deployment
- Similar to PRIVATE CLOUD, but the INFRASTRUCTURE is reserved for use by a SPECIFIC GROUP or ORGANIZATION

- PUBLIC CLOUD

![image](https://github.com/psaumur/CCNA/assets/106411237/94e9c895-9538-4664-93db-085f013ee9fb)

- The most common CLOUD deployment
- Popular PUBLIC CLOUD service providers include:
    - AWS
    - MS AZURE
    - GCP (Google Cloud Platform)
    - OCI (Oracle Cloud Infrastructure)
    - IBM Cloud
    - Alibaba Cloud

- HYBRID CLOUD
    
![image](https://github.com/psaumur/CCNA/assets/106411237/14f910cf-b6e2-4f75-8959-4589d2592e1c)
    
    - Basically ANY combination of the preview THREE DEPLOYMENT TYPES
    - Example: A PRIVATE CLOUD which can offload to a PUBLIC CLOUD when necessary

---

BENEFITS OF CLOUD COMPUTING

- COST
    - CapEx (Capital Expense) of buying HARDWARE and SOFTWARE, setting up DATA CENTERS, etc. are reduced or eliminated
- GLOBAL SCALE
    - CLOUD SERVICES can scale GLOBALLY at a rapid pace. SERVICES can be set up and offered to CUSTOMERS from a geographic location close to them

- SPEED / AGILITY
    - SERVICES are provide ON DEMAND and vast amounts of RESOURCES can be provisioned within minutes

- PRODUCTIVITY
    - CLOUD SERVICES remove the need for many time-consuming tasks such as procuring physical servers, racking them, cabling, installing and updating equipment, etc.
- RELIABILITY
    - Backups in the CLOUD are very easy to perform. Data can be mirrored at multiple sites in different geographic locations to support disaster recovery

---

CONNECTION TO PUBLIC CLOUDS

![image](https://github.com/psaumur/CCNA/assets/106411237/671747bb-6908-47bb-b9c8-47f2df82c821)

# 54. VIRTUALIZATION (CONTAINERS): PART 2

REVIEW OF VIRTUAL MACHINES (TYPE 1 and TYPE2 HYPERVISORS)

![image](https://github.com/psaumur/CCNA/assets/106411237/bfc801ca-a603-4957-a67c-316fb72e25cb)

![image](https://github.com/psaumur/CCNA/assets/106411237/da1b653d-f5f2-42d3-8088-dd3daa430913)

- VIRTUAL MACHINES (VMs) allow multiple OS’s to run on a single PHYISCAL SERVER
- A HYPERVISOR is used to manage and allocate HARDWARE RESOURCES to each VM
    - TYPE 1 HYPERVISORS (aka NATIVE or BARE-METAL) run directly on top of HARDWARE
    - TYPE 2 HYPERVISORS (aka HOSTED) run on top of a HOST OS (ie: WINDOWS)
- TYPE 1 HYPERVISORS are widely used in DATA CENTER ENVIRONMENTS
- TYPE 2 HYPERVISORS are commonly used on personal DEVICES
    - Running a virtual network lab on your PC using Cisco Modeling Labs (CML)

- The OS in each VM can be the same or different (Windows, Linux, MacOS, etc)
- *Bins / Libs* are the SOFTWARE libraries / services needed by the Apps running in each VM
- A VM allows it’s app / apps to run in an ISOLATED environment, separate from the apps in other VMs.
- VMs are easy to create, delete, move, etc.
    - A VM can be easily saved and moved between different physical SERVERS.

![image](https://github.com/psaumur/CCNA/assets/106411237/5ed6704c-f332-49bf-8ff9-ad17a7f74b76)

---

CONTAINERS

![image](https://github.com/psaumur/CCNA/assets/106411237/4f350818-f030-46fe-8850-f2e633d22bfa)

- CONTAINERS are software packages that contain an APP and all dependencies (*Bins/Libs* in the diagram) for the contained APP to run.
    - Multiple APPS can be run in a single CONTAINER, but this is not how CONTAINERS are usually used
- CONTAINERS run on a CONTAINER ENGINE (ie: DOCKER ENGINE)
    - The CONTAINER ENGINE is run on a HOST OS (usually LINUX)
- CONTAINERS are lightweight (small in size) and include only the dependencies required to run the specific APP
- A CONTAINER ORCHESTRATOR is a software platform for automating the DEPLOYMENT, MANAGEMENT, SCALING, etc of CONTAINERS
    - KUBERNETES (originally design by Google) is the most popular CONTAINER ORCHESTRATOR
    - DOCKER SWARM is DOCKER’S CONTAINER ORCHESTRATION tool
- In small numbers, MANUAL operation is possible, but large-scale systems (ie: with Microservices) can require THOUSANDS of CONTAINERS

![image](https://github.com/psaumur/CCNA/assets/106411237/07083826-c7b0-45c1-aefe-e05f63d7acfd)

---

VIRTUAL MACHINES vs. CONTAINERS

![image](https://github.com/psaumur/CCNA/assets/106411237/98a4075d-ab70-4579-ba10-c129e935ca22)

- VMs can TAKE MINUTES to boot up as each VM runs it’s own OS
- CONTAINERS can boot up in milliseconds

- VMs take MORE disk space (Gigabytes)
- CONTAINERS take up VERY LITTLE disk space (Megabytes)

- VMs use MORE CPU/RAM resources (each VM must run its own OS)
- CONTAINERS use FEWER CPU/RAM resources (shared OS)

- VMs are PORTABLE and can MOVE between physical systems running the same HYPERVISOR
- CONTAINERS are MORE portable; they are SMALLER, FASTER to boot up, and DOCKER CONTAINERS can be run on nearly ANY CONTAINER SERVICE

- VMs are more isolated because each VM runs it’s own OS
- CONTAINERS are less isolated because they all run on the same OS; if the OS crashes, all CONTAINERS running on it are effected

![image](https://github.com/psaumur/CCNA/assets/106411237/128a8574-a555-4a3e-9e9c-62f33df2d34d)

# 54. VIRTUALIZATION (VRF): PART 3

INTRO TO VRF

![image](https://github.com/psaumur/CCNA/assets/106411237/e122f3c6-290f-4f33-a31d-f308f12140a3)

- VIRTUAL ROUTING AND FORWARDING (VRF) is used to DIVIDE a SINGLE ROUTER into MULTIPLE VIRTUAL ROUTERS
    - Similar to how VLANs are used to divide a SINGLE SWITCH (LAN) into MULTIPLE VIRTUAL SWITCHES (VLANs)
- It does this by allowing a ROUTER to build MULTIPLE SEPARATE ROUTING TABLES
    - INTERFACES (LAYER 3 only) and ROUTERS are configured to be in a specific VRF (aka *VRF INSTANCE*)
    - ROUTER INTERFACES, SVIs and ROUTED PORTS on MULTILAYER SWITCHES can be configured in a VRF
- TRAFFIC in one VRF cannot be forwarded out of an INTERFACE in another VRF
    - As an exception, VRF LEAKING can be configured to allow traffic to pass BETWEEN VRFs
- VRF is commonly used to facilitate MPLS (Multiple Protocol Label Switching)
    - The kind of VRF we are talking about is VRF-Lite (VRF without MPLS)
- VRF is commonly used by SERVICE PROVIDERS to allow ONE DEVICE to carry traffic from MULTIPLE CUSTOMERS
    - Each CUSTOMER’S TRAFFIC is isolated from the OUTSIDE
    - CUSTOMER IP ADDRESSES can overlap without issue

VRF CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/fec7669b-8868-4529-81fa-6f52e07ff6e4)

Creation and Configuration of VRFs

![image](https://github.com/psaumur/CCNA/assets/106411237/624ebfc0-c7c0-498d-a00b-c19e2738585a)

How to `show ip route` for VRFs

![image](https://github.com/psaumur/CCNA/assets/106411237/cbe724be-4497-4976-9927-18ff5c71a4c7)

`ping` other VRFs

![image](https://github.com/psaumur/CCNA/assets/106411237/f29dd935-0ec7-4756-b24a-fc44391254c0)

# 55. WIRELESS FUNDAMENTALS

- Although we will briefly look at other types of WIRELESS NETWORKS, in this section of the course we will be focusing on WIRELESS LANs using WI-FI
- The STANDARDS we use for WIRELESS LANs are defined in IEEE 802.11
- The term WI-FI is a trademark of the WI-FI ALLIANCE, not directly connected to the IEEE
- The WI-FI ALLIANCE tests and certifies equipment for 802.11 standards compliance
- However, WI-FI has become the common term that people use to refer to 802.11 WIRELESS LANs and that term will be used through the course videos

WIRELESS NETWORKS

- WIRELESS NETWORKS have some issues that we need to deal with

![image](https://github.com/psaumur/CCNA/assets/106411237/f1adc053-b4e7-4779-b497-d17fb8caa973)

1)  ALL DEVICES within range receive ALL FRAMES, like DEVICES connected to an ETHERNET HUB

- Privacy of DATA within the LAN is a greater concern
- CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance) is used to facilitate HALF-DUPLEX communications
- CSMA / CD is used in WIRED NETWORKS to detect and recover from COLLISIONS
- CSMA / CA is used in WIRELESS NETWORKS to avoid COLLISIONS

- When using CSMA / CA, a DEVICE will wait for other DEVICES to STOP TRANSMITTING before it TRANSMITS DATA itself.

![image](https://github.com/psaumur/CCNA/assets/106411237/7d266279-5342-478e-8001-0146a016296b)

2)  WIRELESS COMMUNICATIONS are regulated by various INTERNATIONAL and NATIONAL bodies

3)  WIRELESS SIGNAL COVERAGE AREA must be considered

- Signal Range
- Signal ABSORPTION, REFLECTION, REFRACTION, DIFFRACTION, and SCATTERING

---

SIGNAL ABSORPTION

- ABSOPTION happens when a WIRELESS SIGNAL PASSES THROUGH a material and is converted into HEAT, weakening the SIGNAL

![image](https://github.com/psaumur/CCNA/assets/106411237/9ef52c86-66ef-46fb-872e-cb76f0fb8d83)

SIGNAL REFLECTION

- REFLECTION happens when a SIGNAL BOUNCES off a material (like metal)
    - This is why WI-FI reception is usually POOR in elevators. The SIGNAL bounces off the metal and very little penetrates into the elevator

![image](https://github.com/psaumur/CCNA/assets/106411237/d57a94df-4e82-46f2-8045-de01f7a293f1)

SIGNAL REFRACTION

- REFRACTION happens when a WAVE is BENT when entering a medium where the SIGNAL travels at a different speed
    - For example, glass and water can refract waves

![image](https://github.com/psaumur/CCNA/assets/106411237/9c807832-6feb-40ed-81aa-f9d7337da241)

SIGNAL DIFFRACTION

- DIFFRACTION happens when a WAVE encounters an OBSTACLE and travels AROUND it
    - This can result in “BLIND SPOTS” behind the obstacle

![image](https://github.com/psaumur/CCNA/assets/106411237/abd44fc3-ec6f-484c-8c81-a2de38c26999)

SIGNAL SCATTERING

- SCATTERING happens when a material causes a SIGNAL to SCATTER in all directions
    - Dust, smog, uneven surfaces, etc. can cause scattering

![image](https://github.com/psaumur/CCNA/assets/106411237/9474adb8-3fc0-44ac-b480-c846cec21e9a)

---

4) Other DEVICES using the SAME CHANNELS can cause INTERFERENCE

- For example, a WIRELESS LAN in your neighbor’s house / apartment

---

RADIO FREQUENCY (RF)

- To send WIRELESS SIGNALS, the SENDER applies an ALTERNATING CURRENT to an antenna
    - This creates ELECTROMAGNETIC WAVES which propagate out as WAVES
- ELECTROMAGENETIC WAVES can be measured in multiple ways - for example AMPLITUDE and FREQUENCY
- AMPLITUDE is the MAXIMUM STRENGTH of the ELECTRIC and MAGNETIC FIELDS

![image](https://github.com/psaumur/CCNA/assets/106411237/f7daa2ac-16a7-41f2-8ba4-a7c214c7e96b)

- FREQUENCY measures the number of UP / DOWN CYCLES per a GIVEN UNIT of TIME
- The most COMMON measurement of FREQUENCE is HERTZ
    - Hz (HERTZ) = cycles per second
    - kHz (KILOHERZ) = 1,000 cycles per second
    - MHz (MEGAHERZ) = 1,000,000 cycles per second
    - GHz (GIGAHERTZ) = 1,000,000,000 cycles per second
    - THz (TERAHERTZ) = 1,000,000,000,000 cycles per second
    

4 CYCLES per 1 SECOND = 4 HERTZ

![image](https://github.com/psaumur/CCNA/assets/106411237/448e6f45-6ef1-4c53-abf7-dd843e8d7a84)

![image](https://github.com/psaumur/CCNA/assets/106411237/28ea49c0-c2ef-40f3-a703-884c612c16f7)

- Another important term is PERIOD, the amount of TIME of ONE CYCLE
    - If the FREQUENCY is 4 Hz, the PERIOD is 0.25 SECONDS

![image](https://github.com/psaumur/CCNA/assets/106411237/9ddcffd6-c623-4d75-bee0-d4f01d871085)

- The VISIBLE FREQUENCY RANGE is ~400 THz to 790 THz
- The RADIO FREQUENCY RANGE is 30 Hz to 300 GHz and is used for many purposes.

![image](https://github.com/psaumur/CCNA/assets/106411237/caf70e36-75b2-4fe5-a2e2-2641fad4d7e0)

---

RADIO FREQUENCY BANDS 

- WI-FI uses TWO MAIN BANDS (FREQUENCY RANGES)
- 2.4 GHz band
    - Range is 2.400 - 2.4835 GHz
- 5 GHz band
    - Range is 5.150 - 5.825 GHz
    - Divided into FOUR SMALLER BANDS:
        - 5.150 - 5.250 GHz
        - 5.250 - 5.350 GHz
        - 5.470 - 5.725 GHz
        - 5.725 - 5.825 GHz

- The 2.4 GHz band typically provides FURTHER REACH in open space and BETTER PENETRATION of obstacles such as walls.
    - HOWEVER, more DEVICES tend to use the 2.4 GHz BAND so INTERFERENCE can be a BIGGER PROBLEM compared to 5GHz

** WI-FI 6 (802.11ax) has EXPANDED the spectrum range to include a band in the 6 GHz RANGE

---

CHANNELS

- Each BAND is divided up into MULTIPLE “CHANNELS”
    - DEVICES are configured to TRANSMIT and RECEIVE traffic on one (or more) of these CHANNELS
- The 2.4 GHz BAND is divided into several CHANNELS, each with a 22 MHz RANGE
- In a SMALL WIRELESS LAN with only a single ACCESS POINT (AP), you can use ANY channel
- However, in larger WLANs with multiple APs, it’s important that adjacent APs don’t use OVERLAPPING CHANNELS. This helps avoid INTERFERENCE
- In the 2.4 GHz BAND, it is recommended to use CHANNELS 1, 6 and 11

![image](https://github.com/psaumur/CCNA/assets/106411237/005d246e-d2d2-491e-8d1e-f2fb5afbb664)

- The 5 GHz BAND consists of NON-OVERLAPPING channels so it’s much EASIER to avoid INTERFERENCE between adjacent APs

- Using CHANNELS 1, 6, 11, you can place APs in a “HONEYCOMB” pattern to provide COMPLETE coverage of an area without INTERFERENCE between CHANNELS

![image](https://github.com/psaumur/CCNA/assets/106411237/8bce5d9c-6261-4180-a25c-20007a27f433)

---

WI-FI STANDARDS (802.11)

![image](https://github.com/psaumur/CCNA/assets/106411237/424d3b31-2bbe-454d-973c-fdf1534adfdd)

---

SERVICE SETS

- 802.11 defines different kinds of SERVICE SETS which are groups of WIRELESS NETWORK DEVICES
- There are THREE MAIN TYPES:
    - INDEPENDENT
    - INFRASTRUCTURE
    - MESH
- ALL DEVICES in a SERVICE SET share the same SSID (Service Set Identifier)
- The SSID is a HUMAN-READABLE NAME which identifies the SERVICE SET
- The SSID does NOT have to be UNQUE

SERVICE SETS : IBSS

- An IBSS (INDEPENDENT BASIC SERVICE SET) is a WIRELESS NETWORK in which TWO or MORE WIRELESS DEVICES connect directly without using an AP (ACCESS POINT)
- Also called an AD HOC NETWORK
- Can be used for FILE TRANSFER (ie: AirDrop)
- Not scalable beyond a few DEVICES

![image](https://github.com/psaumur/CCNA/assets/106411237/5fe65388-0045-4f35-bd8b-5325e2779ab2)

SERVICE SETS : BSS

- A BSS (BASIC SERVICE SET) is a kind of infrastructure SERVICE SET in which CLIENTS connect to each other via an AP (ACCESS POINT) but not DIRECTLY to each other
- A BSSID (BASIC SERVICE SET ID) is used to uniquely identify the AP
    - Other APs can use the SAME SSID but NOT THE SAME BSSID
    - The BSSID is the MAC ADDRESS of the APs RADIO
- WIRELESS DEVICES request to *associate* with the BSS
- WIRELESS DEVICES that have associated with the BSS are called “CLIENTS” or “STATIONS”
- The AREA around an AP where its SIGNAL is usable is called a BSA (BASIC SERVICE AREA)

![image](https://github.com/psaumur/CCNA/assets/106411237/ef259f45-ead1-45f3-8ad3-5f343a763988)

SERVICE SETS: ESS

- To create LARGER WIRELESS LANS beyond the range of a SINGLE AP, we use an ESS (EXTENDED SERVICE SET)
- APs with their own BSSs are connected by a WIRED NETWORK
    - Each BSS uses the SAME SSID
    - Each BSS has a UNIQUE BSSID
    - Each BSS uses a DIFFERENT channel to avoid INTERFERENCE
- CLIENTS can pass between APs without having to RECONNECT, providing a SEAMLESS WI-FI experience when moving between APs
    - This is called ROAMING
- The BSAs should overlap about 10-15%

![image](https://github.com/psaumur/CCNA/assets/106411237/4a2ccc9e-c3c2-43db-b0b2-c704d5da223e)

SERVICE SETS: MBSS

- An MBSS (MESH BASIC SERVICE SET) can be used in situations where it’s difficult to run an ETHERNET connection to every AP
- MESH APs use TWO RADIOS:
    - ONE provides BSS to WIRELESS CLIENTS
    - ONE forms a “BACKHAUL NETWORK” which is used to BRIDGE traffic from AP to AP
- At least ONE AP is connected to the WIRED NETWORK and it is called the RAP (ROOT ACCESS POINT)
- The OTHER APs are called MAPs (MESH ACCESS POINTS)
- A PROTOCOL is used to determine the BEST PATH through the MESH (similar to how DYNAMIC ROUTING PROTOCOLS are used to determine the BEST PATH to a DESTINATION)

![image](https://github.com/psaumur/CCNA/assets/106411237/1604f0ea-8a93-4922-a78d-fe55e836ba9a)

---

DISTRIBUTION SYSTEM

- Most WIRELESS NETWORKS are not STANDALONE NETWORKS
    - Rather, they are a way for WIRELESS CLIENTS to connect to the WIRED NETWORK INFRASTRUCTURE
- In 802.11, the UPSTREAM WIRED NETWORK is called the DS (DISTRIBUTION SYSTEM)
- Each WIRELESS BSS or ESS is mapped to a VLAN in the WIRED NETWORK

![image](https://github.com/psaumur/CCNA/assets/106411237/adf9deae-693c-4f1b-8d6d-c4fbfc356418)

- It is possible for an AP to provide MULTIPLE WIRELESS LANs, each with a unique SSID
- Each WLAN is mapped to a separate VLAN and connected to the WIRED NETWORK via a TRUNK
- Each WLAN uses a UNIQUE BSSID, usually by INCREMENTING the LAST digit of the BBSID by one

![image](https://github.com/psaumur/CCNA/assets/106411237/5667abba-dc3f-4571-a11a-43b3e8cf4304)

---

ADDITIONAL AP OPERATIONAL MODES

- APs can operate in ADDITIONAL MODES beyond the ones we’ve introduced so far

- An AP in REPEATER MODE can be used to EXTEND the RANGE of a BSS

- The REPEATER will re-transmit ANY SIGNAL it receives from the AP
    - A REPEATER with a SINGLE RADIO must operate on the SAME CHANNEL as the AP, but this can drastically reduce the overall THROUGHPUT on the CHANNEL
    - A REPEATER with TWO RADIOS can receive on ONE CHANNEL and then retransmit on ANOTHER CHANNEL

![image](https://github.com/psaumur/CCNA/assets/106411237/7973107f-7f2a-47de-9272-186040b038b5)

- A WORKGROUP BRIDGE (WGB) operates as a WIRELESS CLIENT of another AP and can be used to CONNECT WIRED DEVICES to the WIRELESS NETWORK
- In the example below, PC1 does NOT have WIRELESS CAPABILITIES, and also DOES NOT have ACCESS to WIRED CONNECTIONS to SW1
- PC1 has a WIRED CONNECTION to the WGB, which has a WIRELESS CONNECTION to the AP

![image](https://github.com/psaumur/CCNA/assets/106411237/85cffc3f-3e76-4a55-9810-254135162a82)

- AN OUTDOOR BRIDGE can be used to connect NETWORKS over LONG DISTANCES without a PHYSICAL CABLE connecting them
- The APs will use SPECIALIZED ANTENNAS that focus most of the SIGNAL POWER in one direction, which allows the WIRELESS CONNECTION to be made over LONGER DISTANCES than normally possible
- The CONNECTION can be POINT-TO-POINT as in the diagram below, or POINT-TO-MULTIPOINT in which MULTIPLE SITES connect to on CENTRAL SITE

![image](https://github.com/psaumur/CCNA/assets/106411237/36b421fd-ba81-4230-8c67-72b0b88aae8a)

---

REVIEW
![image](https://github.com/psaumur/CCNA/assets/106411237/7bac6988-f3af-4ee3-8046-7d926069934c)


# 56. WIRELESS ARCHITECTURES

802.11 MESSAGE / FRAME FORMAT

![image](https://github.com/psaumur/CCNA/assets/106411237/7b459483-7156-44cf-9ee7-f9391e476636)

- 802.11 FRAMES have a different format than 802.3 ETHERNET FRAMES
- For the CCNA, you don’t have to learn it in as much detail as the ETHERNET and IP HEADERS
- Depending on the 802.11 VERSION and the MESSAGE TYPE, some of the fields might not be present in the FRAME
    - For example: Not ALL messages use all 4 ADDRESS FIELDS
- FRAME CONTROL
    - Provides information such as MESSAGE TYPE and SUBTYPE
    - Indicates if the FRAME is a MANAGEMENT frame
- DURATION / ID
    - Depending on the MESSAGE TYPE, this field can indicate:
        - The TIME (in microseconds) the CHANNEL will be dedicated to transmission of the FRAME
        - Identifier for the ASSOCIATION (the connection)
    
- ADDRESSES
    - Up to FOUR ADDRESSES can be present in an 802.11 FRAME.
    - Which ADDRESSES are present, and their ORDER, depends on the MESSAGE TYPE
        - DESTINATION ADDRESS (DA) : Final RECIPIENT of the FRAME
        - SOURCE ADDRESS (SA) : Original SENDER of the FRAME
        - RECEIVER ADDRESS (RA) : Immediate RECIPIENT of the FRAME
        - TRANSMITTER ADDRESS (TA) : Immediate SENDER of the FRAME
    
- SEQUENCE CONTROL
    - Used to reassemble FRAGMENTS and eliminate DUPLICATE FRAMES

- QoS CONTROL
    - Used in QoS to PRIORITIZE certain traffic
- HT (High Throughput) CONTROL
    - Added in 802.11n to ENABLE High Throughput operations
    - 802.11n is also known as “HIGH THROUGHPUT” (HT) WI-FI
    - 802.11ac is also know as “VERY HIGH THROUGHPUT” (VHT) WI-FI

- FCS (FRAME CHECK SEQUENCE)
    - Same as in an ETHERNET FRAME, used to check for errors

---

802.11 ASSOCIATION PROCESS

- ACCESS POINTS bridge traffic between WIRELESS STATIONS and other DEVICES
- For a STATION to send traffic through the AP, it must be associated with the AP
- There are THREE 802.11 CONNECTION STATES:
    - NOT AUTHENTICATED, NOT ASSOCIATED
    - AUTHENTICATED, NOT ASSOCIATED
    - AUTHENTICATED and ASSOCIATED

- The STATION must be AUTHENTICATED and ASSOCIATED with the AP to send traffic through it

![image](https://github.com/psaumur/CCNA/assets/106411237/568d795d-41ee-4afd-908d-858297e89c6c)

---

802.11 MESSAGE TYPES

- There are THREE 802.11 MESSAGE TYPES
    - MANAGEMENT
    - CONTROL
    - DATA

- MANAGEMENT
    - Used to manage the BSS
        - BEACON
        - PROBE REQUEST / PROBE RESPONSE
        - AUTHENTICATION
        - ASSOCIATION REQUEST / ASSOCIATION RESPONSE

- CONTROL
    - Used to control access to the medium (RADIO FREQUENCY)
    - Assists with delivery of MANAGEMENT and DATA FRAMES
        - RTS (REQUEST TO SEND)
        - CTS (CLEAR TO SEND)
        - ACK

- DATA
    - Used to send actual DATA PACKETS

 

---

AUTONOMOUS APs

- AUTONOMOUS APs are self-contained SYSTEMS that do NOT RELY on a WLC
- AUTONOMOUS APs are configured individually
    - Can be configured by CONSOLE cable (CLI)
    - Can be configured by TELNET (CLI)
    - Can be configured by HTTP / HTTPS Web connection (GUI)
    - An IP ADDRESS for REMOTE MANAGEMENT should be configured
    - The RF PARAMETERS must be manually configured (Transmit Power, Channel, etc)
    - SECURITY POLICIES are handled individually by each AP
    - QoS RULES etc. are configured individually by each AP

 

- There is NO CENTRAL MONITORING or MANAGEMENT of APs

![image](https://github.com/psaumur/CCNA/assets/106411237/57faecbb-36a6-424d-b019-52994a5740db)

- AUTONOMOUS APs connect to the WIRED NETWORK with a TRUNK link
- DATA traffic from WIRELESS CLIENTS have a very direct PATH to the WIRED NETWORK or to other WIRELESS CLIENTS associated with the same AP
- Each VLAN has to STRETCH across the entire NETWORK. This is considered BAD practice
    - Large Broadcast Domains
    - Spanning Tree will disable links
    - Adding / Deleting VLANs is VERY labor-intensive
- AUTONOMOUS APs can be used in SMALL NETWORKS but they are not viable in MEDIUM to LARGE NETWORKS
    - LARGE NETWORKS can have thousands of APs

- AUTONOMOUS APs can also function in the modes covered in the previous video:
    - REPEATER
    - OUTDOOR BRIDGE
    - WORKGROUP BRIDGE

---

LIGHTWEIGHT APs

- The functions of an AP can be split between the AP and a WIRELESS LAN CONTROLLER (WLC)
- The is what is called SPLIT-MAC ARCHITECTURE

- LIGHTWEIGHT APs handle **“real-time”** operations like:
    - TRANSMITTING / RECEIVING RF TRAFFIC
    - ENCRYPTION / DECRYPTION OF TRAFFIC
    - SENDING OUT BEACONS / PROBES
    - PACKET PRIORITIZATION
    - Etc…
- WLC Functions (not time dependent)
    - RF MANAGEMENT
    - SECURITY / QoS MANAGEMENT
    - CLIENT AUTHENTICATION
    - CLIENT ASSOCIATION / ROAMING MANAGEMENT
    - RESOURCE ALLOCATION
    - Etc…
    
- The WLC is also used to centrally configured the lightweight APs
- The WLC can be located in the same SUBNET / VLAN as the lightweight APs it manages OR in a different SUBNET / VLAN
- The WLC and the lightweight APs AUTHENTICATE each other using DIGITAL CERTIFICATES installed on each DEVICE ( X.509 STANDARD CERTIFICATES )
    - This ensures that only AUTHORIZED APs can join the NETWORK

![image](https://github.com/psaumur/CCNA/assets/106411237/c154bcad-ae81-4fb8-9acf-56913dffaf04)

- THE WLC and lightweight APs use a PROTOCOL called CAPWAP (CONTROL AND PROVISIONING OF WIRELESS ACCESS POINTS) to communicate
    - Based on an older PROTOCOL called LWAPP (LIGHTWEIGHT ACCESS POINT PROTOCOL)

- TWO TUNNELS are created between each AP and the WLC :
    - CONTROL TUNNEL (UDP Port 5246)
        - This TUNNEL is used to configure the APs and control and manage operations
        - All traffic in this TUNNEL is ENCRYPTED, by default
    - DATA TUNNEL (UDP Port 5247)
        - All traffic from WIRELESS CLIENTS is sent through this TUNNEL to the WLC
        - IT DOES NOT GO DIRECTLY TO THE WIRED NETWORK !

- Traffic in this TUNNEL is not ENCRYPTED by default but you can configure it to be ENCRYPTED with DTLS (DATAGRAM TRANSPORT LAYER SECURITY)

- Because ALL traffic from WIRELSS CLIENTS is TUNNELED to the WLC with CAPWAP, APs connect to the SWITCH ACCESS PORTS - NOT TRUNK PORTS

![image](https://github.com/psaumur/CCNA/assets/106411237/10917a40-468a-4ea6-8253-bf229d612af1)

---

***  (Not necessary to MEMORIZE for CCNA) ***

There are some KEY BENEFITS to SPLIT-MAC ARCHITECTURE

- SCALABILITY
    - With a WLC (or multiple) it’s SIMPLER to build and support a NETWORK with thousands of APs
- DYNAMIC CHANNEL ASSIGNMENT
    - The WLC can automatically select which channel each AP should use
- TRANSMIT POWER OPTIMIZATION
    - The WLC can automatically set the appropriate transmit power for each AP
- SELF-HEALING WIRELESS COVERAGE
    - When an AP stops functioning, the WLC can increase the transmit power of nearby APs to avoid coverage holes
- SEAMLESS ROAMING
    - CLIENTS can roam between APs with no noticeable delay
- CLIENT LOAD BALANCING
    - If a CLIENT is in range of TWO APs, the WLC can associate the CLIENT with the least-used AP, to balance the load among APs
- SECURITY / QoS MANAGEMENT
    - Central management of SECURITY and QoS policies ensures consistency across the NETWORK

---

- LIGHTWEIGHT APs can be configured to operate in VARIOUS MODES:
    - LOCAL
        - This is the DEFAULT mode where the AP offers a BSS (more multiple BSSs) for CLIENTS to associate with
        
    - FLEXCONNECT
        - Like a LIGHTWEIGHT AP in LOCAL mode, it offers ONE or MORE BSSs for CLIENTS to associate with
        - HOWEVER, FLEXCONNECT allows the AP to locally SWITCH traffic between the WIRED (TRUNK) and WIRELESS NETWORKS (ACCESS) if the TUNNELS to the WLC go down
    
![image](https://github.com/psaumur/CCNA/assets/106411237/aa2d7d98-2d6f-46b6-ab38-7acc96c8dc52)
    

- SNIFFER
    - The AP does NOT OFFER a BSS for CLIENTS
    - Dedicated to CAPTURING 802.11 FRAMES and SENDING them to a DEVICE running software such as WIRESHARK

- MONITOR
    - The AP does NOT OFFER a BSS for CLIENTS
    - Dedicated to RECEIVING 802.11 FRAMES to detect ROGUE DEVICES
    - If a CLIENT is found to be a ROGUE DEVICE, an AP can send DE-AUTHENTICATION MESSAGES to disassociate the ROGUE DEVICE from the AP

- ROGUE DETECTOR
    - The AP does not even USE its RADIO
    - It LISTENS to traffic on the WIRED NETWORK only, but it receives a list of SUSPECTED ROGUE CLIENTS and AP MAC ADDRESSES from the WLC
    - By LISTENING to ARP MESSAGES on the WIRED NETWORK and correlating it with the information it receives from the WLC, it can DETECT ROGUE DEVICES

- SE-CONNECT (SPECTRUM EXPERT CONNECT)
    - The AP does NOT OFFER a BSS for CLIENTS
    - Dedicated to RF SPECTRUM ANALYSIS on ALL CHANNELS
    - It can send information to software such as Cisco Spectrum Expert on a PC to COLLECT and ANALYZE the DATA

- BRIDGE / MESH
    - Like the AUTONOMOUS APs *OUTDOOR BRIDGE* mode, the LIGHTWEIGHT AP can be a DEDICATED BRIDGE between SITES (Example:  over LONG distances)
    - A MESH can be made between the ACCESS POINTS

- FLEX PLUS BRIDGE
    - Adds FLEXCONNECT functionality to the BRIDGE / MESH mode
    - Allows WIRELESS ACCESS POINTS to locally forward traffic even if connectivity to the WLC is lost
    

![image](https://github.com/psaumur/CCNA/assets/106411237/940a414b-208f-408c-a3e2-37e3bfbb0d32)

---

CLOUD-BASED APs

- CLOUD-BASED AP architecture is between AUTONOMOUS AP and SPLIT-MAC ARCHITECTURE
    - AUTONOMOUS APs that are centrally managed in the CLOUD
- CISCO MERAKI is a popular CLOUD-BASED WI-FI solution
- The MERAKI dashboard can be used to configure APs, monitor the NETWORK, generate performance reports, etc.
    - MERAKI also tells each AP which CHANNEL to use, what transmit power, etc.
- However, DATA TRAFFIC is not sent to the CLOUD. It is sent directly to the WIRED NETWORK like when using AUTONOMOUS APs
    - Only management / control traffic is sent to the CLOUD

![image](https://github.com/psaumur/CCNA/assets/106411237/8bd00a94-f965-4257-af46-82be67850feb)

![image](https://github.com/psaumur/CCNA/assets/106411237/93e62771-c2d5-4003-9ade-0d5be855ea66)

---

WIRELESS LAN CONTROLLER (WLC) DEPLOYMENTS

- In a SPLIT-MAC ARCHITECTURE, there FOUR MAIN WLC DEPLOYMENT MODES:
    - UNIFIED
        - THE WLC is a HARDWARE APPLICANCE in a central location of the NETWORK
    - CLOUD-BASED
        - The WLC is a VM running on a SERVER, usually in a PRIVATE CLOUD in a DATA CENTER
        - This is NOT the same as the CLOUD-BASED AP ARCHITECTURE discussed previously
    - EMBEDDED
        - The WLC is integrated within a SWITCH
    - MOBILITY EXPRESS
        - THE WLC is integrated within an AP

---

UNIFIED WLC

- THE WLC is a HARDWARE APPLICANCE in a central location of the NETWORK
- A UNIFIED WLC can support up to about 6000 APs
- If more than 6000 APs are needed, additional WLCs can be added to the NETWORK

![image](https://github.com/psaumur/CCNA/assets/106411237/922eac1f-6c62-4926-89bb-a447f8be2edd)

---

CLOUD-BASED

- The WLC is a VM running on a SERVER, usually in a PRIVATE CLOUD in a DATA CENTER
- CLOUD-BASED WLCs can typically support up to about 3000 APs
- If more than 3000 APs are needed, more WLC VMs can be deployed

![image](https://github.com/psaumur/CCNA/assets/106411237/9d87546c-6397-48d2-941c-007f5e6440aa)

---

EMBEDDED WLC

- The WLC is embedded within a SWITCH
- An EMBEDDED WLC can support up to about 200 APs
- If more than 200 APs are needed, more SWITCHES with EMBEDDED WLCs can be added

![image](https://github.com/psaumur/CCNA/assets/106411237/fc6a79f2-a7b5-4b5a-99d6-b94238362e8e)

---

CISCO MOBILITY EXPRESS WLC

- The WLC is embedded within an AP
- A MOBILITY EXPRESS WLC can support up to about 100 APs
- If more than 100 APs are needed, more APs with EMBEDDED MOBILITY  EXPRESS WLCs can be added

![image](https://github.com/psaumur/CCNA/assets/106411237/4ff02aee-83c9-4a56-8a71-a14e20e8bf3c)

# 57. WIRELESS SECURITY

INTRO TO WIRELESS NETWORK SECURITY

- Although SECURITY is important in ALL NETWORKS, it is even more essential in WIRELESS NETWORKS
- Because WIRELESS SIGNALS are not contained within a WIRE, any DEVICE within range of the signal can receive traffic
- In WIRED NETWORKS, traffic is often only ENCRYPTED when sent over an UNTRUSTED NETWORK such as the INTERNET
- In WIRELESS NETWORKS, it is VERY important to ENCRYPT traffic sent between the WIRELESS CLIENTS and the AP

- We will cover THREE MAIN CONCEPTS:
    - AUTHENTICATION
    - ENCRYPTION
    - INTEGRITY

---

AUTHENTICATION

- All CLIENTS must be AUTHENTICATED before they can associate with an AP
- In a corporate setting, only TRUSTED USERS / DEVICES should be given ACCESS to the NETWORK
    - In corporate settings, a separate SSID which doesn’t have ACCESS to the corporate NETWORK can be provided for GUEST USERS
- Ideally, CLIENTS should also AUTHENTICATE the AP to avoid associating with a malicious AP
- There are MULTIPLE WAYS to AUTHENTICATE:
    - PASSWORD
    - USERNAME / PASSWORD
    - CERTIFICATES

![image](https://github.com/psaumur/CCNA/assets/106411237/00d34740-8da7-428d-8b36-f8998ec2f0cd)

---

ENCRYPTION

- Traffic sent between CLIENTS and APs should be ENCRYPTED so that it can’t be read by anyone except the AP and the CLIENT
- There are many possible PROTOCOLS that can be used to ENCRYPT traffic
- All DEVICES on the WLAN will use the same PROTOCOL, however each CLIENT will use a unique ENCRYPTION / DECRYPTION KEY so that other DEVICES can’t read its traffic
- A “GROUP KEY” is used by the AP to ENCRYPT traffic that it wants to send to all of its clients
    - All of the CLIENTS associated with the AP keep that key so they can DECRYPT the traffic
    

---

INTEGRITY

- As explained in the “SECURITY FUNDAMENTALS” video of the course, INTEGRITY ensures that the message is not modified by a third-party
- The message that is sent by the SOURCE HOST should be the same as the message that is received by the DESTINATION HOST
- A MIC (Message Integrity Check) is added to the message to help protect their INTEGRITY.

![image](https://github.com/psaumur/CCNA/assets/106411237/b632c321-36e5-4a03-b08c-d0a2c2e215da)

---

AUTHENTICATION METHODS

The original 802.11 STANDARD included TWO OPTIONS for AUTHENTICATION:

- OPEN AUTHENTICATION
    - The CLIENT sends an AUTHENTICATION REQUEST and the AP just accepts it
    - The is clearly NOT a SECURE AUTHENTICATION method
    - After the CLIENT is AUTHENTICATED and associated with the AP, it’s possible to require the USER to AUTHENTICATE via other methods before ACCESS to the NETWORK is granted (ie: Starbucks WI-FI)
- WEP (Wired Equivalent Privacy)
    - WEP is used to provide both AUTHENTICATION and ENCRYPTION of WIRELESS traffic
    - For ENCRYPTION, WEP uses the RC4 ALGORITHM
    - WEP is a “SHARED-KEY” PROTOCOL, requiring the SENDER and RECEIVER to have the same KEY
    - WEP KEYS can be 40 bits or 104 bits in length
    - The above KEYS are combined with a 24-bit “IV” (INITIALIZATION VECTOR) to bring the total length to 64 bits or 128 bits
    - WEP ENCRYPTION is NOT SECURE and can easily be cracked
    - WEP can be used for AUTHENTICATION like this:
    

![image](https://github.com/psaumur/CCNA/assets/106411237/86e4f243-1692-41a6-9b15-6b2e99942e50)

---

EAP (Extensible Authentication Protocol)

- EAP is an AUTHENTICATION FRAMEWORK
- It defines a STANDARD SET of AUTHENTICATION FUNCTIONS that are used by the various *EAP METHODS*
- We will look at FOUR EAP METHODS:
    - LEAP
    - EAP-FAST
    - PEAP
    - EAP-TLS
- EAP is integrated with **802.1X** which provides *PORT-BASED NETWORK ACCESS CONTROL*

**802.1X** is used to limit NETWORK ACCESS for CLIENTS connected to a LAN or WLAN until they AUTHENTICATE

There are **THREE MAIN ENTITIES** in 802.1X:

- SUPPLICANT : The DEVICE that wants to connect to the NETWORK
- AUTHENTICATOR : The DEVICE that provides access to the NETWORK
- AUTHENTICATION SERVER (AS) : The DEVICE that receives CLIENT credentials and PERMITS / DENIES ACCESS

![image](https://github.com/psaumur/CCNA/assets/106411237/5565e646-696f-4245-b1e5-d728fe0e3380)

- LEAP (Lightweight EAP)
    - LEAP was developed by Cisco an an improvement over WEP
    - CLIENTS must provide a USERNAME and PASSWORD to AUTHENTICATE
    - In addition, *MUTUAL AUTHENTICATION* is provided by both the CLIENT and SERVER sending a CHALLENGE PHRASE to each other.
    - DYNAMIC WEP KEYS are used, meaning that the WEP KEYS are changed frequently
    - Like WEP, LEAP is considered vulnerable and should not be used anymore

![image](https://github.com/psaumur/CCNA/assets/106411237/0b9ecce2-4219-42d0-8275-086b92134cda)

- EAP-FAST (EAP FLEXIBLE AUTHENTICATION via SECURE TUNNELING)
    - EAP-FAST was also developed by Cisco
    - Consists of THREE PHASES:
        - A PAC (PROTECTED ACCESS CREDENTIAL) is generated and passed from SERVER to CLIENT
        - A SECURE TLS TUNNEL is established between the CLIENT and AUTHENTICATION SERVER
        - Inside of the SECURE (ENCRYPTED) TLS TUNNEL, the CLIENT and SERVER communicated further to AUTHENTICATE / AUTHORIZE the CLIENT
    

![image](https://github.com/psaumur/CCNA/assets/106411237/f17d6f7b-9f87-4cb2-be24-5d8c95dc0cfc)

- PEAP (PROTECTED EAP)
    - Like EAP-FAST, PEAP involves establishing a SECURE TLS TUNNEL between the CLIENT and SERVER
    - Instead of a PAC, the SERVER has a DIGITAL CERTIFICATE
    - The CLIENT uses this DIGITAL CERTIFICATE to AUTHENTICATE the SERVER
    - The CERTIFICATE is also used to establish a TLS TUNNEL
    - Because only the SERVER provides a CERTIFICATE for AUTHENTICATION, the CLIENT must still be AUTHENTICATED within the SECURE TUNNEL
        - Example: MS-CHAP (Microsoft Challenge-Handshake Authentication Protocol)

![image](https://github.com/psaumur/CCNA/assets/106411237/0f9babe7-d86f-49c8-b732-20f31ea26437)

- EAP-TLS (EAP TRANSPORT LAYER SECURITY)
    - Whereas PEAP only requires the AS to have a CERTIFICATE, EAP-TLS requires a CERTIFICATE on the AS and on every single CLIENT
    - EAP-TLS is the MOST SECURE WIRELESS AUTHENTICATION method, but it is more difficult to implement than PEAP because every CLIENT DEVICE needs a CERTIFICATE
    - Because the CLIENT and SERVER AUTHENTICATE each other with DIGITAL CERTIFICATES, there is no need to AUTHENTICATE the CLIENT within the TLS TUNNEL
    - The TLS TUNNEL is still used to exchange ENCRYPTION KEY information (ENCRYPTION methods will be discussed next)

![image](https://github.com/psaumur/CCNA/assets/106411237/c6c57595-fd75-4761-8760-29fab8dbf698)

---

ENCRYPTION / INTEGRITY METHODS

- TKIP (Temporal Key Integrity Protocol)
    - WEP was found to be vulnerable, but WIRELESS hardware at the time was built to use WEP
    - A temporary solution was needed until a new STANDARD was created and a new HARDWARE was built
    - TKIP adds various SECURITY FEATURES:
        - A MIC (Message Integrity Check) is added to protect the integrity of messages
        - A KEY MIXING ALGORITHM is used to create a unique WEP key for every frame
        - The INITIALIZATION VECTOR is doubled in length from 24 bits to 48 bits, making BRUTE-FORCE attacks much more difficult
        - The MIC includes the SENDER MAC ADDRESS to identify the FRAME’s SENDER
        - A TIMESTAMP is added to the MIC to prevent replay attacks. Replay attacks involved re-resending a FRAME that has already been transmitted
        - A TKIP SEQUENCE NUMBER is used to keep track of FRAMES sent from each SOURCE MAC ADDRESS. This also protects against REPLAY ATTACKS

** You probably don’t need to memorize ALL of the above features

** TKIP is used in WPA version 1, which will be discussed in the next section

- CCMP (Counter / CBC-MAC Protocol)
    - CCMP was developed after TKIP and is more SECURE
    - It is used in WPA2
    - To use CCMP, it must be supported by the DEVICE’S hardware.
    - Old hardware built only to use WEP / TKIP cannot use CCMP
    - CCMP consists of TWO DIFFERENT ALGORITHMS to provide ENCRYPTION and MIC :
        - AES (Advanced Encryption Standard) COUNTER MODE ENCRYPTION
            - AES is the MOST SECURE ENCRYPTION PROTOCOL currently available.
            - Widely used all over the world
            - There are multiple MODES of operation for AES.
            - CCMP uses “COUNTER MODE”
        - CBC-MAC (CIPHER BLOCK CHAINING MESSAGE AUTHENTICATION CODE)
            - Used as a MIC to ENSURE the INTEGRITY of MESSAGES

- GCMP (GALOIS / COUNTER MODE PROTOCOL)
    - GCMP is MORE SECURE and EFFICIENT than CCMP
    - Its increased efficiency allows higher data throughput than CCMP
    - It is used in WPA3
    - GCMP consists of TWO ALGORITHMS:
        - AES COUNTER MODE ENCRYPTION
        - GMAC (GALOIS MESSAGE AUTHENTICATION CODE)
            - Used as a MIC to ENSURE the INTEGRITY of MESSAGE

---

WI-FI PROTECTED ACCESS (WPA)

- The WI-FI Alliance has developed THREE WPA CERTIFICATIONS for WIRELESS DEVICES:
    - WPA
    - WPA2
    - WPA3
- To be WPA-CERTIFIED, EQUIPMENT must be TESTED in authorized testing labs
- All of the above support TWO AUTHENTICATION MODES:
    - PERSONAL MODE :
        - A PRE-SHARED KEY (PSK) is used for AUTHENTICATOIN
        - When you connect to a home WI-FI NETWORK, enter the PASSWORD and are AUTHENTICATED, that is PERSONAL MODE
        - This is common in small NETWORKS
        - The PSK itself is NOT sent over the air
        - A FOUR-WAY HANDSHAKE is used for AUTHENTICATION and the PSK is used to GENERATE ENCRYPTION KEYS
    - ENTERPRISE MODE :
        - 802.1X is used with an AUTHENTICATION SERVER (RADIUS SERVER)
        - No specific EAP METHOD is specified, so all are supported (PEAP, EAP-TLS, etc)
    
    WPA
    
    - The WPA CERTIFICATION was developed after WEP was proven to be vulnerable and includes the following PROTOCOLS:
        - TKIP (based on WEP) provides ENCRYPTION / MIC
        - 802.1X AUTHENTICATION (ENTERPRISE MODE) or PSK (PERSONAL MODE)
    
    WPA2
    
    - Was released in 2004 and includes the following PROTOCOLS:
        - CCMP provides ENCRYPTION / MIC
        - 802.1X AUTHENTICATION (ENTERPRISE MODE) or PSK (PERSONAL MODE)
    
    WPA3
    
    - Was released in 2018 and includes the following PROTOCOLS:
        - GCMP provides ENCRYPTION / MIC
        - 802.1X AUTHENTICATION (ENTERPRISE MODE) or PSK (PERSONAL MODE)
        
        - WPA3 also provides several additional security features:
            - PMF (PROTECTED MANAGEMENT FRAMES)
                - Protecting 802.11 MANAGEMENT FRAMES from eavesdropping / forging
            - SAE (SIMULTANEOUS AUTHENTICATION OF EQUALS)
                - Protects the four-way handshake when using PERSONAL MODE AUTHENTICATION
            - FORWARD SECRECY
                - Prevents DATA from being DECRYPTED after it has been transmitted over the air so an ATTACKER can’t capture WIRELESS FRAMES and then try to DECRYPT them later

# 58. WIRELESS CONFIGURATION

TOPOLOGY INTRODUCTION

![image](https://github.com/psaumur/CCNA/assets/106411237/1e8ed6b8-1183-42e7-9584-d5504c52987a)

INTERNAL PC (VLAN 100) ACCESSING DEFAULT GATEWAY via Internal CAPWAP tunnel

![image](https://github.com/psaumur/CCNA/assets/106411237/4dec4c60-945e-4f2c-b7db-3028269ec441)

REACHING External GUEST PC  via DEFAULT GATEWAY + Internal and External CAPWAP tunnels

![image](https://github.com/psaumur/CCNA/assets/106411237/3b1c79a6-f8c5-496b-a0b8-d561ff87880f)

---

LAYER 3 SWITCH CONFIGURATION (SW1)

![image](https://github.com/psaumur/CCNA/assets/106411237/eae43f12-aa95-41a3-8a5d-26ffc5e83262)

PART 2 of configuration

Note DHCP “Option 43”

![image](https://github.com/psaumur/CCNA/assets/106411237/ade4dc29-3017-4d79-99d2-d895968bf741)

WLC SETUP

This helps set up the WLC to allow GUI configuration

![image](https://github.com/psaumur/CCNA/assets/106411237/3a2c00c0-eda3-4b72-af07-b07e820365c5)

![image](https://github.com/psaumur/CCNA/assets/106411237/313e030b-add3-4384-bdf0-96306e3663b1)

Why Jeremy chose FRANCE for Country Code (has to do with regulatory domain of equipment)

![image](https://github.com/psaumur/CCNA/assets/106411237/c3a21043-c4fc-47fb-9294-953700fbd8ed)

![image](https://github.com/psaumur/CCNA/assets/106411237/80dce78b-3a7e-4c93-a5f1-47eefb6e28b0)

---

ACCESSING THE WLC GUI

![image](https://github.com/psaumur/CCNA/assets/106411237/a5b44611-af07-4bf6-94b3-957ee342bb24)

![image](https://github.com/psaumur/CCNA/assets/106411237/7924d814-35f2-40d0-ac3c-a2f8022df2bc)

![image](https://github.com/psaumur/CCNA/assets/106411237/45432356-9b45-43dd-99c7-701984d541c1)

![image](https://github.com/psaumur/CCNA/assets/106411237/f097e29c-c7f6-4045-9451-9fdd5035b4b4)

![image](https://github.com/psaumur/CCNA/assets/106411237/b6ec70b7-d628-422b-b693-d9f0af9d1e78)

---

WLC CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/fbc3b9fd-c0db-48f3-9ce8-270812e00008)

WLC PORTS

- WLC PORTS are the PHYSICAL PORTS that cables connect to
- WLC INTERFACES are the logical interfaces within the WLC (ie: SVIs on a SWITCH)
- WLCs have a few different PORTS:
    - SERVICE PORT
        - A dedicated MANAGEMENT PORT
        - Used for OUT-OF-BAND management
        - Must connected to a SWITCH ACCESS PORT because it only supports one VLAN
        - This PORT can be used to connect to the DEVICE while it is booting, performing system recovery, etc.
    - DISTRIBUTION SYSTEM PORT
        - These are the standard NETWORK PORTS that connect to the “DISTRIBUTION SYSTEM” (WIRED NETWORK) and are used for DATA traffic.
        - These PORTS usually connect to SWITCH TRUNK PORTS, and if multiple distribution PORTS are used they can form a LAG
    - CONSOLE PORT
        - This is a standard CONSOLE PORT, either RJ45 or USB
    - REDUNDANCY PORT
        - This PORT is used to connect to another WLC to form a HIGH AVAILABILITY (HA) pair

![image](https://github.com/psaumur/CCNA/assets/106411237/cec94d93-d58b-43b1-8e5e-f4c07ee430fd)

---

WLC INTERFACES

- MANAGEMENT INTERFACES
    - Used for management traffic such as TELNET, SSH, HTTP, HTTPS, RADIUS authentication, NTP, SYSLOG, etc.
    - CAPWAP TUNNELS are also formed to / from the WLC’s management INTERFACE
- REDUNDANCY MANAGEMENT INTERFACE
    - When TWO WLCs are connected by their REDUNDANCY PORTS, one WLC is “ACTIVE” and the other is “STANDBY”
    - This INTERFACE can be used to connect to and manage the “STANDBY” WLC

- VIRTUAL INTERFACE
    - This INTERFACE is used when communicating with WIRELESS CLIENTS to relay DHCP requests, perform CLIENT WEB AUTHENTICATION, etc.

- SERVICE PORT INTERFACE
    - If the SERVICE PORT is used, this INTERFACE is bound to it and used for OUT-OF-BAND MANAGEMENT

- DYNAMIC INTERFACE
    - These are the INTERFACES used to map a WLAN to a VLAN
    - For example :
        - TRAFFIC from the “INTERNAL” WLAN will be sent to the WIRED NETWORK from the WLCs “INTERNAL” DYNAMIC INTERFACE

---

WLAN CONFIGURATION

Click “NEW”

![image](https://github.com/psaumur/CCNA/assets/106411237/b20dbb39-fac6-4cf3-926b-869e75c04e15)

Fill in details of the interface and click “APPLY”

![image](https://github.com/psaumur/CCNA/assets/106411237/48a4810d-a56c-4aef-8cfd-d2474d42cbb1)

Fill out details (IP, Netmask, Gateway…) and then click “APPLY”

![image](https://github.com/psaumur/CCNA/assets/106411237/6d11036b-3d82-4c2f-a20a-4367eb18ca8a)

INTERNAL interface has now been created

![image](https://github.com/psaumur/CCNA/assets/106411237/80a91b22-c4fa-43e2-b035-05ac6199c6f3)

Now, repeat the above steps for the GUEST interface

![image](https://github.com/psaumur/CCNA/assets/106411237/80d5a300-a3ef-4e46-ae1a-7b7afb6a5078)

Fill out details (IP, Netmask, Gateway…) and then click “APPLY”

![image](https://github.com/psaumur/CCNA/assets/106411237/43f70936-4b10-4647-8f57-a086e3f0b7bc)

![image](https://github.com/psaumur/CCNA/assets/106411237/3a98ae1c-13a4-4bde-ab8c-398f8d16da43)

Now that all the INTERFACES are created, we can start WLAN CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/d80eff95-41c7-43c6-a31e-0ebde3a7cd81)

![image](https://github.com/psaumur/CCNA/assets/106411237/960f24e5-efb9-4a15-9f5f-2a8e45b2d425)

INTERNAL WLAN is set to “MANAGEMENT”, it needs to be changed to “INTERNAL”

![image](https://github.com/psaumur/CCNA/assets/106411237/a3cb544c-3ce4-43b5-b054-e52e8388ab83)

SECURITY will also need to be changed from [WPA2] to [WPA2 PSK]

![image](https://github.com/psaumur/CCNA/assets/106411237/4cb2783e-26db-4584-8daa-feba124e9966)

(Need to CHECK the PSK “Enable” box at the bottom)

Change the PSK FORMAT to “ASCII” and enter a PASSWORD (at least 8 chars in length)

![image](https://github.com/psaumur/CCNA/assets/106411237/220202e1-222f-4966-81a6-aafa81727c33)

![image](https://github.com/psaumur/CCNA/assets/106411237/8cd2c63a-aa10-48c3-b826-fe107d04666d)

- WEB AUTHENTICATION
    - After the WIRELESS CLIENTS gets an IP ADDRESS and tries to access a WEB PAGE, they will have to enter a USERNAME and PASSWORD to AUTHENTICATE

- WEB PASSTHROUGH
    - Similar to the above, but NO USERNAME or PASSWORD are required
    - A warning or statement is displayed and the CLIENT simply has to agree to gain access to the INTERNET
    
- CONDITIONAL and SPLASH PAGE web redirect options are similar but additionally require 802.1x LAYER 2 AUTHENTICATION

---

QoS

![image](https://github.com/psaumur/CCNA/assets/106411237/957336a3-d81c-4914-b35f-99925a316ad3)

Default QoS setting is “SILVER” (Best Effort). This can be changed depending on the class of traffic being sent through the WLAN

---

ADVANCED SETTINGS

![image](https://github.com/psaumur/CCNA/assets/106411237/ed70b1b9-b0b6-4b37-b4a5-4492a0cb9120)

![image](https://github.com/psaumur/CCNA/assets/106411237/12bcb065-78af-47b9-810c-fbe7ad739260)

---

CONFIGURING A NEW WLAN (GUEST)

![image](https://github.com/psaumur/CCNA/assets/106411237/4782e82e-4545-458e-917c-42d40e08748d)

Change STATUS to “ENABLED” and INTERFACE GROUP to “GUEST”

![image](https://github.com/psaumur/CCNA/assets/106411237/7a84ce73-0250-404b-896c-695ac5b9d05a)

![image](https://github.com/psaumur/CCNA/assets/106411237/2ca8357b-7564-4ef9-8f36-cb730a4b415f)

Now, we need to change the SECURITY POLICY to [WPA2][Auth(PSK)]

Returning to MONITORING, we can see the changes we made to the CONFIGURATION

![image](https://github.com/psaumur/CCNA/assets/106411237/5a06ae8b-cad0-46ec-bf34-adab0960fc41)

Current number of CLIENTS is now 0. By connecting to the WLANS, these numbers should change.
To SEE a list of the CLIENTS connected, click the left-hand side “CLIENTS” tab

![image](https://github.com/psaumur/CCNA/assets/106411237/b6eefbd8-f79e-4dc6-90e6-95a8c0c17849)

![image](https://github.com/psaumur/CCNA/assets/106411237/75d359fe-dc41-4d87-9351-e1da0ebbb8c7)

---

ADDTIONAL WLC FEATURES

WIRELESS tab showing a list of the APs currently in the NETWORK

![image](https://github.com/psaumur/CCNA/assets/106411237/29f5608e-9edb-4c6e-9382-998deedd4c72)

Clicking on an AP shows information and configuration settings for it

![image](https://github.com/psaumur/CCNA/assets/106411237/7d87bbcc-ed95-47b6-b966-fb95f5bb7f29)

---

MANAGEMENT tab allows you change the ways you can MANAGE the WLC

Clicking “Mgmt Via Wireless” allows you change if you can access MANAGEMENT via WI-FI

![image](https://github.com/psaumur/CCNA/assets/106411237/605361a0-c8da-47fc-bca3-af09751838dd)

![image](https://github.com/psaumur/CCNA/assets/106411237/e13bdcea-cb87-4e38-9dd4-711079761987)

---

SECURITY tab can allow us to create ACCESS LISTS

![image](https://github.com/psaumur/CCNA/assets/106411237/7eddccfb-07cd-4ba9-914e-54161a4b10f3)

First, NAME the ACL and what kind of IP ADDRESS it’s for

![image](https://github.com/psaumur/CCNA/assets/106411237/e9f303bc-9078-4ff2-be86-f63fb9877008)

CLICK “Add New Rule” to specify the ACL Rules (What traffic can pass)

![image](https://github.com/psaumur/CCNA/assets/106411237/4637053c-042d-4afc-acf8-27e914698c00)

![image](https://github.com/psaumur/CCNA/assets/106411237/c9d26aa3-c277-45ac-8f74-1dbd11e1bda5)

![image](https://github.com/psaumur/CCNA/assets/106411237/afbdb580-5383-4f32-9713-708f0a4ebb7e)

We now need to APPLY the ACL (just like applying it to an INTERFACE on a ROUTER)

Click “CPU ACL” from the left-hand menu

![image](https://github.com/psaumur/CCNA/assets/106411237/3eeee534-2071-47df-97f6-639e46d54b94)

Select the new ACL from the pull-down list and then click “APPLY”

![image](https://github.com/psaumur/CCNA/assets/106411237/7c18a89c-cad3-4f54-b6e5-6d5956edbd37)

![image](https://github.com/psaumur/CCNA/assets/106411237/6319e0ad-4c65-418d-920b-3c1f43ae4b55)

# 59. INTRODUCTION TO NETWORK AUTOMATION

WHY NETWORK AUTOMATION

- Previous versions of the CCNA focused on the traditional model of managing / controlling networks
- The current version focuses on the traditional model as well, but CCNA candidates are expected to have a basic understanding of various topics related to network automation
- In the traditional model, engineers manage devices one at a time by connecting to their CLI via SSH

---

DOWNSIDES OF CONFIGURING DEVICES ONE-BY-ONE

- Typos and other small mistakes are common
- It is time-consuming and very inefficient in large-scale networks
- It is difficult to ensure that all devices ADHERE to the organization’s STANDARD CONFIGURATION

---

BENEFITS OF NETWORK AUTOMATION

- Human Error (Typos, etc) is reduced
- Networks become much more scalable and implemented in a fraction of the time
    - New deployments
    - Network-wide changes
    - Troubleshooting
- Network-wide policy compliance can be assured
    - Standard configurations
    - Software versioning

- The improved efficiency of network operations reduces the OP-EX (operating expenses) of the network. Each task requires fewer man-hours

```
There are various tools / methods that can be used to automate tasks in the network

- SDN (Software-Defined Networking)
- Ansible
- Puppet
- Python scripts
- etc…
```

---

LOGICAL “PLANES” OF NETWORK FUNCTIONS

**What does a ROUTER do?**

- It forwards messages between networks by examining information in the Layer 3 header
- It uses a routing protocol like OSPF to share route information with other routers and build a routing table
- It uses ARP to build an ARP table, mapping IP Addresses to MAC Addresses
- It uses Syslog to keep logs of events that occur
- and MUCH more…

**What does a SWITCH do?**

- It forwards messages within a LAN by examining information in the Layer 2 header
- It uses STP to ensure there are no Layer 2 loops in the network
- It builds a MAC address table by examining the Source MAC address of frames
- It uses Syslog to keep logs of events that occur
- It allows a user to connect to it via SSH and manage it

---

The various functions of network devices can be logically divided up (categorized) into *PLANES*

```
- DATA PLANE
- CONTROL PLANE
- MANAGEMENT PLANE
```


- The operations of the MANAGEMENT PLANE and the CONTROL PLANE are usually managed by the CPU
- However, this is not desirable for DATA PLANE operations because CPU processing is slow (relatively speaking)
- Instead, a specialized hardware ASIC (Application-Specific Integrated Circuit) is used.
    - ASICs are chips built for a specific purpose
- Using a SWITCH, as an example:
    - When a FRAME is received, the ASIC (not the CPU) is responsible for the switching logic
    - The MAC Address table is stored in a kind of memory called TCAM (Ternary Content-Addressable Memory)
        - Another common name for the MAC Address table is CAM TABLE
    - The ASIC feeds the DESTINATION MAC address of the FRAME into the TCAM which returns the matching MAC Address table entry
    - The FRAME is then forwarded out of the appropriate DEVICE
- Modern ROUTERS also use a similar hardware DATA PLANE: An ASIC designed for forwarding logic, and tables store in TCAM

---

A SIMPLE SUMMARY:

>- When a DEVICE receives CONTROL / MANAGEMENT traffic (destined for itself), it will be processed in the CPU
>- When a DEVICE receives DATA traffic which should pass through the DEVICE, it is processed by the ASIC for maximum speed

---

DATA PLANE

- All tasks involved in forwarding USER  DATA / TRAFFIC from one INTERFACE to another are part of the DATA PLANE
- A ROUTER receives a message, looks for the most specific matching ROUTER in its ROUTING TABLE, and forwards it out of the appropriate INTERFACE to the next hop
    - It also de-encapsulates the original LAYER 2 header, and re-encapsulates with a new header destined for the next hop’s MAC address
- A SWITCH receives a message, looks at the DESTINATION MAC Address, and forwards it out of the appropriate INTERFACE (or FLOODS it)
    - This includes functions like adding / removing 802.1q VLAN tags
- NAT (changing the SRC / DST addresses before forwarding) is part of the DATA PLANE
- Deciding to forward / discard messages due to ACL’s, port-security, etc. is part of the DATA PLANE
- The DATA PLANE is also called the ‘FORWARDING PLANE’

![image](https://github.com/psaumur/CCNA/assets/106411237/6a72186b-2956-45f6-8643-801caa2cb28e)

---

CONTROL PLANE

- How does a DEVICE’s DATA PLANE make its forwarding decisions?
    - ROUTING TABLE
    - MAC ADDRESS table
    - ARP table
    - STP
    - etc…
    
- Functions that build THESE tables (and other functions that influence the DATA PLANE) are part of the CONTROL PLANE

- The CONTROL PLANE *controls* what the DATA PLANE does, for example by building the ROUTER’s ROUTING TABLE

- The CONTROL PLANE performs *overhead* work
    - OSPF itself doesn’t forward user data packets, but it informs the DATA PLANE about HOW packets should be forwarded
    - STP itself isn’t directly involved in the process of forwarding FRAMES, but it informs the DATA PLANE about which INTERFACES should and shouldn’t be used to forward FRAMES
    - ARP messages aren’t user data but they are used to build an ARP TABLE which is used in the process of forwarding data

![image](https://github.com/psaumur/CCNA/assets/106411237/4c21b082-5d6e-4388-94c5-bebf33b50c8d)

---

MANAGEMENT PLANE

- Like the CONTROL PLANE, the MANAGEMENT PLANE performs overhead work
    - However, the MANAGEMENT PLANE doesn’t directly affect the forwarding of messages in the DATA PLANE
- The MANAGMENT PLANE consists of PROTOCOLS that are used to manage devices
    - SSH / TELNET : Used to connect to the CLI of a DEVICE to configure / manage it
    - SYSLOG : Used to keep logs of events that occur on the device
    - SNMP : Used to monitor the operations of the device
    - NTP : Used to maintain accurate time on the device

![image](https://github.com/psaumur/CCNA/assets/106411237/3cfffa40-f4cb-4042-8778-139605c2eb26)

---

SOFTWARE-DEFINED NETWORKING (SDN)

- SOFTWARE-DEFINED NETWORKING (SDN) is an approach to networking that centralizes the CONTROL PLANE into an application called a *CONTROLLER*
- SDN is also called SOFTWARE-DEFINED-ARCHITECTURE (SDA) or CONTROLLER-BASED NETWORKING
- Traditional CONTROL PLANES use a distributed architecture
    - For example:
        - Each ROUTER in the NETWORK runs OSPF and the ROUTERS share routing information and then calculate their preferred routes to each destination
- An SDN CONTROLLER centralized CONTROL PLANE functions like calculation routes
    - That is just an example and how much of the CONTROL PLANE is centralized varies greatly
- The CONTROLLER can interact programmatically with the NETWORK DEVICE using APIs (Application Programming Interface)

![image](https://github.com/psaumur/CCNA/assets/106411237/05c4c5d9-5ba4-480c-9c13-72fa1f7937db)

---

SOUTHBOUND INTERFACE (SBI)

- The SBI is used for communications between the CONTROLLER and the NETWORK DEVICES it controls
- It typically consists of a COMMUNICATION PROTOCOL and API (Application Programming Interface)

- APIs facilitate data exchanges between programs
    - DATA is exchanged between the CONTROLLER and the NETWORK DEVICES
    - An API on the NETWORK DEVICES allows the CONTROLLER to access information on the DEVICES, control their DATA PLANE TABLES, etc.
- Some examples of SBIs :
    - OpenFlow
    - Cisco OpFlex
    - Cisco OnePK (Open Network Environment Platform Kit)
    - NETCONF

---

 NORTHBOUND INTERFACE (NBI)

- Using the SBI, the CONTROLLER communicates with the managed DEVICES and gathers information about them:
    - The DEVICES in the NETWORK
    - The TOPOLOGY (how the DEVICES are connected together)
    - The available INTERFACES on each DEVICE
    - Their CONFIGURATIONS
- The NORTHBOUND INTERFACE (NBI) is what allows us to:
    - Interact with the CONTROLLER
    - Access the DATA it gathers about the NETWORK
    - Program the NETWORK
    - Make changes to the NETWORK via the SBI

- A REST API (Representational State Transfer) is used on the controller as an interface for APPS to interact with it
- OSGi (Java Open Services Gateway Initiative) - Java based NBI API

- DATA is sent in a structured (*serialized*) format such as JSON or XML
    - This makes it easier for programs to use the DATA

![image](https://github.com/psaumur/CCNA/assets/106411237/d980626f-f731-46a4-ba14-72c3d21f2fd3)

---

AUTOMATION IN TRADITIONAL NETWORKS VS SDN

- Networking tasks can be automated in traditional NETWORK architectures too:
    - SCRIPTS can be written (ie: using Python) to push commands to many DEVICES at once
    - Python with good use of REGULAR EXPRESSIONS can parse through “show” commands to gather information about network devices
    
- However, the robust and centralized DATA collected by SDN CONTROLLERS greatly facilitates these functions
    - The CONTROLLER collects information about all DEVICES in the NETWORK
    - NORTHBOUND APIs allow APPS to access information in a format that is easy for programs to understand (ie: JSON and XML)
    - The centralized DATA facilitates network-wide analytics
- SDN Tools can provide the benefits of automation without the requirement of third-party scripts and apps.
    - You don’t need expertise in automation to make use of SDN Tools
    - However, APIs allow third-party applications to interact with the CONTROLLER, which can be very powerful


>💡 Although SDN and automation aren’t the same thing, the SDN architecture greatly facilitates the automation of various tasks in the network via the SDN CONTROLLER and APIs

# 60. JSON, XML, AND YAML

DATA SERIALIZATION

- DATA SERIALIZATION is the process of converting DATA into a standardized format/structure that can be stored (in a file) or transmitted (over a network) and reconstructed later (ie: by a different application)
    - This allows the DATA to be communicated between applications in a way both APPLICATIONS understand.

- DATA SERIALIZATION languages allow us to represent *variables* with text

![image](https://github.com/psaumur/CCNA/assets/106411237/f09eeeba-7779-40c8-af18-f1227bf0cf47)

---

JSON (JAVASCRIPT OBJECT NOTATION)

- JSON (JAVASCRIPT OBJECT NOTATION) **is an open standard FILE FORMAT and DATA INTERCHANGE FORMAT that uses human-readable text to store and transmit data objects

- It is standardized in RFC 8259 (https://datatracker.ietf.org/doc/html/rfc8259)
- It was derived from JavaScript, but it is language-independent and many modern programming languages are able to generate and read JSON data
    - REST APIs often use JSON
- *Whitespace* is insignificant

- JSON can represent FOUR “primitive” DATA Types:
    - String
    - Number
    - Boolean
    - Null

- JSON also has TWO “structured” DATA Types:
    - Object
    - Array

---

JSON PRIMITIVE DATA TYPES:

- A STRING is a text value. It is surrounded by double quotes “ “
    - “Hello”
    - “Five”
    - “5”

- A NUMBER is a numeric value. It is NOT surrounded by quotes
    - 5
    - 100
    
- A BOOLEAN is a DATA Type that has only TWO possible values, not surrounded by quotes
    - true
    - false

- A NULL value represents the intentional absence of any object value. It is not surrounded by quotes
    - null

---

JSON STRUCTURED DATA TYPES:

- An OBJECT is an unordered list of *key-value pairs* (variables)
    - Sometimes called a DICTIONARY
    - OBJECTS are surrounded by curly brackets {}
    - The *key* is a STRING
    - The *value* is any valid JSON DATA Type (string, number, boolean, null, object, array)
    - The *key* and *value* are separated by a colon :
    - If there are multiple key-value pairs, each pair is separated by a comma

![image](https://github.com/psaumur/CCNA/assets/106411237/24a15571-bb9f-43b4-889f-69f23ffb91bc)

![image](https://github.com/psaumur/CCNA/assets/106411237/b66f041d-2449-43f0-8a04-2c0da5391411)

![image](https://github.com/psaumur/CCNA/assets/106411237/54d69eed-4369-4ef6-a437-6b5ecce14586)

- An ARRAY is a series of *values* separated by commas
    - Not *key-value pairs*
    - The values do NOT have to be the same DATA Type

![image](https://github.com/psaumur/CCNA/assets/106411237/3212f472-f966-49e5-9b9a-7bedcfe47487)

![image](https://github.com/psaumur/CCNA/assets/106411237/f8075e93-2be7-4b2e-a2af-968961bbc5a7)

---

XML (EXTENSIBLE MARKUP LANGUAGE)

- XML (EXTENSIBLE MARKUP LANGUAGE) was developed as a MARKUP language, but is now used as a general data serialization language
    - Markup languages (ie: HTML) are used to format text (font, size, color, headings, etc)
    - XML is generally less human-readable than JSON
    - Whitespace is insignificant
    - Often used by REST APIs
    - <key> value </key> (similar to HTML)

![image](https://github.com/psaumur/CCNA/assets/106411237/f954b0ef-f563-4536-94c8-334b6d8f97c6)

![image](https://github.com/psaumur/CCNA/assets/106411237/948dae9e-b59b-4607-8e6d-b39837baba70)

---

YAML (YAML AIN’T MARKUP LANGUAGE)

- YAML originally meant *YET ANOTHER MARKUP LANGUAGE* but to distinguish its purpose as a data-serialization language rather than a markup language, it was repurposed to *YAML AINT MARKUP LANGUAGE*
- YAML is used by the network automation tool ANSIBLE (covered later in the course)
- YAML is VERY Human-Readable
- Whitespace **is significant** (unlike JSON and XML)
    - Indentation is very important
- YAML files start with - - - (three dashes)
- - is used to indicate a list
- Keys and Values are represented as key : value

![image](https://github.com/psaumur/CCNA/assets/106411237/ecfa3659-4bc3-4596-9f11-10d2644eac1a)

COMPARISON BETWEEN JSON and YAML using the same DATA

![image](https://github.com/psaumur/CCNA/assets/106411237/16e0e98b-5653-4f8a-a388-1706f91a30d4)

# 61. REST APIS

API REVIEW

- An API (Application Programming Interface) is a software interface that allows two applications to communicate with each other.
- APIs are essential not just for network automation but for all kinds of applications
- In SDN Architecture, APIs are use to communicate between apps and the SDN controller (via the NBI) and between the SDN controller and the network devices (via the SBI)
- The NBI typically uses REST APIs
- NETCONF and RESTCONF are popular Southbound APIs

---

CRUD OPERATIONS AND HTTP VERBS

- CRUD ( CREATE, READ, UPDATE, DELETE) refers to the operations we perform using REST APIs

- CREATE :
    - Used to CREATE new variables and set their initial values
        - Example:  create a variable “ip_address” and set the value to “10.1.1.1”

- READ :
    - Used to READ the value of a variable
        - Example: Read the value of variable “ip_address” (”10.1.1.1”)

- UPDATE :
    - Used to CHANGE / UPDATE the value of a variable
        - Example: Change the value of “ip_address” from “10.1.1.1” to “10.2.3.4”
    
- DELETE :
    - Used to DELETE variables
        - Example: Delete variable “ip_address”

- HTTP uses *verbs* (aka. methods) that map to these CRUD operations
- REST APIs typically use HTTP

![image](https://github.com/psaumur/CCNA/assets/106411237/b25ca0c6-5a79-4dcc-afde-096b1868219b)

---

HTTP REQUEST :

- When an HTTP client sends a request to an HTTP server, the HTTP header includes information like this:
    - An HTTP Verb (ie: GET)
    - A URI (Uniform Resource Identifier) indicating the resource it is trying to access

![image](https://github.com/psaumur/CCNA/assets/106411237/e859d701-50bc-475a-89ca-5267efaeaf87)

An example of a URI (demonstrated later)

![image](https://github.com/psaumur/CCNA/assets/106411237/23dc6233-ce58-44c6-805b-05f1cbc7b933)

- The HTTP request can include additional headers which pass additional information to the server.

Check the list at  https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers

![image](https://github.com/psaumur/CCNA/assets/106411237/010f553f-971d-49d8-be1b-dd0eff5854ac)

- An example would be an ACCEPT header, which informs the server about the types(s) of data that can be sent back to the client.
    - Example: **Accept: application/json** or **Accept: application/xml**

- You can also view standard HTTP header fields with some examples at https://en.wikipedia.org/wiki/List_of_HTTP_header_fields

- When a REST client makes an API call (request) to a REST server, it will send an HTTP request like the one above

> 💡 REST APIs do NOT have to use HTTP for communication, although HTTP is the most common choice 

---

HTTP RESPONSE :

- The server’s response will include a STATUS CODE indicating if the request succeeded or failed, as well as other details
- The FIRST digit indicates the class of the response:
    - 1xx : Informational - request was received, continuing process
    - 2xx : Successful - request was successfully received, understood, and accepted
    - 3xx : Redirection - further action needs to be taken in order to complete the request
    - 4xx : Client Error - request contains bad syntax or cannot be fulfilled
    - 5xx : Server Error - server failed to fulfill an apparently valid request

![image](https://github.com/psaumur/CCNA/assets/106411237/1ab2d4c3-11c1-4189-9a44-ae0f6405536c)

Examples of each HTTP Response class:

- 1xx Informational
    - 102 Processing indicates that the server received the request and is processing it but the response is not available yet

- 2xx Successful
    - 200 OK **indicates that the request succeeded
    - 201 Created indicates the request succeeded and a new resource was created

- 3xx Redirection
    - 301 Moved Permanently indicates that the request resource has been moved and the server indicates its new location

- 4xx Client Error
    - 403 Unauthorized means the client must authenticate to get a response
    - 404 Not Found means the requested resource was not found

- 5xx Server Error
    - 500 Internal Server Error means the server encountered something unexpected that it doesn’t know how to handle

---

REST APIs

- REST stands for Representational State Transfer
- REST APIs are also know as REST-based APIs or RESTful APIs
    - REST isn’t a specific API. Instead it describes a set of rules about how the API should work
    
- The SIX constraints of RESTful architecture are:
    - Stateless
    - Layered system
    - Uniform Interface
    - Client-Server
    - Cacheable or non-cacheable
    - Code-on-Demand (optional)

- For applications to communicate over a network, networking protocols must be used to facilitate those communications
    - For REST APIs, HTTP(S) is the most common choice

---

REST: Client-Server

- REST APIs use a client-server architecture
- The client uses API calls (HTTP requests) to access the resources on the server
- The separation between the client and server means they can both change and evolve independently of each other
    - When the client application changes or the server application changes, the interface between them must not break

![image](https://github.com/psaumur/CCNA/assets/106411237/e39d0588-8e4c-441b-97b9-c2345bf09342)

---

REST: Stateless

- REST APIs exchanges are STATELESS
- This means that each API exchange is a separate event, independent of all past exchanges between the client and server
    - The server does not store information about previous requests from the client to determine how it should respond to new requests
- If authentication is required, this means that the client must authenticate with the server for each request it makes
- TCP is an example of a STATEFUL protocol
- UDP is an example of  STATELESS protocol

** Although REST APIs use HTTP, which uses TCP (STATEFUL) as it’s LAYER 4 protocol, HTTP and REST APIs themselves aren’t STATEFUL. The functions of each layer are separate ! 

---

REST: Cacheable or Non-Cacheable 

- REST APIs must support caching of data
- *Caching* refers to storing data for future use
    - Example :
        - Your computer might cache many elements of a web page so it doesn’t have to retrieve the entire page every time you visit. This improves performance for the client and reduces load on the server
- Not all resources have to be cacheable but cacheable resources MUST be declared as cacheable

FOR THE CCNA

![image](https://github.com/psaumur/CCNA/assets/106411237/d3747417-a936-498c-99d3-f508d436d451)

---

REST API CALLS USING CISCO DEVNET

- “Cisco DevNet is Cisco’s developer program to help developers and IT professionals who want to write applications and develop integrations with Cisco products, platforms, and API’s”

- DevNet offers lots of free resources such as courses, tutorials, labs, sandboxes, documentation, etc to learn about AUTOMATION and develop your skills

- There is also a DevNet certification track that you can pursue if you are interested in AUTOMATION

- We will use their Cisco DNA Center Sandbox to send a REST API call using Postman
    - DNA Center is one of Cisco’s SDN Controllers (covered in more detail later)
    - Postman is a platform for building an using APIs
---

TO START:

- Make an account on [developer.cisco.com](http://developer.cisco.com) (Used my NetAcademy login)
- Make an accounts on [postman.com](http://postman.com) and download the desktop app (https://www.postman.com/downloads) - Used my [gmail.com](http://gmail.com) account

# 62. SOFTWARE DEFINED NETWORKING (SDN)

SD REVIEW

- SOFTWARE DEFINED NETWORKING (SDN) is an approach to networking that centralizes the control plane into an application called a *controller*
- Traditional control planes use a distributed architecture
- A SDN controller centralizes control plane functions like calculating routes
- The controller can interact programmatically with the network devices using APIs
- The SBI (South Bound Interface) is used for communications between the controller and the network device it controls
- The NBI (North Bound Interface) is what allows us to interact with the controller with our scripts and applications

SDN ARCHITECTURE

![image](https://github.com/psaumur/CCNA/assets/106411237/9d7e1a89-3537-48cc-a410-cef352b6a2cb)

---

CISCO SD-ACCESS

- Cisco SD-ACCESS is Cisco’s SDN solution for automating campus LANs
    - ACI (Application Centric Infrastructure) is their SDN solution for automating data center networks
    - SD-WAN is their SDN solution for automating WANs
- Cisco DNA (Digital Network Architecture) Center is the controller at the center of SD-Access

![image](https://github.com/psaumur/CCNA/assets/106411237/4c1662ee-490c-4eee-8970-550ca60feabb)

- The UNDERLAY is the underlying physical network of devices and connections (including wired and wireless) which provide IP connectivity (ie: using IS-IS)
    - Multilayer Switches and their connections

![image](https://github.com/psaumur/CCNA/assets/106411237/41bb11dd-31c9-493e-9fec-af847f0732dc)

- The OVERLAY is the virtual network built on top of the physical underlay network

![image](https://github.com/psaumur/CCNA/assets/106411237/99f48b9e-ed68-4c11-b456-d0f6ccf13fed)

- The FABRIC is the combination of the OVERLAY and UNDERLAY; the physical and virtual network as a whole

![image](https://github.com/psaumur/CCNA/assets/106411237/35cf981c-337d-4117-9124-9f210e85bff3)

---

SD-ACCESS UNDERLAY

- The UNDERLAY’s purpose is to support the VXLAN tunnels of the OVERLAY
- There are THREE different ROLES for switches in SD-ACCESS:
    - EDGE NODES : Connect to End HOSTS
    - BORDER NODES : Connect to devices outside of the SD-ACCESS Domain ; ie: WAN routers
    - CONTROL NODES : Uses LISP (Locator ID Separation Protocol) to perform various control plane functions
    
- You can add SD-ACCESS on top of the existing network (*brownfield deployment*) if your network hardware and software supports it
    - Google ‘Cisco SD-ACCESS compatibility matrix’ if you are curious
    - In this case DNA CENTER won’t configure the UNDERLAY

- A NEW deployment (*greenfield deployment)* will be configured by DNA CENTER to use the optimal SD-ACCESS UNDERLAY:
    - ALL Switches are LAYER 3 and use IS-IS as their ROUTING PROTOCOL
    - All Links between Switches are ROUTED PORTS. This means STP is not needed
    - EDGE NODES (ACCESS SWITCHES) act as the the DEFAULT GATEWAY of END HOSTS *(Routed Access Layer)*

![image](https://github.com/psaumur/CCNA/assets/106411237/0315f1e5-d9c6-47ce-acf2-1de6f14ac89c)

![image](https://github.com/psaumur/CCNA/assets/106411237/84d48992-30f9-45cf-856a-089ce00d0641)

---

SD-ACCESS OVERLAY

- LISP (Locator ID Separation Protocol) provides the control plane of SD-ACCESS
    - A list of mappings of EIDs (endpoint identifiers) to RLOCs (routing locators) is kept
    - EIDs identify END HOSTS connected to EDGE SWITCHES
    - RLOCS identify the EDGE SWITCH which can be used to reach the END HOST
    - There is a LOT more detail to cover about LISP but I think you can see how it differs from traditional CONTROL PLANE
    
- Cisco TrustSec (CTS) provides policy control (QoS, Security Policy, etc.)

- VXLAN provides the DATA PLANE of SD-ACCESS

![image](https://github.com/psaumur/CCNA/assets/106411237/8fd0bb65-31df-4db5-a79c-044c68c37b01)

![image](https://github.com/psaumur/CCNA/assets/106411237/b4c017b1-cc59-4305-9924-f25a5445a36b)

![image](https://github.com/psaumur/CCNA/assets/106411237/5adcaf16-4caf-4de2-9b8f-3e777c841bc6)

---

CISCO DNA CENTER

- Cisco DNA Center has TWO MAIN ROLES:
    - The SDN Controller in SD-ACCESS
    - A network manager in a traditional network (non-SD-ACCESS)
- DNA Center is an application installed on Cisco UCS server hardware
- It has a REST API which can be used to interact with DNA Center
- The SBI supports protocols such as NETCONF and RESTCONF (as well as traditional protocols like Telnet, SSH, and SNMP)
- DNA Center enables *Intent-Based Networking* (IBN)
    - The goal is to allow the engineer to communicate their intent for network behavior to DNA Center, and then DNA Center will take care of the details of the actual configurations and policies on devices

- Traditional security policies using ACLs can become VERY cumbersome
    - ACLs can have thousands of entries
    - The intent of entries is forgotten with time and as engineers leave and new engineers take over

- DNA Center allows the engineer to specify the intent of the policy
    - Examples :
        - THIS group of users can’t communicate with THAT group
        - THIS group can access THIS server but not THAT server
    - DNA CENTER will take care of the exact details of implementing this policy

![image](https://github.com/psaumur/CCNA/assets/106411237/30773f46-3564-4d66-a175-20962d1569dd)

---

>For more details, you can check out [sandboxdnac.cisco.com](http://sandboxdnac.cisco.com) (User: devnetuser, Password: Cisco123!)

---

DNA CENTER NETWORK MANAGEMENT VS. TRADITIONAL

Traditional Management :

- DEVICES are configured one-by-one via SSH or Console connection
- DEVICES are manually configured via Console connection before being deployed
- Configurations and polices are managed per-device
- New network deployments can take a long time due to the manual labor required
- Errors and failures are more likely due to increased manual effort

DNA CENTER-based Network Management :

- DEVICES are centrally managed and monitored from the DNA CENTER GUI or other applications using it’s REST API
- The Administrator communicates their intended network behavior to DNA CENTER, which changes those intentions into configurations on the managed network devices
- Configurations and policies are centrally managed
- Software versions are also centrally managed. DNA CENTER can monitor cloud servers for new versions and then update the managed devices
- New network deployments are much quicker. New devices can automatically receive their configurations from DNA CENTER without manual configuration

![image](https://github.com/psaumur/CCNA/assets/106411237/cb9e0184-6b45-4dcc-85ae-cef3245c1629)

# 63. ANSIBLE, PUPPET, AND CHEF

CONFIGURATION DRIFT

- CONFIGURATION DRIFT is when individual changes made over time causes a device’s configuration to deviate from the standard / correct configurations as defined by the company
    - Although each device will have unique parts of its configurations (IP Addresses, hostname, etc) most of a device’s configuration is usually defined in standard templates designed by the network architects / engineers of the company
    - As individual engineers make changes to devices (for example, to troubleshoot and fix network issues, test configurations, etc), the configuration of a device can drift away from the standard.
    - Records of these individual changes and their reasons aren’t kept
    - This can lead to future issues
- Even without automation tools, it is best to have standard configuration management practices.
    - When a change is made, save the config as a text file and place it in a shared folder
        - A standard naming system like (*hostname_yyyymmdd)* might be used.
        - There are flaws to this system, as an engineer might forget to place the new config in the folder after making changes. Which one should be considered the “CORRECT” config?
        - Even if configurations are properly saved like this, it doesn’t guarantee that the configurations actually match the standard
---

CONFIGURATION PROVISIONING

- CONFIGURATION PROVISIONING refers to how configuration changes are applied to devices
    - This includes configuring new devices, too
- Traditionally, configuration provisioning is done by connecting to devices one-by-one via SSH
    - This is not practical in large networks
- Configuration management tools like Ansible, Puppet, and Chef allow us to make changes to devices on a mass scale with a fraction of time and effort.

- TWO ESSENTIAL COMPONENTS:
    - Templates
    - Variables

![image](https://github.com/psaumur/CCNA/assets/106411237/0c74b2a6-1ce7-4758-b6b8-340594d567c3)

---

INTRO TO CONFIGURATION MANAGEMENT TOOLS

- CONFIGURATION MANAGEMENT TOOLS are network automation tools that facilitate the centralized control of large numbers of network devices
- The option you need to be aware of for the CCNA are Ansible, Puppet, and Chef
- These tools were originally developed after the rise of VMs, to enable server system admins to automate the process of creating, configuring, and removing VMs
    - However, they are also widely used to manage network devices
    
- These tools can be used to perform tasks such as :
    - Generate configurations for new devices on a large scale
    - Perform configuration changes on devices (all devices in your network, or certain subset of devices)
    - Check device configurations for compliance with defined standards
    - Compare configurations between devices, and between different versions of configurations on the same device

![image](https://github.com/psaumur/CCNA/assets/106411237/f9eb7783-5e42-4cfe-aec8-8b57cd316f4d)

---

ANSIBLE 

- ANSIBLE is a configuration management tool owned by Red Hat
- Ansible itself is written in Python
- Ansible is *agentless*
    - It doesn’t require any special software to run on the managed devices
- Ansible uses SSH to connect to devices, make configuration changes, extract info, etc
- Ansible uses a *push* model. The Ansible server (Control node) uses SSH to connect to managed devices and *push* configuration changes to them
    - Puppet and Chef use a *pull* model
    
- After installing Ansible itself, you must create several text files:
    - PLAYBOOKS :
        - These files are “blueprints of automation tasks”
        - They outline the logic and actions of the tasks that Ansible should do
        - Written in YAML
    - INVENTORY :
        - These files list the devices that will be managed by Ansible, as well as characteristics of each device such as their device role (Access Switch, Core Switch, WAN Router, Firewall, etc.)
        - Written in INI, YAML, or other formats
    - TEMPLATES :
        - These files represent a device’s configuration file, but specific values for variables are not provided.
        - Written in JINJA2 format
    - VARIABLES :
        - These files list variables and their values.
        - These values are substituted into the templates to create complete configuration files.
        - Written in YAML

![image](https://github.com/psaumur/CCNA/assets/106411237/ba2a68b5-7661-4eff-bd5f-8c32bde354da)

---

PUPPET 

- PUPPET is a configuration management tool written in RUBY
- Puppet is typically agent-based
    - Specific software must be installed on the managed devices
    - Not all Cisco devices support a Puppet agent
    
- It CAN be run *agentless,* in which a proxy agent runs on an external host, and a proxy agent uses SSH to connect to the managed devices and communicate with them
- The Puppet server is called the “Puppet master”
- Puppet uses a PULL model (clients “pull” configurations from the Puppet master)
    - Clients use TCP 8140 to communicate with the Puppet master
- Instead of YAML, it uses a proprietary language for files
- Text files required on the Puppet master include:
    - MANIFEST :
        - The file defines the desired configuration state of a network device
    - TEMPLATES :
        - Similar to Ansible templates.
        - Used to generate MANIFESTS

![image](https://github.com/psaumur/CCNA/assets/106411237/ec26ad33-7534-4f15-93f0-4557337bfaec)

---

CHEF

- CHEF is a configuration management tool written in RUBY
- CHEF is Agent-Based
    - Specific software must be installed on the managed devices
    - Not all Cisco devices support a CHEF agent
- CHEF uses a PULL model
- The server uses TCP 10002 to send configurations to clients
- Files use a DSL (Domain-Specific Language) based on Ruby
- Text files used by CHEF include:
    - RESOURCES :
        - The “ingredients” in a RECIPE.
        - Configuration objects managed by CHEF
    - RECIPES :
        - The “recipes” in a COOKBOOK.
        - Outlines the logic and actions of the tasks performed on the resources
    - COOKBOOKS :
        - A set of related RECIPES grouped together
    - RUN-LIST :
        - An ordered list of RECIPES that are run to bring a device to the desired configuration state

![image](https://github.com/psaumur/CCNA/assets/106411237/eaf5be1b-3635-4806-bb7a-f397ffa1b411)

---

MEMORIZE THIS CHART FOR THE CCNA

![image](https://github.com/psaumur/CCNA/assets/106411237/a4d212e6-df46-45d1-a2ca-3e55220c4b5c)

