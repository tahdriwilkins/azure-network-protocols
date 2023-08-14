<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this project, I observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create our Resources
- Observe ICMP Traffic
- Observe SSH Traffic
- Observe DNS Traffic
- Observe 

<h2>Actions and Observations</h2>

<p>
<img width="1128" alt="image" src="https://github.com/tahdriwilkins/azure-network-protocols/assets/141438778/c4186f3e-1220-4637-aa35-b22242ad423f">
</p>

- Created 2 Virtual Machines in Mircosoft Azure. VM1 is Windows and VM2 is Linux Ubuntu
<br />

<p>
<img width="1128" alt="image" src="https://github.com/tahdriwilkins/azure-network-protocols/assets/141438778/798432de-9d75-4cd8-b746-907744967094">
</p>

- Then I download wireshark in the Windows Virtual Machine
<br />

<p>
<img width="1128" alt="image" src="https://github.com/tahdriwilkins/azure-network-protocols/assets/141438778/942a9e44-b78f-455e-ad9f-f881f25bb79e">
</p>

- Upon opening up wireshark, I can observe all of the traffic coming in. The goal is to only observe ICMP traffic
<br />


<p>
<img width="1128" alt="image" src="https://github.com/tahdriwilkins/azure-network-protocols/assets/141438778/214a9476-1569-4f66-b09d-e01a924a58ca">
<img width="1128" alt="image" src="https://github.com/tahdriwilkins/azure-network-protocols/assets/141438778/08373a59-fec2-45b2-8bc7-c51b9f93fdf8">
</p>

- Then we filter for ICMP in wireshark. After I then go to VM2 to get the Private IP address which is 10.0.0.5. Go back into VM1 and open powershell so I can ping VM2 and observe what happens
<br />


<p>
<img width="1128" alt="image" src="https://github.com/tahdriwilkins/azure-network-protocols/assets/141438778/688118fa-0edc-4633-8840-8ee3f3a03818">
<img width="1128" alt="image" src="https://github.com/tahdriwilkins/azure-network-protocols/assets/141438778/03ff55e0-1e74-408a-a60f-574f022baba0">
</p>

- I can also deny the ICMP traffic by going into VM2 Network Secruity Group and adding an inbound rule to deny ICMP traffic. Once I log back into VM1, the ping times out
<br />


<p>
<img width="1128" alt="image" src="https://github.com/tahdriwilkins/azure-network-protocols/assets/141438778/4e3217ce-96f0-49b5-b9b0-b7698d8ebd5b">
<img width="1128" alt="image" src="https://github.com/tahdriwilkins/azure-network-protocols/assets/141438778/e34b214e-528b-4572-b636-7997bc9d23d9">
</p>

- Back in Wireshark, filter for SSH traffic only. From the Windows 10 VM, “SSH into” Ubuntu Virtual Machine (via its private IP address)
- I then type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark
<br />


<p>
<img width="1128" alt="image" src="https://github.com/tahdriwilkins/azure-network-protocols/assets/141438778/43ef9740-c6df-4f1d-bf4a-d2248b4c322e">
</p>

- Back in Wireshark, filter for DHCP traffic only. Then from the Windows 10 VM, attempt to issue your VM a new IP address from the command line (ipconfig /renew)
- Observe the DHCP traffic appearing in WireShark
<br />


<p>
<img width="1128" alt="image" src="https://github.com/tahdriwilkins/azure-network-protocols/assets/141438778/ccd23a4c-d949-4993-abb8-e55138e423c0">
</p>

- Back in Wireshark, filter for DNS traffic only. Then from the Windows 10 VM within a command line, use nslookup to see what google.com IP addresses are
- Observe the DNS traffic being show in WireShark
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


