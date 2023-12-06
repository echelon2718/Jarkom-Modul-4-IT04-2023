# Jarkom Modul 4 IT04 2023
- Kevin Putra Santoso (5027211030)
- Bagus Cahyo Arrasyid (5027211033)

## Modul 4
### Lakukan konfigurasi sesuai dengan Topologi yang sudah diberikan
### Topologi CPT

![it04_topocpt](https://github.com/asxklm/Jarkom-Modul-4-IT04-2023/assets/113827418/b982be2c-8c6b-49fe-9a54-0ef2364acb27)

### Topologi GNS3

![it04_topogns3](https://github.com/asxklm/Jarkom-Modul-4-IT04-2023/assets/113827418/d0c6c386-3899-4628-9908-873854f59585)

### Prefix IP
Kelompok kami IT04 mempunyai prefix IP `192.235.x.x`

## VLSM
### Rute / Subneting (A)
Kelompok kami mengelompokkan subnet dan merutekan topologi diatas sebagai berikut

![subnetvlsm(A)](https://github.com/asxklm/Jarkom-Modul-4-IT04-2023/assets/113827418/db1f9086-5805-4a68-9196-fe50ce49fb70)

### Tree 
Perhitungan VLSM hanya membutuhkan perhitungan total `Host` yang ditampung dan dapat langsung dilakukan pembagian IP

![it04_treevlsm](https://github.com/asxklm/Jarkom-Modul-4-IT04-2023/assets/113827418/241f0b7b-3db7-42fc-a2b8-89c39371b8a9)

### Pembagian IP
Berdasar Tree diatas dapat dilakukan pembagian IP sebagai berikut

![it04_pembagianipvlsm](https://github.com/asxklm/Jarkom-Modul-4-IT04-2023/assets/113827418/057de9d3-a03f-4c58-98c3-f7e6bfc89654)

### Routing
```bash
#### Aura ####

192.235.7.160/27 via 192.235.7.110 # A4
192.235.7.112/30 via 192.235.7.110 # A5
192.235.7.116/30 via 192.235.7.110 # A6
192.235.24.0/21  via 192.235.7.110 # A7
192.235.16.0/22  via 192.235.7.110 # A8
192.235.7.120/30 via 192.235.7.110 # A9

192.235.7.124/30 via 192.235.7.126 # A11
192.235.7.152/29 via 192.235.7.126 # A13
192.235.7.132/30 via 192.235.7.126 # A14
192.235.20.0/22 via 192.235.7.126 # A15
192.235.9.0/24 via 192.235.7.126 # A16
192.235.7.136/30 via 192.235.7.126 # A17
192.235.10.0/23 via 192.235.7.126 # A18
192.235.7.140/30 via 192.235.7.126 # A19
192.235.7.192/26 via 192.235.7.126 # A20
192.235.12.0/22 via 192.235.7.126 # A21

192.235.7.104/30 via 192.235.7.106 # A1
192.235.8.0/24 via 192.235.7.106 # A2
192.235.7.108/30 via 192.235.7.110 # A3

#### Denken ####
0.0.0.0/0 via 192.235.7.105

#### Frieren ####
0.0.0.0/0 via 192.235.7.109
192.235.7.116/30 via 192.235.7.114
192.235.24.0/21 via 192.235.7.114
192.235.16.0/22 via 192.235.7.114
192.235.7.120/30 via 192.235.7.114
192.235.7.144/29 via 192.235.7.114
192.235.7.112/30 via 192.235.7.114

#### Flamme ####
0.0.0.0/0 via 192.235.7.113
192.235.24.0/21 via 192.235.7.118
192.235.7.144/29 via 192.235.7.122
192.235.7.116/30 via 192.235.7.118
192.235.7.120/30 via 192.235.7.122

#### Fern ####
0.0.0.0/0 via 192.235.7.117

#### Himmel ####
0.0.0.0/0 via 192.235.7.121

#### Eisen ####
0.0.0.0/0 via 192.235.7.125
192.235.20.0/22 via 192.235.7.134
192.235.9.0/24 via 192.235.7.134
192.235.10.0/23 via 192.235.7.138
192.235.7.140/30 via 192.235.7.138
192.235.7.192/26 via 192.235.7.138
192.235.12.0/22 via 192.235.7.138
192.235.7.132/30 via 192.235.7.134
192.235.7.136/30 via 192.235.7.138

#### Lugner ####
0.0.0.0/0 via 192.235.7.133

#### Lawine ####
0.0.0.0/0 via 192.235.7.141
192.235.12.0/22 via 192.235.7.194
192.235.7.192/26 via 192.235.7.194

#### Heiter ####
0.0.0.0/0 via 192.235.7.193
```

## CIDR
### Pengelompokan subneting 
pada CIDR menggunakkan `Rute` yang masih sama dengan VLSM dengan pengelompokan lebih lanjut yang berdasar pada Gabungkan subnet paling jauh di dalam topologi.

![subnetingcidr](https://github.com/asxklm/Jarkom-Modul-4-IT04-2023/assets/113827418/4a28c157-e15d-491a-b35e-1b587530c78b)

### Tree 
Tree pada CIDR dibuat berdasar pengelompokan subnet diatas

![it04_treecidr](https://github.com/asxklm/Jarkom-Modul-4-IT04-2023/assets/113827418/63eafbd2-9056-4719-a17a-8a6f3949c5a5)

### Pembagian IP
Berdasar Tree diatas dapat dilakukan pembagian IP sebagai berikut

![it04_pembagianipcidr](https://github.com/asxklm/Jarkom-Modul-4-IT04-2023/assets/113827418/29c92eb9-cc7f-42df-9abb-4c59c3d3d8f4)


### Konfigurasi Network

#### RoyalCapital (63 Host)

```
#A1
auto eth0
iface eth0 inet static
address 192.235.8.5
netmask 255.255.255.0
gateway 192.235.8.1
```

#### WilleRegion (63 Host)

```
#A1
auto eth0
iface eth0 inet static
address 192.235.8.10
netmask 255.255.255.0
gateway 192.235.8.1
```

#### Denken 

```
auto lo
iface lo inet loopback

#A2
auto eth0
iface eth0 inet static
address 192.235.7.106
netmask 255.255.255.252
gateway 192.235.7.105

#A1
auto eth1
iface eth1 inet static
address 192.235.8.1
netmask 255.255.255.0
```

#### Aura 

```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet dhcp

#A20
auto eth1
iface eth1 inet static
address 192.235.7.141
netmask 255.255.255.252

#A2
auto eth2
iface eth2 inet static
address 192.235.7.105
netmask 255.255.255.252

#A3
auto eth3
iface eth3 inet static
address 192.235.7.109
netmask 255.255.255.252
```

#### Frieren 

```
auto lo
iface lo inet loopback

#A20
auto eth0
iface eth0 inet static
address 192.235.7.142
netmask 255.255.255.252
gateway 192.235.7.141

#A19
auto eth1
iface eth1 inet static
address 192.235.7.137
netmask 255.255.255.252

#A21
auto eth2
iface eth2 inet static
address 192.235.7.161
netmask 255.255.255.224
```

#### LakeKorridor (24 Host)

```
#A21
auto eth0
iface eth0 inet static
address 192.235.7.165
netmask 255.255.255.224
gateway 192.235.7.161
```

#### Flamme 

```
auto lo
iface lo inet loopback

#A19
auto eth0
iface eth0 inet static
address 192.235.7.138
netmask 255.255.255.252
gateway 192.235.7.137

#A14
auto eth1
iface eth1 inet static
address 192.235.7.129
netmask 255.255.255.252

#A16
auto eth2
iface eth2 inet static
address 192.235.20.1
netmask 255.255.252.0

#A17
auto eth3
iface eth3 inet static
address 192.235.7.133
netmask 255.255.255.252
```

#### Fern 

```
auto lo
iface lo inet loopback

#A17
auto eth0
iface eth0 inet static
address 192.235.7.134
netmask 255.255.255.252
gateway 192.235.7.133

#A18
auto eth1
iface eth1 inet static
address 192.235.24.1
netmask 255.255.248.0
```

#### LaubHills (397 Host)

```
auto eth0
iface eth0 inet static
address 192.235.25.5
netmask 255.255.248.0
gateway 192.235.24.1
```

#### AppetitRegion (625 Host)

```
auto eth0
iface eth0 inet static
address 192.235.25.10
netmask 255.255.248.0
gateway 192.235.24.1
```

#### RohrRoad (1000 Host)

```
#A16
auto eth0
iface eth0 inet static
address 192.235.20.5
netmask 255.255.252.0
gateway 192.235.20.1
```

#### Himmel 

```
auto lo
iface lo inet loopback

#A14
auto eth0
iface eth0 inet static
address 192.235.7.130
netmask 255.255.255.252
gateway 192.235.7.129

#A13
auto eth1
iface eth1 inet static
address 192.235.7.145
netmask 255.255.255.248
```

#### ShcwerMountains (5 Host)

```
auto eth0
iface eth0 inet static
address 192.235.7.147
netmask 255.255.255.248
gateway 192.235.7.145
```

#### Eisen 

```
auto lo
iface lo inet loopback

#A3
auto eth0
iface eth0 inet static
address 192.235.7.110
netmask 255.255.255.252
gateway 192.235.7.109

#A15
auto eth1
iface eth1 inet static
address 192.235.7.153
netmask 255.255.255.248

#A4
auto eth2
iface eth2 inet static
address 192.235.7.113
netmask 255.255.255.252

#A5
auto eth3
iface eth3 inet static
address 192.235.7.117
netmask 255.255.255.252

#A8
auto eth4
iface eth4 inet static
address 192.235.7.121
netmask 255.255.255.252
```

#### Stark 

```
auto eth0
iface eth0 inet static
address 192.235.7.114
netmask 255.255.252.0
gateway 192.235.7.113
```

#### Lugner 

```
auto lo
iface lo inet loopback

#A5
auto eth0
iface eth0 inet static
address 192.235.7.118
gateway 192.235.7.117
netmask 255.255.255.252

#A6
auto eth1
iface eth1 inet static
address 192.235.12.1
netmask 255.255.252.0

#A7
auto eth2
iface eth2 inet static
address 192.235.9.1
netmask 255.255.255.0
```

#### TurkRegion (1000 Host)

```
auto eth0
iface eth0 inet static
address 192.235.12.5
netmask 255.255.252.0
gateway 192.235.12.1
```

#### GrobeForest (250 Host)

```
auto eth0
iface eth0 inet static
address 192.235.9.5
netmask 255.255.255.0
gateway 192.235.9.1
```

#### Richter 

```
auto eth0
iface eth0 inet static
address 192.235.7.154
netmask 255.255.252.0
gateway 192.235.7.153
```

#### Revolte

```
auto eth0
iface eth0 inet static
address 192.235.7.155
netmask 255.255.252.0
gateway 192.235.7.153
```

#### Linie 

```
auto lo
iface lo inet loopback

#A8
auto eth0
iface eth0 inet static
address 192.235.7.122
gateway 192.235.7.121
netmask 255.255.255.252

#A9
auto eth1
iface eth1 inet static
address 192.235.10.1
netmask 255.255.254.0

#A10
auto eth2
iface eth2 inet static
address 192.235.7.125
netmask 255.255.255.252
```

#### GranzChannel (254 Host)

```
auto eth0
iface eth0 inet static
address 192.235.10.5
netmask 255.255.254.0
gateway 192.235.10.1
```

#### Lawine 

```
auto lo
iface lo inet loopback

#A10
auto eth0
iface eth0 inet static
address 192.235.7.126
netmask 255.255.255.252
gateway 192.235.7.125

#A11
auto eth1
iface eth1 inet static
address 192.235.7.193
netmask 255.255.255.192
```

#### BredtRegion (29 Host)

```
auto eth0
iface eth0 inet static
address 192.235.7.197
netmask 255.255.255.192
gateway 192.235.7.193
```

#### Heiter 

```
auto lo
iface lo inet loopback

#A11
auto eth0
iface eth0 inet static
address 192.235.7.222
netmask 255.255.255.192
gateway 192.235.7.193

#A12
auto eth1
iface eth1 inet static
address 192.235.16.1
netmask 255.255.252.0
```

#### Sein 

```
auto eth0
iface eth0 inet static
address 192.235.16.2
netmask 255.255.252.0
gateway 192.235.16.1
```

#### RiegelCanyon (510 Host)

```
auto eth0
iface eth0 inet static
address 192.235.16.7
netmask 255.255.252.0
gateway 192.235.16.1
```

### Routing 

#### Denken 

```
up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.235.7.105
```

#### Lugner 

```
up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.235.7.110
```

#### Linie 

```
up route add -net 192.235.7.192 netmask 255.255.255.192 gw 192.235.7.126
up route add -net 192.235.16.0 netmask 255.255.252.0 gw 192.235.7.126
```

#### Lawine 

```
up route add -net 192.235.16.0 netmask 255.255.252.0 gw 192.235.7.222
```

#### Heiter

```
up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.235.7.126
```

#### Himmel 

```
up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.235.7.138
```

#### Flamme 

```
up route add -net 192.235.24.0 netmask 255.255.248.0 gw 192.235.7.134
up route add -net 192.235.7.144 netmask 255.255.255.248 gw 192.235.7.130
```

#### Fern 

```
up route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.235.7.138
```

#### Frieren

```
up route add -net 192.235.7.132 netmask 255.255.255.252 gw 192.235.7.138
up route add -net 192.235.24.0 netmask 255.255.248.0 gw 192.235.7.138
up route add -net 192.235.20.0 netmask 255.255.252.0 gw 192.235.7.138
up route add -net 192.235.7.128 netmask 255.255.255.252 gw 192.235.7.138
up route add -net 192.235.7.144 netmask 255.255.255.248 gw 192.235.7.138
```

#### Eisen 

```
up route add -net 192.235.12.0 netmask 255.255.252.0 gw 192.235.7.118
up route add -net 192.235.9.0 netmask 255.255.255.0 gw 192.235.7.118

up route add -net 192.235.10.0 netmask 255.255.254.0 gw 192.235.7.122
up route add -net 192.235.7.124 netmask 255.255.255.252 gw 192.235.7.122
up route add -net 192.235.7.192 netmask 255.255.255.192 gw 192.235.7.122
up route add -net 192.235.16.0 netmask 255.255.252.0 gw 192.235.7.122
```

#### Aura 

```
# Frieren
up route add -net 192.235.7.160 netmask 255.255.255.224 gw 192.235.7.142
up route add -net 192.235.7.136 netmask 255.255.255.252 gw 192.235.7.142
up route add -net 192.235.7.132 netmask 255.255.255.252 gw 192.235.7.142
up route add -net 192.235.24.0 netmask 255.255.248.0 gw 192.235.7.142
up route add -net 192.235.20.0 netmask 255.255.252.0 gw 192.235.7.142
up route add -net 192.235.7.128 netmask 255.255.255.252 gw 192.235.7.142
up route add -net 192.235.7.144 netmask 255.255.255.248 gw 192.235.7.142

# Denken
up route add -net 192.235.8.0 netmask 255.255.255.0 gw 192.235.7.106

# Eisen
up route add -net 192.235.7.112 netmask 255.255.255.252 gw 192.235.7.110
up route add -net 192.235.7.116 netmask 255.255.255.252 gw 192.235.7.110
up route add -net 192.235.12.0 netmask 255.255.252.0 gw 192.235.7.110
up route add -net 192.235.9.0 netmask 255.255.255.0 gw 192.235.7.110
up route add -net 192.235.7.120 netmask 255.255.255.252 gw 192.235.7.110
up route add -net 192.235.10.0 netmask 255.255.254.0 gw 192.235.7.110
up route add -net 192.235.7.124 netmask 255.255.255.252 gw 192.235.7.110
up route add -net 192.235.7.192 netmask 255.255.255.192 gw 192.235.7.110
up route add -net 192.235.16.0 netmask 255.255.252.0 gw 192.235.7.110
up route add -net 192.235.7.152 netmask 255.255.255.248 gw 192.235.7.110
```

