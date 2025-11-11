**# 🧭 Ext2 File System Explorer

A **C++ command-line tool** for exploring and manipulating **Ext2 file systems** inside **VirtualBox VDI disk images**.  
This project provides direct, low-level access to virtual disk structures, allowing users to navigate, inspect, and transfer files between a host machine and a virtual disk image.

## 🚀 Features
- Read and parse VirtualBox VDI disk images  
- Navigate Ext2 file systems interactively  
- Copy files between host and VDI images  
- Analyze file system structures (superblocks, inodes, directories)  
- Support for 1024B and 4096B block sizes  
- Educational tool for learning OS and file system internals  

## 🏗️ Build Instructions
Make sure you have **GCC/G++** installed and a **Linux environment**.

```bash
g++ -std=c++11 -o ext2explorer *.cpp
▶️ Usage

Run the program by providing the path to your VDI disk image:

./ext2explorer path/to/disk.vdi


You’ll be greeted with an interactive shell to explore the Ext2 file system.

💬 Commands
Command	Description
ls / ls -l	List directory contents
cd [dir]	Change directory (cd alone goes up one level)
read <vdi_path> <host_path>	Export a file from VDI to host
write <host_path> <vdi_path>	Import a file from host to VDI
clear	Clear the terminal screen
quit	Exit the explorer
🧪 Examples
ls -l
cd /home/user/documents
read /config.txt ./backup_config.txt
write ./script.sh /scripts/new_script.sh

🗂️ Project Structure
File	Description
main.cpp	Interactive shell and main logic
vdifunctions.*	VDI disk image handling
indexNode.*	Inode operations and file data access
blockFunctions.*	Superblock and block management
entry.h	Directory entry structures
⚙️ Requirements

Linux environment

GCC/G++ compiler

VirtualBox VDI file (formatted with Ext2)

⚠️ Notes & Warnings

🧠 Educational Use Only: Designed for OS and file system learning.

💾 Backup First: Always back up VDI files before write operations.

⚠️ Use With Caution: Direct modification of disk structures can lead to data loss.

📚 Learning Outcomes

This project demonstrates:

How Ext2 organizes and stores files

Inode and block-level management

Parsing binary disk structures in C++

Core operating system and file system principles

👨‍💻 Author

Raj Budhathoki
Computer Science Student, YSU’25
AI/ML Enthusiast | Full Stack Developer | OS & Systems Learner

🧩 License

This project is open for educational and non-commercial use.
Use responsibly and credit appropriately.**
