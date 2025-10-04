## Audit linux vm :heavy_exclamation_mark:
- os-releae
- hostname
- network config
- ntp
- dns
- users
- cron tasks
- iptables
- disks
- open ports
- kernel config
- containers

**Run playbook**
```
ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i 'ip-addr,' playbook.yaml -u username --ask-pass --ssh-extra-args='-o IdentitiesOnly=yes -o HostKeyAlgorithms=+ssh-rsa'
```
need enter username password

**Example**
```
ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -i '192.168.10.1,' playbook.yaml -u admin --ask-pass --ssh-extra-args='-o IdentitiesOnly=yes -o HostKeyAlgorithms=+ssh-rsa'
```
