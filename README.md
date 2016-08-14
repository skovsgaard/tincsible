# Introduction
This is a playbook for setting up a Tinc VPN of Raspberry Pis. In the interest of simplicity, it assumes you're running Raspbian on all of them.

It's is basically just a very simplified version of [ansible-tinc](https://github.com/thisismitch/ansible-tinc).

## Your `hosts` file
For this to work you will need to place a `hosts` file in this directory, containing data in the following format:

```
[vpn]
node01 vpn_ip=10.0.0.1 ansible_host=192.168.1.2
node02 vpn_ip=10.0.0.2 ansible_host=192.168.1.3
node04 vpn_ip=10.0.0.4 ansible_host=192.168.1.5

[removevpn]
node03 vpn_ip=10.0.0.3 ansible_host=192.168.1.4
```

You can basically just move lines between the two blocks depending on whether you want to uninstall Tinc and remove the node from the mesh or you want to add or re-add it.
