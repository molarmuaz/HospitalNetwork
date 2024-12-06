**Hospital Network Design and Implementation**  
A Computer Networks Project

**Objective**  
The goal of this project is to create and put into place a complete hospital network architecture that guarantees safe internet access, effective data routing, and smooth departmental communication. Network Address Translation (NAT) is used to secure external traffic, and DHCP is used to manage dynamic IP addressing on the network. Implementing a scalable design that accommodates upcoming improvements like internal security measures is another goal of the project.

**Technologies Used**  
The hospital network is configured using 

* Cisco Packet Tracer for simulation and testing.   
* Enhanced Interior Gateway Routing Protocol (EIGRP) is implemented for efficient and dynamic routing between department routers.   
* A centralized DHCP server is used to assign IP addresses dynamically to devices within their respective departmental subnets.   
* Network configurations are managed using Cisco IOS commands via router and switch Command Line Interface (CLI).   
* Subnetting and NAT configurations are integral to the design to keep internal IP Addresses private.

**Implementation Details:**  
The administrative, emergency (ER), outpatient (OP), and pharmacy departments make up the various divisions of the network design.  

A central router serves as the backbone, and each department has its own subnet, router, and switch. Interdepartmental communication is facilitated by the central router, which is set up with IP 192.168.10.0/24 and uses NAT to control internet access. 

When connecting to external networks, the NAT router translates addresses to secure internal devices. Admin 192.168.30.0/24, ER 192.168.50.0/24, OP 192.168.70.0/24, and Pharmacy 192.168.90.0/24 are the subnet allocations. Within the network, these subnets guarantee isolation and effective traffic control.

EIGRP is configured across all routers to dynamically update routing tables, allowing optimal paths for data transmission. The DHCP server dynamically assigns IP addresses within each subnet, ensuring hassle-free device configuration. NAT is configured on the central router to translate internal private IP addresses to a global IP when accessing the internet. This adds an additional layer of security, as external networks cannot directly access internal devices.

**Network Diagram and NAT Table**  
The network topology reflects the IP addressing scheme, with NAT configured on the central router. The NAT table displays mappings between internal private IP addresses and global addresses used for internet access. This ensures secure and efficient communication across the hospital's departments and external resources.

![Screenshot_1](https://github.com/user-attachments/assets/b618308f-cddb-49f5-ad51-7e4a28e9f660)

Central:  
![image](https://github.com/user-attachments/assets/e4646487-b9e9-4ce0-b586-38d8b042bc2f)
  
Admin:   
![image](https://github.com/user-attachments/assets/0c8ce5ec-20e7-4b95-873c-aab5311f8551)

Emergency:

![image](https://github.com/user-attachments/assets/268e9875-fbc1-43d6-a06d-a4a7eb78d1dd)


Outpatient:

![image](https://github.com/user-attachments/assets/a6c4f690-e563-4d58-bba0-1e935c15ac79)


Pharmacy:

![image](https://github.com/user-attachments/assets/a5be5862-d482-4eb7-bc08-6bbf0c56bb31)


NAT Table:  
![image](https://github.com/user-attachments/assets/27914b13-2178-454a-a473-796fdfd97ce4)


**Results and Testing**  
The network was rigorously tested to validate its functionality. DHCP servers successfully assigned IP addresses to client devices in each department, and inter-departmental communication was verified using EIGRP. 

![image](https://github.com/user-attachments/assets/4494dcfe-4605-4532-a0df-6ef969e5a04c)

Devices in the Admin department were able to access resources in other departments and the internet, demonstrating effective NAT translation. The NAT table logs confirmed proper address mappings for outgoing traffic. Connectivity tests using ICMP (ping) and traceroute further validated routing and address translation.

![image](https://github.com/user-attachments/assets/b925f242-cc95-46d5-a4e0-3e7cc8b35716)


**Challenges and Learnings**  
Setting up DHCP and designating DHCP pools to manage dynamic IP address distribution across all PCs across all departments was one of the difficulties faced. Determining appropriate inside and outside interfaces on the central router was another difficulty caused by the NAT configuration. Despite these challenges, the experiment offered insightful information about the complexities of IP address management, dynamic routing, and network segmentation.

**Conclusion**  
The hospital network was effectively planned and put into place to facilitate safe internet access and effective departmental collaboration. Secure external communication and ideal routing were guaranteed by the usage of EIGRP and NAT. Future suggestions include strengthening network security to stop unwanted access and putting Access Control Lists (ACLs) in place for internal traffic limits. The groundwork for future advancements in network administration and security is laid by this scalable design.  
