# Linux/Bash Commands
## Commands worthy of remembering.

|Commands|Description|Example|
|--------|-----------|-------|
|`clear`|Cleans the current terminal state|`clear`|
|`cd`|Changes the current directory|`cd` home/user/Desktop|
|`man`|Shows the manual for the specified command|`man` mkdir|
|`whoami`|Prints the current user| `whoami`|
|`sudo`|Allows us to run a command as root|`sudo` apt install cmatrix|
|`cp`| Copies the specified file to a new one| `cp` file.txt file_copy.txt|
|`wget`|Utility for downloading files from the web|`wget` https://git.io/vpn -O openvpn-install.sh|
|`pacman`|Package manager for Arch-based distributions| `sudo pacman -Syuu`|
|`useradd`|Creates a new user including a personal home dir| `sudo useradd -m newUser -G wheel -p 123456`|
|`touch`|Creates a new file| `touch file.txt`|
|`mkdir`|Creates a new directory| `mkdir newDir`|
|`rmdir`|Deletes the specified directory| `rmdir -rf newDir`|
|`tree`|displays a tree shaped list of the current directory and subdirectories| `tree`|
|`ls`|Lists the file in the specified route| `ls -l /bin/`|
|`cat`|Prints the content of a given file| `cat file.txt`|
|`mv`|Moves a given file to the specified route, can also be used to rename| `mv file.txt /bin/`|
|`grep`|Useful for searching inside files| `grep -rin "log" /home/*`|
|`ps`|Prints the current processes| `ps -A`|
|`chmod`|Changes the permissions for the given file or directory| `chmod 777 file.txt`|
|`su`|If a user is given, switches to it, if not, it switches to the root user| `su - newUser`|
|`pkill`|Kills the given process| `sudo pkill colord`|
|`history`|Prints all commands used until now on the terminal| `history`|
|`ln`|Creates a hard link with the given name to the given file. (if -s is used, creates a soft link)| `ln -s /var/log/pacman.log ~/pacman.log`|
|`crontab`|Allows to configure the crontab Daemon| `crontab -e`|
|`nano`|Text editor on the terminal| `nano file.txt`|
|`vim`|Text editor on the terminal| `vim file.txt`|
|`docker`|enables multiple operations with docker| `docker Build/images/run/ps`|
|`build`|Build an image from a docker file| `docker build ubuntu`|
|`images`|List all images on a Docker host| `Docker images`|
|`run`|Run an image| `docker run ubuntu`|
|`ps`|List all running and stopped instances| `docker ps`|
|`stop`|Stop a running instance| `docker stop ${instance id}`|
|`rm`|Remove an instance| `docker rm ${instance id}`|
|`rmi`|Remove an image| `docker rmi ubuntu`|
|`mdadm --create --verbose /${Folder}/md0 --level=stripe --raid-devices=2 ${Disk 1} ${Disk 2}`| Create Raid 0| `mdadm --create --verbose /dev/md0 --level=stripe --raid-devices=2 /dev/sdb1 /dev/sdc1`|
|`mdadm --create --verbose /${Folder}/md0 --level=1 --raid-devices=2 ${Disk 1} ${Disk 2}`| Create Raid 1| `mdadm --create --verbose /dev/md0 --level=1 --raid-devices=2 /dev/sdb1 /dev/sdc1`|
|`mdadm --create --verbose /${Folder}/md0 --level=10 --raid-devices=4 /dev/${Set of disks}`| Create Raid 1+0| `mdadm --create --verbose /dev/md0 --level=10 --raid-devices=4 /dev/sd[b-e]1`|
|`mount -t ext4 /${Folder}/md0 ${Location}`|Mount the raid in a specific location| `mount -t ext4 /dev/md0 /mnt/miraid`|
