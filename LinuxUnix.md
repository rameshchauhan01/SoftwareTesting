|CMD Command			| UNIX Command	| PowerShell Command 	|	PowerShell Alias|
|---------------	|---------------|--------------------	|-----------------|
|dir					|  ls			| Get-ChildItem		 	|	gci|
|cls					|  clear		| Clear-Host(function)	|	cls|
|del, erase, rmdir	|	rm			| Remove-Item			|   ri|
|copy				|	cp			| Copy-Item				|   ci|
|move				|	mv			| Move-Item				|   mi|
|rename				|	mv			| Rename-Item			|   rni|
type				|	cat			| Get-Content			|   gc
cd					|	cd			| Set-Location			|   sl
md					|	mkdir		| New-Item				|   ni
pushd				|	pushd		| Push-Location			|  pushd
popd				|	popd		| Pop-Location			|  popd

# To configure static IP address in RHEL / CentOS / Fedora, you will need to edit:
## vi /etc/sysconfig/network
Open that file and set =>
NETWORKING=yes, HOSTNAME=node01.tecmint.com ,GATEWAY=192.168.0.1, NETWORKING_IPV6=no, IPV6INIT=no
Next open=>
#vi /etc/sysconfig/network-scripts/ifcfg-eth0
DEVICE="eth0", BOOTPROTO="static", DNS1="8.8.8.8", DNS2="4.4.4.4", GATEWAY="192.168.0.1", HOSTNAME="node01.tecmint.com", HWADDR="00:19:99:A4:46:AB"
IPADDR="192.68.0.100", NETMASK="255.255.255.0", NM_CONTROLLED="yes", ONBOOT="yes", TYPE="Ethernet", UUID="8105c095-799b-4f5a-a445-c6d7c3681f07"

# Next edit resolve.conf file by opening it with a text editor such as nano or vi:
## vi /etc/resolv.conf
