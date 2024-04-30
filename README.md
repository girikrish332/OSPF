OSPF Configuration Guide

This guide outlines the OSPF (Open Shortest Path First) configuration for the network topology described. OSPF is a dynamic routing protocol used for routing within an Autonomous System (AS).
Network Topology
Router used in this network are c3600

The network consists of the following devices:

    Routers C3600: R1, R2, R3, R4, R5, R6
    PCs: PC1, PC2

Router Configurations
R1 Configuration

bash

en
conf t
int f0/0
ip add 192.168.20.10 255.255.255.0
no sh
exit

int f1/0
ip add 192.168.10.10 255.255.255.0
no sh
exit

int lo0
ip add 1.1.1.1 255.255.255.0
exit

router ospf 1
net 192.168.20.0 0.0.0.255 area 0
net 192.168.10.0 0.0.0.255 area 0

R2 Configuration

bash

en
conf t
int f0/0
ip add 192.168.20.20 255.255.255.0
no sh
exit

int f1/0
ip add 192.168.30.10 255.255.255.0
no sh
exit

int lo0
ip add 2.2.2.2 255.255.255.0
exit

router ospf 1
net 192.168.20.0 0.0.0.255 area 0
net 192.168.30.0 0.0.0.255 area 0

R3 Configuration

bash

en
conf t
int f0/0
ip add 192.168.30.20 255.255.255.0
no sh
exit

int f1/0
ip add 192.168.40.10 255.255.255.0
no sh
exit

int lo0
ip add 3.3.3.3 255.255.255.0
exit

router ospf 1
net 192.168.30.0 0.0.0.255 area 0
net 192.168.40.0 0.0.0.255 area 0

R4 Configuration

bash

en
conf t
int f0/0
ip add 192.168.40.20 255.255.255.0
no sh
exit

int f1/0
ip add 192.168.50.10 255.255.255.0
no sh
exit

int lo0
ip add 4.4.4.4 255.255.255.0
exit

router ospf 1
net 192.168.40.0 0.0.0.255 area 0
net 192.168.50.0 0.0.0.255 area 0

R5 Configuration

bash

en
conf t
int f0/0
ip add 192.168.50.20 255.255.255.0
no sh
exit

int f1/0
ip add 192.168.60.10 255.255.255.0
no sh
exit

int lo0
ip add 5.5.5.5 255.255.255.0
exit

router ospf 1
net 192.168.50.0 0.0.0.255 area 0
net 192.168.60.0 0.0.0.255 area 0

R6 Configuration

bash

en
conf t
int f0/0
ip add 192.168.60.20 255.255.255.0
no sh
exit

int f1/0
ip add 192.168.10.20 255.255.255.0
no sh
exit

int lo0
ip add 6.6.6.6 255.255.255.0 
exit

router ospf 1
net 192.168.60.0 0.0.0.255 area 0
net 192.168.10.0 0.0.0.255 area 0

PC Configurations
PC1 Configuration

ip 192.168.40.12 255.255.255.0 192.168.40.10

PC2 Configuration

ip 192.168.40.14 255.255.255.0 192.168.40.20

This README file provides the OSPF configuration for the network topology described, including configurations for routers (R1-R6) and PCs (PC1, PC2). Ensure that each device is configured accordingly to establish OSPF routing within the network.
