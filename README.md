![image](https://github.com/user-attachments/assets/519d2d0c-4daa-495b-83de-2193453e8b70)


<h1>Understading DNS</h1>
In this lab, we will explore and experiment with the Domain Name System (DNS) to gain a beter understanding of how it works. DNS convers computer names to IP addresses which can be used by the computer to locate resouces. DNS is integrated wuth Active Directory and automatically gets installed on the Domain Controller(DC).

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- DNS

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- A Virtual Machine with Active Directory
- A Client VM joined to your Network 

<h2>DNS Steps</h2>

DNS (Domain Name System) is like the phonebook of the internet. It translates human-friendly website names (like google.com) into computer-friendly IP addresses (like 142.250.190.14).

![image](https://github.com/user-attachments/assets/bcdfe05a-a96e-4401-aabe-9e9855a48462)

The DC also doubles as a DNS server, which means its responsible for resolving all requests from the network. In order to do this, the server uses "Root Hint". A Root Hint Server is a special type of DNS server that helps other DNS servers find the root of the internet's domain name system (DNS). It acts as a starting point when a DNS server needs to resolve a domain name but doesn’t have the answer cached or stored locally.

![image](https://github.com/user-attachments/assets/47cabd30-7941-44a9-b4d5-e651280554b7)

Once you log into both the Virtual Machines (azure) for Client and Domain Controller, you then will get the public IP address for both and connect to them in Remote Desktop (using one remote desktop for each). Log into Client as admin "mydomain.com/admin/(yourname)" and open up Powershell to ping mainframe. When your computer tries to interact with a host name on the network, it will first go through a few steps. The first step is for it to check the Local DNS Cashe, if there is no success then it will continue its search by connecting to the Local Host File, before lastly checking the DNS Server.

![image](https://github.com/user-attachments/assets/8fe92000-fd14-4fe0-860a-8737f22f10b5)

Next we are going to create a DNS A-record on DC for “mainframe” and have it point to DC Private IP address. By doing so you go to DNS on the start menu -> DC-> mydomain.com and note the Private IP address for DC. In order to create a new A-record, inside of the DNS manager we are going to right click and select "New Host" and name it "mainframe" with the IP address the same as the DC private IP address.


![image](https://github.com/user-attachments/assets/c30d4965-b368-49b5-b39a-2c87534a4bc2)
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps" />
</p>
<p>
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<br />

<p>
