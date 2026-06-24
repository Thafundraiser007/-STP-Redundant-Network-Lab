📡 STP Redundant Network Lab (Cisco Packet Tracer)

Cisco Packet Tracer STP redundancy lab with a DHCP server providing automatic IP addressing in a switched LAN environment.

🧾 Overview

This project demonstrates Spanning Tree Protocol (STP) in a small enterprise LAN topology using Cisco Packet Tracer. The lab shows how STP prevents switching loops and ensures network redundancy and failover when multiple physical paths exist between switches.

The network consists of one core switch and multiple access switches connected to end devices, with a DHCP server providing automatic IP address assignment.

🏗️ Network Topology
1 Core Switch (STP Root Bridge)
3 Access Switches (End-user connectivity)
Multiple redundant uplinks between switches
1 DHCP Server
End devices (PCs) connected via access switches
🔌 Port Design
Fa0/1 – Fa0/4: Uplink ports between all switches (redundancy links)
Fa0/5 – Fa0/24: End-user access ports
🔁 STP Functionality

This lab focuses on demonstrating:

Prevention of Layer 2 switching loops
Automatic blocking of redundant links
Dynamic failover when an active link goes down
STP root bridge election (core switch as root)

When redundant paths exist, STP places one link into a blocking state. If the active link fails, STP automatically reconverges and activates the backup path.

⚙️ Configuration Summary
🧠 Core Switch
Configured as STP Root Bridge
Uplink ports (Fa0/1–Fa0/4) configured as trunk links
Handles inter-switch communication
🧠 Access Switches
Connected to core switch via uplinks
Fa0/1–Fa0/4 used as uplinks between switches
Fa0/5–Fa0/24 configured as access ports for end devices
PortFast enabled on edge ports only
🧠 DHCP Server
Provides automatic IP addressing to clients
Network: 192.168.1.0/24
Default gateway: 192.168.1.1
IP range: 192.168.1.100 – 192.168.1.200
🧪 Testing & Verification
✅ STP Status Verification

Command used:

show spanning-tree

Result:

Core switch confirmed as ROOT bridge
One redundant link placed in BLOCKING state
Active forwarding path successfully established
🔁 Redundancy / Failover Test
Active uplink manually shut down
STP recalculated topology
Previously blocked link transitioned to FORWARDING state

Result:
✔ Network traffic successfully rerouted through backup link
✔ No switching loops detected
✔ Automatic STP convergence confirmed
📡 DHCP Verification
Clients configured to obtain IP via DHCP
IP addresses successfully assigned by DHCP server
Gateway and subnet mask correctly applied
📁 Files Included
Screenshots in folder
Packet Tracer topology file (.pkt)
<img width="1205" height="892" alt="11  Redundancy Successful" src="https://github.com/user-attachments/assets/9514aff3-4f71-4ff9-99d9-723730ecddcf" />

🚀 Key Skills Demonstrated
Cisco Switching Fundamentals
Spanning Tree Protocol (STP)
Network redundancy design
Layer 2 loop prevention
DHCP configuration and troubleshooting
Packet Tracer simulation and validation
📌 Conclusion

This lab demonstrates how STP ensures a loop-free and highly available switched network. Redundant links remain in standby mode and are automatically activated when the primary path fails, ensuring continuous network connectivity.

AUTHOR:
Jamill Naipao
