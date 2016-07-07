This script creates config file `dhcpd.conf` for dhcpd daemon using a template:  
		host host1 {
			hardware ethernet host1_MAC_address;
			fixed-address host1_ip_address;
			option host-name “CAN1”;
			option option-150 tftp_address;
			option BITI.transfer-mode “tftp”;
			option BITI.config-file-name “host1.confg”;
		}   
##### How it works
First step: it parses `Network Addresses.xlsx` file for getting lists of ips, hostnames and mac-addresses.  
(add your data into the appropriate columns)  
Second step: creates `dhcpd.conf` file with  necessary blocks.  

Here's a short video, how it works:  
https://youtu.be/FTJi1kBK_sU  

##### Usage
		python dhcpd.py  

##### Requirements
		(python 2.7)
		pip install lxml==3.6.0  
		pip install openpyxl==2.3.5  
