# PROJECT
Mini-project
# DEFNITION
In the LAN architecture, a single DHCP-enabled router provides IP addressing and the switch is
configured with two VLANs VLAN 10 assigned to the HR department and VLAN 20 assigned to the
sales department .

# DHCP- ROUTING CLI-COMMANDS
Router# config terminal

Router(config)# ip dhcp pool LAN 1

Router(dhcp - config)# network 192.168.0.0 255.255.255.0

Router(dhcp - config)# default - router 192.168.0.1
# SWITCH-VLAN CLI-COMMANDS

Switch# config terminal

Switch(config)# int fa 0/1

Switch(config - if)# switchport mode access

Switch(config - if)# switchport access vlan 10

exit

Switch(config)# int fa 0/2

Switch(config - if)# switchport mode access

Switch(config - if)# switchport access vlan 10

exit

Switch# config terminal

Switch(config)# int fa 0/3

Switch(config - if)# switchport mode access

Switch(config - if)# switchport access vlan 20

exit

Switch(config)# int fa 0/4

Switch(config - if)# switchport mode access

Switch(config - if)# switchport access vlan 20

exit
