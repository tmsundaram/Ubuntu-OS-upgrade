Playbook: Ubuntu-OS-upgrade
Using ansible upgrade major/minor release in an automated way. 
Tested on Ubuntu 14.04 and 16.04. Upgrade from 14.04 to 16.04 is fully supported.

for minor OS update/patching use this command.

#ansible-playbook os_update -K
 
To upgrade from Ubuntu 14.04 to 16.04. Use the command below.

#ansible-playbook dist_upgrade_os.yaml -K

To list the currently installec packages alone use this command.

#ansible-playbook os_update -K --tags collect_data

- Host name and remote user must set in ansible hosts file. Default: /etc/ansible/hosts
- User must have sudo privileges and ssh keys configured already

On any OS update/change activity the change in package details captured under /root/package_list/<remote hostname>
