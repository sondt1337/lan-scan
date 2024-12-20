# network-lan-scanner

A powerful Python-based network scanning tool that detects and analyzes devices on your local network.

## Features

- 🔍 Auto-detection of available local networks
- 📱 Device discovery and status checking
- 📍 Detailed device information including:
  - IP address
  - MAC address
  - Vendor identification (via MAC address)
  - Open ports with service identification
- ⚡ Multi-threaded scanning for improved performance
- 📊 Clean tabulated results display
- 📈 Scanning statistics and metrics

## System Requirements

- Python 3.6+
- Required Python packages:
  ```
  ipaddress
  netifaces
  requests
  tabulate
  ```

## Example
```
=== Network Scanner v3.0 ===

Available networks:
1. 127.0.0.0/8 (Interface: lo)
2. 192.168.39.0/24 (Interface: ens160)
3. 172.17.0.0/16 (Interface: docker0)
4. 172.18.0.0/16 (Interface: br-810b879b415b)
5. 192.168.122.0/24 (Interface: virbr0)

Select network to scan (enter number): 2
Scanning results:
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| IP             | MAC               | Vendor                                         | Open Ports                                                                                                                                                                           |
+================+===================+================================================+======================================================================================================================================================================================+
| 192.168.39.1   | xx:xx:xx:xx:xx:xx | Routerboard.com                                | 53(DNS), 1723(PPTP), 1194(OpenVPN), 8291(Mikrotik-API)                                                                                                                               |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.8   | xx:xx:xx:xx:xx:xx | Routerboard.com                                | 1194(OpenVPN), 1723(PPTP), 8291(Mikrotik-API)                                                                                                                                        |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.10  | xx:xx:xx:xx:xx:xx | Hangzhou Ezviz Software Co.,Ltd.               | 8000(HTTP-Alt), 554(RTSP)                                                                                                                                                            |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.26  | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 7070(RealPlayer)                                                                                                                                                                     |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.27  | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 22(SSH), 25565(Minecraft)                                                                                                                                                            |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.34  | xx:xx:xx:xx:xx:xx | Hangzhou Ezviz Software Co.,Ltd.               | 8000(HTTP-Alt)                                                                                                                                                                       |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.35  | xx:xx:xx:xx:xx:xx | Routerboard.com                                | N/A                                                                                                                                                                                  |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.36  | xx:xx:xx:xx:xx:xx | Ubiquiti Inc                                   | 22(SSH)                                                                                                                                                                              |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.37  | xx:xx:xx:xx:xx:xx | TP-LINK TECHNOLOGIES CO.,LTD.                  | N/A                                                                                                                                                                                  |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.38  | xx:xx:xx:xx:xx:xx | Hon Hai Precision Ind. Co.,Ltd.                | 80(HTTP), 8443(HTTPS-Alt), 9000(Node), 8009(AJP)                                                                                                                                     |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.40  | xx:xx:xx:xx:xx:xx | Ubiquiti Inc                                   | 22(SSH)                                                                                                                                                                              |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.45  | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 7070(RealPlayer)                                                                                                                                                                     |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.46  | xx:xx:xx:xx:xx:xx | Cisco Systems, Inc                             | 80(HTTP), 443(HTTPS), 23(TELNET)                                                                                                                                                     |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.51  | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 80(HTTP), 22(SSH), 6000(X11)                                                                                                                                                         |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.52  | xx:xx:xx:xx:xx:xx | ASUSTek COMPUTER INC.                          | 22(SSH), 7070(RealPlayer)                                                                                                                                                            |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.53  | xx:xx:xx:xx:xx:xx | Ruijie Networks Co.,LTD                        | 80(HTTP), 443(HTTPS), 53(DNS), 1883(MQTT)                                                                                                                                            |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.54  | xx:xx:xx:xx:xx:xx | Ruijie Networks Co.,LTD                        | 80(HTTP), 443(HTTPS), 53(DNS), 1883(MQTT)                                                                                                                                            |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.64  | xx:xx:xx:xx:xx:xx | Hangzhou Hikvision Digital Technology Co.,Ltd. | 443(HTTPS), 8443(HTTPS-Alt), 80(HTTP), 8000(HTTP-Alt), 554(RTSP)                                                                                                                     |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.71  | xx:xx:xx:xx:xx:xx | ASUSTek COMPUTER INC.                          | 22(SSH), 7070(RealPlayer), 9090(HAProxy)                                                                                                                                             |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.86  | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 7070(RealPlayer)                                                                                                                                                                     |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.88  | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | N/A                                                                                                                                                                                  |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.89  | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 22(SSH)                                                                                                                                                                              |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.92  | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 3389(RDP), 139(NetBIOS), 135(MSRPC), 445(SMB), 5357(WSDAPI)                                                                                                                          |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.100 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 22(SSH)                                                                                                                                                                              |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.107 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 7070(RealPlayer)                                                                                                                                                                     |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.111 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 3389(RDP)                                                                                                                                                                            |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.127 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 8081(HTTP-Alt), 80(HTTP), 443(HTTPS), 22(SSH), 3306(MySQL), 9090(HAProxy)                                                                                                            |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.129 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 8080(Webmin), 6666(IRC-FileTransfer), 3389(RDP), 139(NetBIOS), 445(SMB), 135(MSRPC), 5357(WSDAPI)                                                                                    |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.146 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 22(SSH)                                                                                                                                                                              |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.150 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | N/A                                                                                                                                                                                  |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.158 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 22(SSH)                                                                                                                                                                              |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.163 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 22(SSH), 3389(RDP), 7070(RealPlayer)                                                                                                                                                 |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.164 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 80(HTTP), 22(SSH), 3389(RDP), 8009(AJP)                                                                                                                                              |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.182 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 80(HTTP), 8888(HTTP-Alt), 22(SSH)                                                                                                                                                    |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.183 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 3389(RDP), 22(SSH), 7070(RealPlayer), 5938(TeamViewer)                                                                                                                               |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.186 | xx:xx:xx:xx:xx:xx | ASUSTek COMPUTER INC.                          | 80(HTTP), 8000(HTTP-Alt), 8080(Webmin), 5000(UPnP), 6666(IRC-FileTransfer), 22(SSH), 6379(Redis), 5432(PostgreSQL), 9200(Elasticsearch), 7070(RealPlayer), 9090(HAProxy), 9000(Node) |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.191 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 8000(HTTP-Alt), 22(SSH), 3389(RDP), 5432(PostgreSQL), 7070(RealPlayer)                                                                                                               |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.200 | xx:xx:xx:xx:xx:xx | Micro-Star INTL CO., LTD.                      | 80(HTTP), 8000(HTTP-Alt), 443(HTTPS), 22(SSH), 902(VMware)                                                                                                                           |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.201 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 80(HTTP), 22(SSH), 53(DNS)                                                                                                                                                           |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.202 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 80(HTTP), 22(SSH)                                                                                                                                                                    |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.204 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | 22(SSH), 3389(RDP)                                                                                                                                                                   |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.240 | xx:xx:xx:xx:xx:xx | VMware, Inc.                                   | N/A                                                                                                                                                                                  |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.244 | xx:xx:xx:xx:xx:xx | KTNF                                           | 80(HTTP), 8000(HTTP-Alt), 443(HTTPS), 22(SSH), 902(VMware)                                                                                                                           |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.245 | xx:xx:xx:xx:xx:xx | KTNF                                           | 80(HTTP), 8000(HTTP-Alt), 443(HTTPS), 902(VMware)                                                                                                                                    |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| 192.168.39.246 | xx:xx:xx:xx:xx:xx | Micro-Star INTL CO., LTD.                      | 8000(HTTP-Alt), 443(HTTPS), 80(HTTP), 902(VMware)                                                                                                                                    |
+----------------+-------------------+------------------------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Statistics:
- Scanning time: 90.68 seconds
- Number of devices found: 45
```
>  I cloak my MAC address to shield my identity and ensure my network presence remains secure. It's not just about staying hidden—it's about taking control of my digital footprint in a world where privacy is power...
