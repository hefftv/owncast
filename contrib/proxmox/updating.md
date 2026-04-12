# Updating Owncast on Proxmox 
**This file was created to migrate from Owncast v0.2.4 to v0.2.5**

## Proxmox LXC
*From Upgrade instructions from 0.2.4*
1. Stop the service from running. run `systemctl stop owncast.service`
   Be sure to check via `top` that no owncast process is running
2. (non-root install) change user to owncast user or process owner. `owncast": su -c `
3. Change to the directory where Owncast is installed on your server. Default is `/opt/owncast/` 
** Be sure you install this *inside* this directory. Installing owncast inside `/opt/` will break your install**
4. If you’ve customized your web interface in any way you will want to back up the files you’ve changed or customized. 
5. Run the installer `curl https://owncast.online/install.sh |bash` 
6. Restart the service. If you're running under systemd `systemctl start owncast.service`.
