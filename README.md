# -IT-Infrastructure-Portfolio
Hands-on enterprise labs demonstrating Active Directory deployment, GPO security management, and Cisco network engineering.
IT Infrastructure & Systems Portfolio
Candidate: Ramakant Joshi
Location: Copenhagen, Denmark
Education: Technical Education Copenhagen (TEC)
Contact: rajo@elev.tec.dk | 41605001 | https://www.linkedin.com/in/ramakant-joshi-529882127/
________________________________________
Portfolio Overview
This portfolio contains documented engineering labs demonstrating my hands-on capabilities in Systems Administration (Windows Server 2022) environments were designed, configured, and verified by me to simulate real-world enterprise architectures.
________________________________________
Project 1: Enterprise Active Directory & Group Policy Deployment
Project Overview
•	Objective: Design, deploy, and secure a centralized Windows Domain environment using VirtualBox to simulate a corporate infrastructure.
•	Core Technologies: Windows Server 2022 Standard, Active Directory Domain Services (AD DS), DNS, DHCP, and Group Policy Management.
•	Environment Parameters: Domain: firma.local | DC Hostname: SRV-01 | Network: 192.168.1.0/24
Implementation Details
1.	Network Baseline: Configured Domain Controller with a static IP (192.168.1.10). Configured workstation PC1 to use the server as its preferred DNS to successfully bind the client to the firma.local tree.
 
2.	Directory Identity Structure: Deployed Active Directory Domain Services. Built a dedicated Organizational Unit (OU) named Elever to segregate restricted user profiles from core staff.
 
3.	Security Hardening (GPO): Created and enforced a Group Policy Object (GPO) titled Disable control panel. Tied this rule to the Elever OU to restrict access to the control panel subsystem.

 

Verification & Diagnostics
•	Network Connectivity: Executed bidirectional ping sweeps between host and guest environments to verify Layer 3 connectivity.
•	Service Availability Check: Validated that crucial authentication and name resolution ports were online using command line telnet mapping:
cmd
telnet firma.local 53
•	GPO Enforcement Proof: Logging into the client workstation under a user account in the Elever OU and trying to open the Control Panel displays the following native security barrier:

