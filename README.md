# Enterprise Network Security & Firewall Management (Cisco ASA)

This project focuses on designing and managing security policies for an enterprise network using a **Cisco ASA (Adaptive Security Appliance) Firewall**. It demonstrates how to protect internal organizational data and services from external threats using advanced security configurations.

## 📌 Project Overview
The core objective of this project is to implement robust security measures, including **Access Control Lists (ACLs)**, **Network Address Translation (NAT)**, and **Stateful Packet Inspection (SPI)**, to regulate inbound and outbound traffic within a corporate environment.

### Key Features:
* **Firewall Deployment:** Implementation of Cisco ASA as the primary security barrier.
* **Traffic Control:** Fine-grained control over network communication using Standard and Extended ACLs.
* **Security via NAT:** Using Static NAT to expose internal servers safely without revealing private IP structures.
* **Stateful Inspection:** Allowing legitimate return traffic (like ICMP) while maintaining a high security posture.
* **Simulator:** Designed and tested on **Cisco Packet Tracer**.

---

## 🛠️ Technical Implementation & Security Policies

### 1. Access Control Lists (ACLs)
To balance security and business needs, specific traffic rules were applied:
* **Restricted Access:** PC0 was restricted from internet access to prevent unauthorized external communication.
* **Allowed Access:** PC1 and PC2 were granted internet/external connectivity for business operations.
* **Inbound Filtering:** ACLs were configured to ensure only authorized outside users could reach the internal web server.

### 2. NAT (Network Address Translation)
* **Static NAT Configuration:** The internal web server (Private IP: `192.168.1.2`) was mapped to a Public IP (`6.6.6.3`).
* **Security Benefit:** This hides the internal network topology from potential attackers while allowing essential services to remain reachable from the "Outside" network.

### 3. Stateful Packet Inspection (SPI)
* Configured the firewall to monitor the state of active connections.
* Specifically implemented to allow **ICMP (Ping)** traffic to return safely through the firewall once a connection is initiated from the "Inside".

---

## 🚀 Configuration Steps
1. **Network Topology:** Structured the network into three zones: *Inside* (Trusted), *Outside* (Untrusted), and *DMZ* (for Servers).
2. **ASA Initialization:** Configured interface security levels (Inside: 100, Outside: 0).
3. **ACL Deployment:** Wrote and applied ACL rules to the specific interfaces to manage traffic flow.
4. **NAT Setup:** Configured Static NAT rules for the web server to enable secure external access.
5. **Testing & Debugging:** Performed rigorous ping tests and HTTP requests to verify that security policies were enforced correctly.

---

## ✅ Results & Learning Outcomes
* **Successful Security Enforcement:** Verified that unauthorized users (PC0) were blocked while authorized users could browse successfully.
* **Server Protection:** The internal web server was successfully accessed via its public NAT IP, keeping its private identity hidden.
* **Stateful Flow:** Verified that the ASA correctly inspected and allowed legitimate return traffic.
* **Problem Solving:** Gained hands-on experience in troubleshooting NAT issues and ACL placement logic.

## 📂 Deliverables
* `.pkt` file: The complete Cisco ASA simulation and network design.
* `Enterprise Network Security & Firewall Management (Cisco ASA) REPORT.docx`: Comprehensive technical documentation including security policy details.

---
**Project by:** Shumaila Arif (Roll No: 68279)  
**Program:** BS Cyber Security  
**Course:** Information Security
