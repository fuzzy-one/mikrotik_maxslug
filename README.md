# maxslug's Mikrotik Networking Configuration Files

```mermaid
graph LR;
WAN1[Fiber ONT] ---|DHCP,EAP| Router(Router<br />rb4011);
WAN2[WISP] ---|DHCP| Router;
Router ---|Trunk| WAP2((WAP2<br />cap ac));
Router ---|Trunk| WAP3((WAP3<br />cap ac));
Router ---|Trunk| SW1(SW1<br />crs109);
Router ---|VLAN200| Server;
Router ---|VLAN400| ATA;
SW1 ---|Trunk| WAP1((WAP1<br />cap ac));
Router ---|Trunk| SW2(SW2<br />crs109);
SW2 ---|VLAN300| Backup{Backup<br />SSID};
WAP1 ---|VLAN100| Admin{Admin<br />SSID};
WAP1 ---|VLAN200| LAN{LAN<br />SSID};
WAP1 ---|VLAN300| Guest{Guest<br />SSID};
```
