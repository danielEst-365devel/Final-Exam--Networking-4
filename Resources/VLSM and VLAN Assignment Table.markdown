# VLSM and VLAN Assignment Table

| Device/Subnet             | VLAN | IP Address        | Subnet Mask       | Gateway         | Subnet Range        | Role                     |
|---------------------------|------|-------------------|-------------------|-----------------|---------------------|--------------------------|
| **Router (Cisco 2911)**   |      |                   |                   |                 |                     |                          |
| G0/0.10 (Floor 1 GW)    | 10   | 192.168.0.1       | 255.255.255.192   | -               | 192.168.0.0-63      | Floor 1 Gateway          |
| G0/0.20 (Floor 2 GW)    | 20   | 192.168.0.65      | 255.255.255.192   | -               | 192.168.0.64-127    | Floor 2 Gateway          |
| G0/0.30 (Floor 3 GW)    | 30   | 192.168.0.129     | 255.255.255.192   | -               | 192.168.0.128-191   | Floor 3 Gateway          |
| G0/0.40 (Floor 4 GW)    | 40   | 192.168.0.193     | 255.255.255.192   | -               | 192.168.0.192-255   | Floor 4 Gateway          |
| G0/0.99 (Management GW) | 99   | 192.168.0.145     | 255.255.255.240   | -               | 192.168.0.144-159   | Management Gateway       |
| G0/1 (to ISP)           | -    | 192.168.0.154     | 255.255.255.252   | 192.168.0.153   | 192.168.0.152-155   | ISP WAN Link             |
| **Core Switch (Cisco 2960-24TT)** |      |                   |                   |                 |                     |                          |
| VLAN 99 Interface       | 99   | 192.168.0.146     | 255.255.255.240   | 192.168.0.145   | 192.168.0.144-159   | Management Interface     |
| FA0/1 (to Floor 1)      | Trunk| -                 | -                 | -               | -                   | Core-to-Floor 1 Trunk    |
| FA0/2 (to Floor 2)      | Trunk| -                 | -                 | -               | -                   | Core-to-Floor 2 Trunk    |
| FA0/3 (to Floor 3)      | Trunk| -                 | -                 | -               | -                   | Core-to-Floor 3 Trunk    |
| FA0/4 (to Floor 4)      | Trunk| -                 | -                 | -               | -                   | Core-to-Floor 4 Trunk    |
| **Floor 1 Switch (Cisco 2960-24TT)** |      |                   |                   |                 |                     |                          |
| VLAN 99 Interface       | 99   | 192.168.0.147     | 255.255.255.240   | 192.168.0.145   | 192.168.0.144-159   | Management Interface     |
| Floor 1 Subnet          | 10   | 192.168.0.0/26    | 255.255.255.192   | 192.168.0.1     | 192.168.0.0-63      | End Devices/Wireless     |
| **Floor 2 Switch (Cisco 2960-24TT)** |      |                   |                   |                 |                     |                          |
| VLAN 99 Interface       | 99   | 192.168.0.148     | 255.255.255.240   | 192.168.0.145   | 192.168.0.144-159   | Management Interface     |
| Floor 2 Subnet          | 20   | 192.168.0.64/26   | 255.255.255.192   | 192.168.0.65    | 192.168.0.64-127    | End Devices/Wireless/Srv |
| **Floor 3 Switch (Cisco 2960-24TT)** |      |                   |                   |                 |                     |                          |
| VLAN 99 Interface       | 99   | 192.168.0.149     | 255.255.255.240   | 192.168.0.145   | 192.168.0.144-159   | Management Interface     |
| Floor 3 Subnet          | 30   | 192.168.0.128/26  | 255.255.255.192   | 192.168.0.129   | 192.168.0.128-191   | End Devices/Wireless     |
| **Floor 4 Switch (Cisco 2960-24TT)** |      |                   |                   |                 |                     |                          |
| VLAN 99 Interface       | 99   | 192.168.0.150     | 255.255.255.240   | 192.168.0.145   | 192.168.0.144-159   | Management Interface     |
| Floor 4 Subnet          | 40   | 192.168.0.192/26  | 255.255.255.192   | 192.168.0.193   | 192.168.0.192-255   | End Devices/Wireless     |
| **ISP Cloud**             | -    | 192.168.0.153     | 255.255.255.252   | -               | 192.168.0.152-155   | WAN Endpoint             |