# unifi-tools
Some tools to perform odd or non-controller tasks Ubiquiti's Unifi APs


## Get These Tools
```
git clone https://github.com/anotherbhav/unifi-tools

cd unifi-tools
```

# reboot_aps.yml

## Why
- I have problems after upgrades where some APs don't let devices connect
- a reboot of the AP always fixes the problem
- I don't want to sit here all day and remember to reboot each AP

## Behavior
- reboot a group of APs listed in ansible.hosts
- only reboot 1 AP at a time
- wait 90s for AP to come back
- if it fails, stop rebooting the rest

## example
```
ansible-playbook reboot_aps.yml

$ ansible-playbook reboot_aps.yml
Enter Access-Point admin credentials:
...
```
