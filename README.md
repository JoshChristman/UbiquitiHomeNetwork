# 🏠 Ubiquiti Home Network Project

## 📌 Overview
This project documents the setup of a **secure and high-performance home network** using **Ubiquiti UniFi** hardware. The network is segmented using VLANs for optimized security and performance, with IDS/IPS enabled. The setup also integrates **a NAS for media storage**, **security cameras**, and **a guest network with a captive portal**.

## 📸 Installed Networking Hardware
The following image showcases the installed networking hardware, including **Starlink, UniFi Cloud Gateway Max, Switch Ultra 60W, Surge Protector, and U6 Plus AP**:

![Installed Networking Hardware](https://imgur.com/lbD3BSm.png)

## 🌐 Network Topology
The following diagram represents the **UniFi Network Topology** as displayed in the GUI, showing all **UniFi devices, NAS, and household clients**:

![Network Topology](https://imgur.com/MEX76hq.png)

## 🔥 Firewall Rules
This network enforces **strict firewall rules** to ensure security and VLAN segmentation.

### ❌ Block Rules
- **Block Inter-VLAN Traffic** (except for specific allow rules)
- **Block Nights_Watch (Cameras) from Internet & VLANs**
- **Block Guest VLAN from accessing internal networks**
- **Block IoT VLAN (WiFi_Walkers) from internal networks except NAS (10.25.1.10)**
- **Block Unauthorized Traffic**

### ✅ Allow Rules
- **Allow The_Mad_Ping (Admin) to All VLANs**
- **Allow Wildlings_Net to WiFi_Walkers** (but **not** The_Mad_Ping)
- **Allow Guest VLAN to Internet (Captive Portal Authentication Required)**
- **Allow IoT VLAN to access NAS (10.25.1.10) on media ports only**
- **Allow VPN to access specific VLANs (Admin, Home Lab)**

### 🖼️ Screenshot of Firewall Rules
![Firewall Rules](https://imgur.com/1OrmYJh.png)

## 🔄 VLAN Breakdown
| VLAN Name      | Purpose                        | Restrictions |
|---------------|--------------------------------|--------------|
| **Nights_Watch** | Security Cameras Only       | No Internet, No VLAN Access |
| **Pings_Landing** | Guest Network (Captive Portal) | No Inter-VLAN Access |
| **WiFi_Walkers** | IoT Devices (Smart TVs, etc.) | Only access NAS (10.25.1.10) |
| **Wildlings_Net** | Kids & Family Devices | No Admin Access, Limited IoT Access |
| **The_Mad_Ping** | Admin & Default Network | Full Access |

## 🛠️ Hardware Used
**Gateway:** UniFi Cloud Gateway Max  
![UniFi Gateway](https://imgur.com/dukUWK0.png)

**Switch:** UniFi Switch Ultra 60W  
![UniFi POE Switch](https://imgur.com/RLbTTHy.png)

**Access Point:** UniFi U6 Plus AP  
![UniFi AP](https://imgur.com/tapENkg.png)

**Security Cameras:** UniFi G5 Turret Ultra (x2)  
![UniFi Cameras](https://imgur.com/RpbC73h.png)

**NAS:** Custom NAS for Media & Backup  
![NAS](https://imgur.com/D0IyJud)

## 🔮 Future Improvements
- **Implement VLAN-Specific Bandwidth Controls** to prevent congestion
- **Enhance Logging & Monitoring** with better analytics tools
- **Fine-tune IDS/IPS policies** to reduce false positives
- **Automate Network Backups** to improve reliability

---

### 🚀 About This Project
This project is part of my **GitHub portfolio** showcasing **network administration skills**. It is structured for **resume and job applications** in system administration and cybersecurity. 

👉 **GitHub Profile:** [github.com/JoshChristman](https://github.com/JoshChristman)  
👉 **LinkedIn:** [linkedin.com/in/Josh-Christman](https://www.linkedin.com/in/Josh-Christman)
