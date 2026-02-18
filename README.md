*This project has been created as part of the 42 curriculum by adchebbi.*

# Born2beRoot

## 📌 Description

Born2beRoot is an introduction to system administration through virtualization.  
The goal is to install and configure a secure Linux server inside a virtual machine while respecting strict security rules.

This project focuses on understanding how a Linux system works without a graphical interface, especially regarding user management, security, services, and monitoring.

---

## 🖥 Operating System Choice

I chose **Debian stable** because it is beginner-friendly, stable, and well documented.  
It is widely used for servers and easier to configure than Rocky Linux, especially regarding security tools.

---

## 🔎 Key Comparisons

- **Debian vs Rocky**: Debian is community-based and simpler; Rocky is enterprise-oriented and uses SELinux.
- **AppArmor vs SELinux**: AppArmor is easier to configure; SELinux offers more advanced control.
- **UFW vs firewalld**: UFW is simpler and suitable for Debian.
- **VirtualBox vs UTM**: VirtualBox is widely supported; UTM is mainly for Apple Silicon.

---

## 🗂 Partitioning & Security

LVM was used for flexible disk management and easier resizing.  
Disk encryption protects data in case of physical access to the disk.

Separate partitions improve security and prevent system failure if one partition becomes full.

Security measures implemented:

- SSH on port 4242
- Root login disabled
- UFW enabled at startup
- Strong password policy
- Sudo logging and restricted configuration
- AppArmor enabled

---

## 📊 Monitoring

A Bash script (`monitoring.sh`) displays system information every 10 minutes using cron and wall, including CPU usage, memory, disk usage, active connections, LVM status, and sudo command count.

---

## 📚 Resources & AI Usage

Official Debian documentation and Linux man pages were used.

AI was used to clarify concepts (LVM, security tools) and structure this README. All configurations were implemented manually.
