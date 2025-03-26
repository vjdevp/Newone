Pre-Update Planning
Identify why the patch is needed:
Security vulnerability fix
Performance improvements
Compatibility updates
Bug fixes
==========================================
rpm -q kernel 
sudo grubby --info=ALL
============================================

Backup the System

Take a full backup of:
System configuration files (/etc)
User data
Bootloader configuration (e.g., /boot/grub/grub.cfg)

==========================================
 Check System Logs
dmesg | grep -i error
journalctl -k
=============================================
====Set the previous kernel as default:===
sudo grubby --set-default /boot/vmlinuz-4.18.0-372.16.1.el8.x86_64
sudo grubby --default-kernel

===Remove the new kernel:===
sudo yum remove kernel-<version>
exp:- sudo yum remove kernel-4.18.0-425.3.1.el8.x86_64
sudo reboot
