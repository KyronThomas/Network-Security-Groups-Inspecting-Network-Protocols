# Network Security Groups & Inspecting Network Protocols 🔒🌐

This project demonstrates how to create, configure, and test **Network Security Groups (NSGs)** in Azure, as well as how to inspect and understand **network protocols** using built-in tools.

---

## 🧰 Technologies Used

- Microsoft Azure (NSG & VMs)
- Windows Server 2022 / Windows 10
- Network Security Groups (NSGs)
- Remote Desktop Protocol (RDP)
- Wireshark / Packet Monitoring Tools
- PowerShell & Command Prompt

---

## 📡 What Are NSGs?

Network Security Groups are like firewalls that control **inbound and outbound traffic** to Azure resources. Each rule defines the allowed or denied traffic by:
- **Port**
- **Protocol (TCP/UDP)**
- **Source/Destination IP**
- **Priority**

---

## 🛠️ Setup Steps

### 1. Create Two Virtual Machines in Azure
- One acts as a **web server**
- One acts as a **client/test machine**
- Place them in the same **Virtual Network**

### 2. Create a Network Security Group
- Navigate to **Azure Portal → Networking → NSG**
- Add **inbound rules** for RDP (port 3389), HTTP (80), etc.
- Add **outbound rules** to restrict or allow traffic as needed

### 3. Associate NSG with VM's Network Interface or Subnet
- Apply the NSG to the **VM's NIC** or to the **subnet**
- Verify traffic is affected as expected

---

## 🔍 Protocol Inspection (Optional Lab)

Use tools like **Wireshark** or **Windows built-in monitors** to capture and analyze traffic:

### Examples:
- Run `ping` from the client to the server
- Use `telnet <ip> 80` to test open ports
- Open Wireshark and filter by `tcp.port == 80` to watch HTTP traffic

---

## ✅ Validation Checklist

- [x] NSG rules successfully allow/block expected traffic  
- [x] Able to RDP into allowed VM  
- [x] Blocked traffic shows proper error or timeout  
- [x] Packet analysis verifies correct protocol behavior  

---

## 📘 Learning Outcomes

- Understand how NSGs secure Azure VMs  
- Learn to build traffic rules based on specific needs  
- Gain basic protocol inspection skills  
- Know how to troubleshoot connectivity issues  

---

>  NSGs are a critical component of cloud security. Combining NSG knowledge with packet analysis gives you a powerful skillset for defending and understanding modern networks!
