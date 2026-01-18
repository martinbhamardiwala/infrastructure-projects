# 🔒 Project-1 — Firewall Implementation & Network Security

> **Note:** For security purposes, I cannot describe the project in detailed depth and types of devices we used.

---

## 📌 Project Description  
A firewall implementation project designed to enforce strict access control and protect sensitive network devices. The goal was to meet client security requirements by blocking unauthorized internet access while allowing essential services and controlled internal communication.

---

## 🧩 Client Requirements

The client requested the following firewall and network security policies:

- **Block all websites related to data transfer and online backup**, except **Dropbox**  
- **Block all gaming, gambling, financial, and stock-related websites**  
- **Block all social media sites**, except **WhatsApp**  
- **Restrict NAS devices**
  - There were **2 NAS systems**
  - **Block WAN traffic to NAS**
  - **Allow NAS access only within LAN**   
- **Block internet traffic for camera IP group**
  - **Only allow access from NVR IPs**

---

## 🛠️ Our Solution (Implementation Steps)

Below is the structured approach we used to meet the client requirements:

### 1. Network Assessment & Planning
- Identified all network devices, IP addresses, and traffic flow  
- Created a topology diagram for firewall placement  
- Listed all required services and exceptions (e.g., Dropbox)

### 2. Firewall Setup
- Deployed a firewall in front of the network  
- Configured zones: **LAN**, **WAN**, **DMZ** (if applicable)

### 3. Web Content Filtering
- Created URL filtering rules to block:
  - Online backup / data transfer sites  
  - Gaming & gambling sites  
  - Financial & stock trading sites  
  - Social media platforms  
- Allowed **only Dropbox** as an exception

### 4. NAS Traffic Restriction
- Identified NAS IP addresses  
- Configured rules:
  - **Deny WAN access**
  - **Allow LAN access only**
  - Block all incoming internet traffic to NAS

### 5. Camera IP Restrictions
- Grouped camera LAN IP addresses  
- Created firewall rules to:
  - Block internet access for camera group  
  - Allow access only from authorized **NVR IPs**

### 6. Testing & Validation
- Conducted testing for each policy  
- Verified:
  - Blocked sites were inaccessible  
  - NAS was unreachable from WAN  
  - Cameras could only be accessed by NVR  
  - Remote management worked securely  

---

## 📊 Result

- All client requirements were successfully implemented  
- Strict access control was enforced across the network  
- NAS devices were secured from WAN threats  
- Camera network was protected and limited to NVR access  
- Overall network security posture improved significantly
