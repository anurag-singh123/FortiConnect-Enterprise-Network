# **FortiConnect Enterprise Network**

A comprehensive enterprise network project, designed for a company with its own data center, headquarters, and branch offices. This network setup includes high availability, robust security, and efficient traffic management to support scalable and secure operations. This README provides an overview of the architecture, features, and configurations used in the project.

## **Table of Contents**
1. [Project Overview](#project-overview)
2. [Network Design and Architecture](#network-design-and-architecture)
3. [Data Center Setup](#data-center-setup)
4. [Headquarters and Branch Office Structure](#headquarters-and-branch-office-structure)
5. [Security Features](#security-features)
6. [Routing and Communication](#routing-and-communication)
7. [IoT Integration](#iot-integration)
8. [Device and Network Security](#device-and-network-security)
9. [Management and Monitoring](#management-and-monitoring)
10. [Technologies and Protocols Used](#technologies-and-protocols-used)
11. [Project Structure](#project-structure)
12. [Getting Started](#getting-started)
13. [Future Enhancements](#future-enhancements)
14. [Contact Information](#contact-information)

---

## **1. Project Overview**
This project represents a highly secure and efficient enterprise network with its own data center, headquarters, and branch offices. It includes:
- **Data Center** with core routers, ASA firewall, and various servers.
- **Spine-Leaf Topology** to optimize traffic flow.
- **Multiple Security Layers**: NAT, access lists, firewall policies, port security, and wireless security.
- **IoT Integration** with a home network setup for remote management.
- **Routing Protocol**: OSPF configured across the network for dynamic routing.

## **2. Network Design and Architecture**
- **Data Center**: Equipped with primary and standby core routers for redundancy.
- **Firewall**: An ASA firewall is configured to create public, private, and DMZ zones.
- **Spine-Leaf Topology**: Implemented across data center and office structures to reduce traffic congestion.
- **Port Channels**: Configured between firewall and switches for enhanced throughput and reliability.

## **3. Data Center Setup**
The data center architecture includes:
- **Primary and Standby Routers** for high availability.
- **ASA Firewall**: Divides network into three zones:
  - **Public Zone**
  - **Private Zone**
  - **DMZ Zone**: Hosts external servers like DNS, HTTP, SMTP, IoT, NTP, AAA, and Syslog.
- **Internal Servers** in the private zone, such as FTP, internal SMTP, and Radius server.
- **Spine-Leaf Switch Structure** with port channels to improve traffic management.

## **4. Headquarters and Branch Office Structure**
- **Spine-Leaf Topology** replicated in HQ and branches.
- **Devices Used**: Routers, Layer 3 and Layer 2 switches, Access Points, PCs, smartphones, printers, IoT devices, and more.
- **VLANs** and **VTP** for network segmentation.
- **STP** configured on switches to prevent loops and ensure network stability.

## **5. Security Features**
- **Firewall Policies**: Configured on the ASA firewall to control traffic in each zone.
- **Access Control Lists (ACLs)**: Used for granular control over network access.
- **Network Address Translation (NAT)**: Allows secure communication between internal and external networks.
- **Infrastructure Security**: Password-protected devices and SSH for secure remote management.
- **Wireless Security**: Configured WPA2 Personal for secure Wi-Fi connections.

## **6. Routing and Communication**
- **Routing Protocol**: OSPF (Open Shortest Path First) implemented across the network for dynamic routing and efficient communication between network zones.
- **Inter-VLAN Routing**: Configured for secure and segregated traffic flow within the network.

## **7. IoT Integration**
- **IoT Server**: Manages all IoT devices in the network.
- **Home Network (Jack's Home)**: IoT devices in Jack’s home are connected to the IoT server, allowing him to control them remotely from the enterprise network.

## **8. Device and Network Security**
- **Port Security**: Enabled on all switches to prevent unauthorized device connections.
- **Password Protection**: All devices are secured with strong passwords.
- **SSH Access**: Configured on all network devices for encrypted remote management.
- **Firewall Syslog Monitoring**: Logs monitored through a Syslog server connected to the firewall.

## **9. Management and Monitoring**
- **Syslog Server**: Connected to the firewall for tracking network events and logs.
- **Access Control**: Enforced through ACLs and firewall policies to secure sensitive zones.

## **10. Technologies and Protocols Used**
- **Network Devices**: Routers, L3 switches, L2 switches, ASA firewall, various servers (FTP, DNS, HTTP, SMTP, etc.), IoT devices, access points, PCs, smartphones, and more.
- **Protocols**:
  - **OSPF**: Used for dynamic routing.
  - **STP**: Spanning Tree Protocol for loop prevention.
  - **VTP**: VLAN Trunking Protocol for VLAN management.
  - **NAT**: Network Address Translation for secure internal-to-external communication.
  - **WPA2**: Wireless security protocol.
  - **SSH**: Secure Shell for device access.
- **Security**:
  - **Firewall Policies and ACLs**
  - **Port Security** on switches
  - **Wireless Security**: WPA2 Personal for secure Wi-Fi connections.

## **11. Project Structure**
```markdown
Project-Directory/
├── Data-Center/
│   ├── Core-Routers/
│   ├── ASA-Firewall/
│   ├── Public-Zone/
│   ├── Private-Zone/
│   ├── DMZ-Zone/
│   ├── Spine-Leaf-Switches/
├── Headquarters/
│   ├── Routers/
│   ├── Switches/
│   ├── VLANs/
├── Branch-Offices/
│   ├── Routers/
│   ├── Switches/
│   ├── VLANs/
└── Documentation/
    ├── Network-Diagram.png
    ├── Configurations/
    ├── README.md
```

## **12. Getting Started**
To set up this project:
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/your-username/FortiConnect-Enterprise-Network.git
   ```
2. Open the network simulation file (if using Cisco Packet Tracer, .pkt format) to view or simulate the network.
3. Refer to the **Configurations** directory for initial configuration files and setup instructions.

## **13. Future Enhancements**
- **SD-WAN Integration** for enhanced connectivity between branches.
- **Advanced Security**: Implement more advanced firewall rules, intrusion detection/prevention systems.
- **Network Automation**: Using Ansible or Python scripts to automate configurations and monitoring.

## **14. Contact Information**
For questions, feedback, or suggestions:
- **GitHub**: (https://github.com/anurag-singh123)
- **Email**: anurag.singh01018@gmail.com

## Screenshots
![Screenshot 2024-11-02 000217](https://github.com/user-attachments/assets/8709363a-6b1a-4e0d-82ee-2c51259f8075)
![Screenshot 2024-11-02 185531](https://github.com/user-attachments/assets/312d2fce-ad17-4d21-beab-aab1ba320b45)
![Screenshot 2024-11-02 185622](https://github.com/user-attachments/assets/a198fd98-135e-44cc-a2e5-897aff52efa1)
![Screenshot 2024-11-02 185633](https://github.com/user-attachments/assets/ed041df3-aa21-435c-8b45-ba88bbc1ab57)
![Screenshot 2024-11-02 185556](https://github.com/user-attachments/assets/c999573d-cd6a-47fb-a908-99c24ed5e2c1)


