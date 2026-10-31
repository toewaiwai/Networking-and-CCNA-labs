<img width="431" height="121" alt="image" src="https://github.com/user-attachments/assets/65ae42bb-fb1e-4f36-8727-e6f52f48f204" />


Configure ASW01

<img width="926" height="311" alt="image" src="https://github.com/user-attachments/assets/06301cbe-4ca3-4d17-96b4-c06aa60a1d14" />

Configure ASW02

<img width="873" height="358" alt="image" src="https://github.com/user-attachments/assets/224dbadc-e0e3-4487-96ee-c9951b24ebe0" />


Configure DSW

```
Switch>en
Switch#conf t
Switch(config)#hostname DSW
DSW(config)#interface range Gig1/3, Gig1/4
DSW(config-if-range)#switchport mode trunk
DSW(config)#end
```

<img width="955" height="320" alt="image" src="https://github.com/user-attachments/assets/72fb90de-1ce1-4ee7-b1e5-85276906ecaa" />

Inter-VLAN routing

```
DSW(config)#vlan 10
DSW(config-vlan)#name HR
DSW(config-vlan)#vlan 20
DSW(config-vlan)#name Admin
DSW(config-vlan)#exit
```

```
DSW(config)#interface vlan 10
DSW(config-if)#ip address 192.168.1.254 255.255.255.0
DSW(config-if)#no shut
DSW(config-if)#exit
DSW(config)#interface vlan 20
DSW(config-if)#ip address 192.168.2.254 255.255.255.0
DSW(config-if)#no shut
```

<img width="940" height="268" alt="image" src="https://github.com/user-attachments/assets/e4451f00-b376-4e67-8af2-19a03d7de4d3" />


Verify

<img width="491" height="307" alt="image" src="https://github.com/user-attachments/assets/0b62253e-5a63-4dea-890d-01257dd94ad8" />



