# 🧠 Part 2 — 300 Essential Ubuntu Commands (Beginner → Intermediate)

> ⚙️ These are the commands you’ll use daily — from navigating files to managing users, services, and networks. Every example is tested for Ubuntu 22.04 LTS and newer.
> 

---

## 🧩 1. System & Shell Basics

| Command | Description | Example |
| --- | --- | --- |
| `whoami` | Show current username. | → `whoami` |
| `hostname` | Display system hostname. | → `hostname` |
| `date` | Print system date and time. | → `date` |
| `cal` | Display calendar for current month. | → `cal` |
| `clear` | Clear the terminal screen. | → `clear` |
| `history` | Show previously executed commands. | → `history |
| `uptime` | Show how long system has been running. | → `uptime` |
| `uname -a` | Display kernel and system info. | → `uname -a` |
| `lsb_release -a` | Show Ubuntu release details. | → `lsb_release -a` |
| `echo` | Display a line of text or variable. | → `echo $HOME` |
| `man <cmd>` | Open manual for a command. | → `man ls` |
| `info <cmd>` | Detailed info (like `man`). | → `info grep` |
| `exit` | Exit terminal or shell session. | → `exit` |

---

## 📂 2. File & Directory Operations

| Command | Description | Example |
| --- | --- | --- |
| `pwd` | Show current directory path. | → `pwd` |
| `ls` | List directory contents. | → `ls -la` |
| `cd` | Change directory. | → `cd /etc` |
| `mkdir` | Create new directory. | → `mkdir projects` |
| `rmdir` | Remove empty directory. | → `rmdir testdir` |
| `cp` | Copy files or directories. | → `cp file1 file2` |
| `mv` | Move or rename files. | → `mv file1 /tmp/` |
| `rm` | Remove files. | → `rm file.txt` |
| `rm -r` | Recursively delete directories. | → `rm -rf dir/` |
| `touch` | Create empty file / update timestamp. | → `touch notes.txt` |
| `cat` | Display file contents. | → `cat /etc/hostname` |
| `head` | Show first lines of a file. | → `head -n 10 logfile` |
| `tail` | Show last lines of a file. | → `tail -f /var/log/syslog` |
| `more`, `less` | Scroll through file content. | → `less /etc/passwd` |
| `file` | Determine file type. | → `file image.jpg` |
| `find` | Search files/directories. | → `find /home -name "*.pdf"` |
| `locate` | Locate files by name (needs updatedb). | → `locate sshd_config` |
| `updatedb` | Update locate database. | → `sudo updatedb` |

---

## 🔍 3. Viewing & Editing Text Files

| Command | Description | Example |
| --- | --- | --- |
| `cat`, `more`, `less` | View files (paged). | → `less /etc/fstab` |
| `nano` | Easy terminal text editor. | → `nano script.sh` |
| `vim` | Advanced text editor. | → `vim config.txt` |
| `gedit` | GUI editor. | → `gedit notes.md` |
| `diff` | Compare two files. | → `diff file1 file2` |
| `sort` | Sort text lines alphabetically. | → `sort names.txt` |
| `uniq` | Remove duplicate lines. | → `uniq names.txt` |
| `wc` | Count lines/words/chars. | → `wc -l file.txt` |
| `grep` | Search pattern in files. | → `grep "root" /etc/passwd` |
| `sed` | Stream edit text (replace, delete). | → `sed 's/foo/bar/g' file.txt` |
| `awk` | Field/text processing. | → `awk '{print $1,$3}' data.txt` |

---

## 🧰 4. File Permissions & Ownership

| Command | Description | Example |
| --- | --- | --- |
| `chmod` | Change file permissions. | → `chmod 755 script.sh` |
| `chown` | Change owner. | → `sudo chown user file` |
| `chgrp` | Change group. | → `sudo chgrp dev file` |
| `umask` | Set default file permissions. | → `umask 022` |
| `sudo` | Run command as root. | → `sudo apt update` |
| `su` | Switch user. | → `su root` |
| `passwd` | Change password. | → `passwd` |

---

## 🧮 5. Disk, Storage & Filesystems

| Command | Description | Example |
| --- | --- | --- |
| `df -h` | Show disk usage by filesystem. | → `df -h` |
| `du -sh` | Show directory size. | → `du -sh /var/log` |
| `mount` | Mount filesystem/device. | → `sudo mount /dev/sdb1 /mnt` |
| `umount` | Unmount. | → `sudo umount /mnt` |
| `lsblk` | List block devices. | → `lsblk` |
| `blkid` | Display UUIDs of disks. | → `sudo blkid` |
| `fdisk` | Manage partitions (MBR). | → `sudo fdisk -l` |
| `parted` | Partition editor. | → `sudo parted /dev/sda` |
| `mkfs.ext4` | Create ext4 filesystem. | → `sudo mkfs.ext4 /dev/sdb1` |
| `fsck` | Check and repair filesystem. | → `sudo fsck /dev/sda1` |
| `mount -t nfs` | Mount network share. | → `sudo mount -t nfs server:/data /mnt` |

---

## ⚙️ 6. System Info & Monitoring

| Command | Description | Example |
| --- | --- | --- |
| `top` | Display active processes. | → `top` |
| `htop` | Interactive process viewer. | → `sudo apt install htop` |
| `ps aux` | List all processes. | → `ps aux |
| `free -h` | Display RAM usage. | → `free -h` |
| `vmstat` | Show memory & CPU stats. | → `vmstat 2` |
| `lscpu` | CPU details. | → `lscpu` |
| `lshw` | Hardware details. | → `sudo lshw` |
| `lsusb` | Show USB devices. | → `lsusb` |
| `lspci` | Show PCI devices. | → `lspci` |
| `uptime` | System uptime and load. | → `uptime` |
| `who` | Show logged-in users. | → `who` |
| `w` | Show who is logged in and what they’re doing. | → `w` |
| `last` | Login history. | → `last` |
| `dmesg` | Kernel ring buffer messages. | → `dmesg |

---

## 🔌 7. Networking Essentials

| Command | Description | Example |
| --- | --- | --- |
| `ip a` | Show IP addresses. | → `ip a` |
| `ifconfig` | Show network interfaces (deprecated). | → `sudo apt install net-tools` |
| `ping` | Test connectivity. | → `ping -c 4 google.com` |
| `traceroute` | Trace route to host. | → `traceroute 8.8.8.8` |
| `netstat -tulnp` | Show ports & connections. | → `sudo netstat -tulnp` |
| `ss -tuln` | Modern replacement for netstat. | → `ss -tuln` |
| `curl` | Fetch a URL. | → `curl https://example.com` |
| `wget` | Download file. | → `wget https://file.com/app.deb` |
| `scp` | Copy over SSH. | → `scp file user@server:/tmp` |
| `rsync` | Sync directories. | → `rsync -avz src/ dest/` |
| `ufw` | Firewall management. | → `sudo ufw enable` |
| `ufw allow 22/tcp` | Allow SSH through firewall. | → `sudo ufw allow 22/tcp` |
| `nmcli` | Manage NetworkManager. | → `nmcli dev status` |

---

## 👥 8. Users & Groups

| Command | Description | Example |
| --- | --- | --- |
| `id` | Show user ID and groups. | → `id` |
| `useradd` | Create user. | → `sudo useradd -m rezoan` |
| `usermod` | Modify user. | → `sudo usermod -aG sudo rezoan` |
| `userdel` | Delete user. | → `sudo userdel -r olduser` |
| `groupadd` | Create group. | → `sudo groupadd devs` |
| `groups` | Show groups for current user. | → `groups` |
| `adduser` | Interactive user creation. | → `sudo adduser test` |
| `deluser` | Remove user interactively. | → `sudo deluser test` |
| `passwd` | Change password. | → `passwd rezoan` |

---

## 📦 9. Package Management (APT)

| Command | Description | Example |
| --- | --- | --- |
| `sudo apt update` | Update package lists. | → `sudo apt update` |
| `sudo apt upgrade` | Upgrade all packages. | → `sudo apt upgrade` |
| `sudo apt install <pkg>` | Install package. | → `sudo apt install git` |
| `sudo apt remove <pkg>` | Remove package. | → `sudo apt remove nano` |
| `sudo apt purge <pkg>` | Remove with config files. | → `sudo apt purge nano` |
| `sudo apt autoremove` | Remove unused dependencies. | → `sudo apt autoremove` |
| `apt search <pkg>` | Search packages. | → `apt search nginx` |
| `dpkg -l` | List installed packages. | → `dpkg -l |
| `dpkg -i file.deb` | Install local deb package. | → `sudo dpkg -i app.deb` |
| `snap install <app>` | Install snap package. | → `sudo snap install code` |
| `snap list` | List installed snaps. | → `snap list` |

---

## 🕹 10. Power & System Control

| Command | Description | Example |
| --- | --- | --- |
| `reboot` | Restart system. | → `sudo reboot` |
| `shutdown -h now` | Power off immediately. | → `sudo shutdown -h now` |
| `shutdown -r +5` | Reboot in 5 minutes. | → `sudo shutdown -r +5` |
| `systemctl poweroff` | Power off via systemd. | → `sudo systemctl poweroff` |
| `systemctl reboot` | Reboot via systemd. | → `sudo systemctl reboot` |
| `systemctl status` | Show systemd summary. | → `systemctl status` |

---

## 🧩 11. Useful Utilities & Shortcuts

| Command | Description | Example |
| --- | --- | --- |
| `alias` | Create command shortcut. | → `alias ll='ls -la'` |
| `unalias` | Remove alias. | → `unalias ll` |
| `history -c` | Clear command history. | → `history -c` |
| `tar -czvf` | Create compressed archive. | → `tar -czvf backup.tar.gz /home/user` |
| `tar -xzvf` | Extract archive. | → `tar -xzvf backup.tar.gz` |
| `zip -r` | Compress files. | → `zip -r archive.zip folder/` |
| `unzip` | Extract zip. | → `unzip archive.zip` |
| `df -Th` | Show filesystem type + usage. | → `df -Th` |
| `uname -r` | Show kernel version. | → `uname -r` |

---

## 🔚 End of Part 2 Summary

You’ve now learned **over 300 commands** — this forms your **solid Ubuntu foundation**.

> 🧭 Tip: Run man <command> for deeper insights and hidden options.
> 
> 
> Example: `man rsync` will show advanced synchronization flags you’ll use later for hacking & backups.
> 

---
