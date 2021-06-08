# Networking
Collection of devices exchanging data.

## Network components
**Host** : Computer connected to a network, helps communicate with other hosts in the network. Hosts include clients and servers.
**Server** : Host whose software allow them to provide services to other hosts (client)
**Client** : Host that requests the service

## Server-client architechture
Structure that partitions tasks/ workloads between the providers (server) of a resource/server and service requesters (client).

## Peer-to-peer architecture 
Here the workload is partitioned between peers. Peers are equally privileged and equipotent. Both peers can request from each other.
- e.g Network print sharing: a printer is connected to one device via USB, this device is then configured to a shared printer. Other devices in the network can then access the shared printer as a resource on te network.

## Intermediary device 
Networking device positioned between a remote access service (RAS) and a RAS client.
- Switches and wireless access points (network access)
- Routers
- Firewalls

## Network media
- Metal wired (usually Cu) cable
- Fiber optic (drawing glass/ plastic, diameter is slightly thicker than a human hair)
- Wireless

## End device
A source or destination device in a networked system e.g a user's PC.

## Network type is based on
- Size of area covered
- Number of users connected
- Type of serices
- Area of responsibility

	- LAN: Local Area Network (house/office)
	- WAN : Wide Area Network (extends over a large geographic area for the primary purpose of computer networking)


## Internet
### Internet interconnected network
WAN/ LAN - can be wired, fiber optic, wireless (public).
### Intranet
LAN/WAN - Network internal to an organisation (private)
### Extranet
Controlled, private network that allows third party partners to gain information about a company, without granting access to an organisations entire network.

Private networks are not routable like public networks.

## Communication fundamentals
A source (sender) and destination (reader) communicate over a channel. The purpose is to transmit a message over the channel from source to destination.

## Message delivery options
- Unicast: delivered to one destination
- Multicast: delivered to a set of destinations
- Broadcast: delivered to all destinations in a network

## Protocol standards
Group of interelated protocols

### Open System Interconnection (OSI) model, a conceptual framework used to describe the functions of a network system.
**Physical Layer**
Lowest layer of the OSI model, electrically transmits raw unstructured data bits across the network from the physical layer of the sending device to the physical layer of the receiving device e.g voltages, pin layout, cabling.
**Data Link Layer**
Directly connected nodes are used to perform node-to-node data transfer where data is packaged into frames. Data link layer also corrects errors that may have occurred at the physical layer.
- Data link layer encompasses two sub-layers, Media Access Control (MAC), provides flow control and multiplexing for device transmissions over a network.
- Logical Link Control (LLC) provides flow and error control over the physical medium.
**Network Layer**
Responsile for receiving frames from the data link layer and delivering them to their intended destinations based on the addresses contained inside the frame.
- Network layer finds the destination by using logical addresses such as IP (internet protocol).
- Routers are crucial component used to quite literally route information where it needs to go between networks
**Transport Layer**
Transport layer manages the delivery and error checking of data packets.
- TCP: Transmission Control Protocol
- UDP: User Datagram Protocol
**Session Layer**
Controls conversation between different computers.
**Presentation Layer**
Formats or translates data for the application layer based on the syntax that the application accepts.
**Application Layer**
The end user and the application layer interact directly with the software application (top layer).


In TCP/IP session, presentation, application are considered as application.
Application layer
Transport layer
Internet layer
Network access layer

Layers work together by encapsulation - when data moves from upper layer to lower layer of TCP/IP protocol stack, during an outgoing transmission, each layer includes a bundle of relevant information called "header" along with the actual data.
Decapsulation - each layer takes out info from previous layer.

## Port number
Communication end point.
- Identifies a specific process/ type of network service.
- Port numbers are always associated with an IP address of a host and the type of transport used for communication.
- Source ports and destination ports form a channel/

###Port numbers
0-65535 (2^16) 16 bits

0-1023: well known ports: reserved for popular services, e.g email
1024-49151: registered ports e.g applications
49152-65535: private/dynamic ports

Some examples of TCP port numbers:
**TCP 20** : FTP file transfer protocol - data transfer
**TCP 21** : FTP control
**TCP 22** : SSH (secure shell) access port host
**TCP 23** : telnet 
**TCP 25** : SMTP - simple mail tranfer protocol
**TCP 80** : HTTP (web) hyper text transfer protocol

Bandwidth: maximum rate of data transfer accross a given path e.g bits per second

## Positional Number System
### Binary Numeral System (0,1)
**2^n** - radix=2, position in number=n

| Radix              | 2   | 2   | 2   | 2   | 2   | 2   | 2   | 2   |
| Position in number | 7   | 6   | 5   | 4   | 3   | 2   | 1   | 0   |
| Calculate          | 2^7 | 2^6 | 2^5 | 2^4 | 2^3 | 2^2 | 2^1 | 2^0 |
| Position value     | 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| 1=                 | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 1   |
| 2=                 | 0   | 0   | 0   | 0   | 0   | 0   | 1   | 0   |
| 3=                 | 0   | 0   | 0   | 0   | 0   | 0   | 1   | 1   |
| 8=                 | 0   | 0   | 0   | 0   | 1   | 0   | 0   | 0   |
| 17=                | 0   | 0   | 0   | 1   | 0   | 0   | 1   | 0   |
| 172=               | 1   | 0   | 1   | 0   | 0   | 0   | 1   | 1   |
| 255=               | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |

### Decimal Numeral System

| Radix              | 10   | 10   | 10   | 10   |
| Position in number | 4    | 2    | 1    | 0    |
| Calculate          | 10^3 | 10^2 | 10^1 | 10^0 |
| Position value     | 1000 | 100  | 10   | 1    |
| 1=                 | 0    | 0    | 0    | 1    |
| 2=                 | 0    | 0    | 0    | 2    |
| 34=                | 0    | 0    | 30   | 4    |
| 3458=              | 3    | 4    | 5    | 8    |

### Hexadecimal Numeral System
**16^n** 

| Hexidecimal | 0    | 1    | 2    | 3    | 4    | 5    | 6    | 7    | 8    | 9    | A    | B    | C    | D    | E    | F    |
| Decimal     | 0    | 1    | 2    | 3    | 4    | 5    | 6    | 7    | 8    | 9    | 10   | 11   | 12   | 13   | 14   | 15   |
| Binary      | 0000 | 0001 | 0010 | 0011 | 0100 | 0101 | 0110 | 0111 | 1000 | 1001 | 1010 | 1011 | 1100 | 1101 | 1110 | 1111 |

e.g converting from hexidecimal to decimal and binary
hex- A9, dec- (10 x 16^1) + (9 x 16^0) = 169, binary- 1010, 1001
hex- CAB, dec- (12 x 16^2) + (10 x 16^1) + (10 x 16^0) = 3243, binary - 1100, 1010, 1011 

## MAC address: Media Acess Link
MAC address controls device interaction
48 bit 12 hexidecimal (6 octets)

|OUI     |NIC     |
|Vendor  |Device  |
|02 42 90|c1 b4 8c|

OUI:organisationally unique identifier
NIC:network interfacing controller

- To view the MAC address of your PC : ipconfig /all (Windows PowerShell), ifconfig -a (MAC terminal, Linux shell)
The MAC address is not routable, you can't find where it exists outside the local address.

## Network Layer (3) Addressing
**IP address** : A numerical lable assigned to each device connected to a network that uses the Internet Protocol for communication.
**IP** : the internet protocol is a set of rules governing the format of data sent via the internet.

IPV4 - series of 1s and 0s (binary numeral system)
32 bit (4 octet)

**IP classes**
|       |Octet 1|Octet 2|Octet 3|Octet 4|
|Class A|1-127  |0-255  |0-255  |0=255  |
|Class B|128-191|0-255  |0-255  |0=255  |
|Class C|192-223|0-255  |0-255  |0=255  |
|Class D|224-239|0-255  |0-255  |0=255  |
|Class E|240-255|0-255  |0-255  |0=255  |

Class A first octet starts with 0
Class B first octet starts with 10
Class C first octet starts with 110

Class A - 2^24 available host IP addresses
Class B - 2^16 available host IP addresses
Class B - 2^8 avaiable host IP addresses

**Subnet Mask**
- 32 bit address
- Used to mask a portion of the IP address to distinguish the network ID from the host ID
	- Calculate the Network ID: convert the IP to binary, calculate the logical AND for the IP address and the Subnet Mask
- Every host on a TCP/IP network requires a subnet mask
- In the subnet mask:
	-Bits that correspond to the network ID are set to 1
	-Bits that correspond to the network ID are set to 0
	- 1s on left, 0s on right

e.g
255.0.0.0 = 1111 1111.0000 0000.0000 0000.0000 0000 = /8
255.255.0.0 = 1111 1111.1111 1111.0000 0000.0000 0000 = /16
255.255.255.0 = 1111 1111.1111 1111.1111 1111.0000 0000 = /24
255.255.255.128 = 1111 1111.1111 1111.1111 1111.1000 0000 = /25
255.255.255.192 = 1111 1111.1111 1111.1111 1111.1100 0000 = /26
255.255.255.224 = 1111 1111.1111 1111.1111 1111.1110 0000 = /27
255.255.255.252 = 1111 1111.1111 1111.1111 1111.1111 1100 = /32

**Logical AND**
0 AND 0 = 0
0 AND 1 = 0
1 AND 0 = 0
1 AND 1 = 1
e.g calculate Network ID
Host ID: 192.128.2.1
logical AND
Subnet Mask: 255.255.255.0
Network ID: 192.128.2.1

**Broadcast ID (bcast IP)**
- The last IP in the network
- All host in a network should have the same Broadcast IP
- Use the broadcast IP to send specific data to all the machines on the same network

**Ping**
- Ping is Internet Control Message Protocol (ICMP) packet.
- Ping allows a user to ping another device IP address, this helps determine whether a device is reachable via the network.

command prompt:
ping 192.128.2.1

Returns:
Reply from... : host has received the ping message back from the destination device within the designated time period
Request timed out: host did not receive the ping message back from the destination device within designated time period
Destination host unreachable: route to destination computer system cannot be found