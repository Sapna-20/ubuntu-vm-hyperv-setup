# ubuntu-vm-hyperv-setup
vm- Hyper-V setup 

# 🐧 Ubuntu 24.04 LTS Server VM Setup using Hyper-V

This project documents the steps I followed to **create a virtual machine (VM) for Ubuntu 24.04 LTS Server** using **Microsoft Hyper-V** on a Windows system. It includes step-by-step setup, troubleshooting experience, screenshots, and usage of the VM.

---

## 🎯 Objective

To set up and configure a working Ubuntu 24.04 LTS Server VM using Hyper-V and explore how such a server can be used in production/testing environments.

---

## 🪜 Step-by-Step Process

### 1️⃣ Enable Hyper-V

- Verified Hyper-V support via `msinfo32`.
- Enabled Hyper-V from:
  ```
  Control Panel → Programs → Turn Windows features on or off → Check "Hyper-V"
  ```
- Restarted system.

### 2️⃣ Download Ubuntu Server ISO

- Downloaded ISO from: [Ubuntu 24.04 Server ISO](https://ubuntu.com/download/server)

### 3️⃣ Launch Hyper-V Manager

- Opened **Hyper-V Manager** via Windows Search.

### 4️⃣ Create New Virtual Machine

- **Name**: UbuntuServer2404  
- **Generation**: 2 (UEFI supported)
- **RAM**: 2048 MB  
- **Networking**: Default switch  
- **Disk**: 20 GB virtual hard disk  
- **Installation media**: Ubuntu 24.04 ISO

### 5️⃣ Start the Virtual Machine

- Right-click → Connect → Start

### 6️⃣ Install Ubuntu 24.04

- Selected Language, Keyboard layout
- Network auto-configured
- Disk: Used full disk
- Created user and hostname
- Chose to install OpenSSH Server
- Rebooted after installation

### 7️⃣ Post-Installation

```bash
sudo apt update && sudo apt upgrade
sudo apt install openssh-server
```

---

## ⚙️ Usage in Real-world Scenarios

This VM can be used for:
- 🧪 Testing Linux-based applications
- 🐍 Setting up Python or web servers
- 🧰 Hosting development environments
- 🔐 Learning system administration and security

---

## 💡 Challenges Faced

- **Networking Configuration**: Initially the VM didn’t get internet. Fixed it by using the "Default Switch".
- **Secure Boot Errors**: Resolved by disabling secure boot for the VM.

---

## 📚 Resources

- [Ubuntu Server Docs](https://ubuntu.com/server/docs)
- [Hyper-V Official Docs](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/)

---

## 🏁 Final Outcome

Successfully set up an Ubuntu 24.04 Server VM using Hyper-V with basic SSH access and update capabilities. Ready for further development or configuration!

---
