# Jarkom Modul 5 I03 2023

**Group I03** 
**Members:** 
- Fauzan Ahmad Faisal (5025211067)
- Muhammad Ghifari Taqiuddin (5025211063)

# Topology
## GNS3
<img width="1010" alt="Topologi" src="https://github.com/ghifarit53/Jarkom-Modul-5-I03-2023/assets/59758342/5390efa8-b53a-45ee-9acc-7c2d1928941a">

## Subnet distribution
![Pembagian Subnet](https://github.com/ghifarit53/Jarkom-Modul-5-I03-2023/assets/59758342/e47a1979-150a-41b0-b9ff-7776db2b7b28)

<img width="992" alt="Subnet" src="https://github.com/ghifarit53/Jarkom-Modul-5-I03-2023/assets/59758342/b3c371e7-e99a-46f5-a3e0-0f296d4ef982">

## IP Tree VLSM
![VLSM I03 Modul 5](https://github.com/ghifarit53/Jarkom-Modul-5-I03-2023/assets/59758342/587786c5-3b58-4f9b-a956-1c4e62596f55)

## IP distribution according to the tree
<img width="898" alt="Pembagian IP VLSM" src="https://github.com/ghifarit53/Jarkom-Modul-5-I03-2023/assets/59758342/6942260b-7c4f-4136-a228-d9a74e68d887">

# Node Configuration
## Aura
```
auto eth0
iface eth0 inet dhcp

# A8
auto eth1
iface eth1 inet static
  address 10.60.9.149
  netmask 255.255.255.252

# A6
auto eth2
iface eth2 inet static
  address 10.60.9.141
  netmask 255.255.255.252

up route add -net 10.60.0.0 netmask 255.255.252.0 gw 10.60.9.150 # A9
up route add -net 10.60.4.0 netmask 255.255.252.0 gw 10.60.9.150 # A10
up route add -net 10.60.9.144 netmask 255.255.255.252 gw 10.60.9.142 # A7
up route add -net 10.60.9.136 netmask 255.255.255.252 gw 10.60.9.142 # A5
up route add -net 10.60.8.0 netmask 255.255.255.0 gw 10.60.9.142 # A4
```

## Heiter
```
auto lo
iface lo inet loopback

# A8
auto eth0
iface eth0 inet static
  address 10.60.9.150
  netmask 255.255.255.252
  gateway 10.60.9.149

# A9
auto eth1
iface eth1 inet static
  address 10.60.0.1
  netmask 255.255.252.0

# A10
auto eth2
iface eth2 inet static
  address 10.60.4.1
  netmask 255.255.252.0

up route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.60.9.149 # Default routing
up route add -net 10.60.9.140 netmask 255.255.255.252 gw 10.60.9.149 # A6
up route add -net 10.60.9.144 netmask 255.255.255.252 gw 10.60.9.149 # A7
up route add -net 10.60.9.136 netmask 255.255.255.252 gw 10.60.9.149 # A5
up route add -net 10.60.8.0 netmask 255.255.255.0 gw 10.60.9.149 # A4
```

## Sein
```
# A10
auto eth0
iface eth0 inet static
  address 10.60.4.2
  netmask 255.255.252.0
  gateway 10.60.4.1
```

## Frieren
```
auto lo
iface lo inet loopback

# A6
auto eth0
iface eth0 inet static
  address 10.60.9.142
  netmask 255.255.255.252
  gateway 10.60.9.141

# A7
auto eth1
iface eth1 inet static
  address 10.60.9.145
  netmask 255.255.255.252

# A5
auto eth2
iface eth2 inet static
  address 10.60.9.137
  netmask 255.255.255.252

up route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.60.9.141 # Default routing
up route add -net 10.60.9.148 netmask 255.255.255.252 gw 10.60.9.141 # A8
up route add -net 10.60.0.0 netmask 10.60.3.255 gw 10.60.9.141 # A9
up route add -net 10.60.4.0 netmask 255.255.252.0 gw 10.60.9.141 # A10
up route add -net 10.60.8.0 netmask 255.255.255.0 gw 10.60.9.138 # A4
```

## Himmel
```
auto lo
iface lo inet loopback

# A5
auto eth0
iface eth0 inet static
  address 10.60.9.138
  netmask 255.255.255.252
  gateway 10.60.9.137

# A4
auto eth1
iface eth1 inet static
  address 10.60.8.1
  netmask 255.255.255.0

up route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.60.9.137 # Default routing
up route add -net 10.60.9.140 netmask 255.255.255.252 gw 10.60.9.137 # A6
up route add -net 10.60.9.144 netmask 255.255.255.252 gw 10.60.9.137 # A7
up route add -net 10.60.9.148 netmask 255.255.255.252 gw 10.60.9.137 # A8
up route add -net 10.60.0.0 netmask 255.255.252.0 gw 10.60.9.137 # A9
up route add -net 10.60.4.0 netmask 255.255.252.0 gw 10.60.9.137 # A10
```