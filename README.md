# ansible-bind-ha

This is a ansible playbook to create high available dns authoritative servers with bind9 on debian9

First, you need to copy inventory.ini-sample :
`cp inventory.ini-sample inventory.ini`

Then edit the file to list you servers.

You can customize configuration by editing the group_vars/all.yaml file.
```
# Set to true to display more information when running ansible playbook
debug: true
# The default internal zone name first configured
default_zone: dns.local.
# The default internal reverse zone name
default_reverse_zone: 1.168.192.in-addr.arpa.
# The size of the records in the reverse zone. Must be greater equal than 1, or lower equal than 4
reverse_size_ipv4: 1
```
