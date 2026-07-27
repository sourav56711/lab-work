ifconfig
enp2s0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.10.1.105  netmask 255.255.0.0  broadcast 10.10.255.255
        inet6 fe80::97a6:1457:7502:7f77  prefixlen 64  scopeid 0x20<link>
        ether 30:56:0f:55:64:7b  txqueuelen 1000  (Ethernet)
        RX packets 50083  bytes 50071355 (50.0 MB)
        RX errors 0  dropped 29  overruns 0  frame 0
        TX packets 27694  bytes 6921928 (6.9 MB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 3062  bytes 337900 (337.9 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 3062  bytes 337900 (337.9 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

mtech@programminlab-H610M-K-DDR4:~/Desktop$ ip -a
Usage: ip [ OPTIONS ] OBJECT { COMMAND | help }
       ip [ -force ] -batch filename
where  OBJECT := { address | addrlabel | fou | help | ila | ioam | l2tp | link |
                   macsec | maddress | monitor | mptcp | mroute | mrule |
                   neighbor | neighbour | netconf | netns | nexthop | ntable |
                   ntbl | route | rule | sr | tap | tcpmetrics |
                   token | tunnel | tuntap | vrf | xfrm }
       OPTIONS := { -V[ersion] | -s[tatistics] | -d[etails] | -r[esolve] |
                    -h[uman-readable] | -iec | -j[son] | -p[retty] |
                    -f[amily] { inet | inet6 | mpls | bridge | link } |
                    -4 | -6 | -M | -B | -0 |
                    -l[oops] { maximum-addr-flush-attempts } | -br[ief] |
                    -o[neline] | -t[imestamp] | -ts[hort] | -b[atch] [filename] |
                    -rc[vbuf] [size] | -n[etns] name | -N[umeric] | -a[ll] |
                    -c[olor]}
mtech@programminlab-H610M-K-DDR4:~/Desktop$ iftop
interface: enp2s0
IP address is: 10.10.1.105
MAC address is: 30:56:0f:55:64:7b
pcap_open_live(enp2s0): enp2s0: You don't have permission to capture on that device (socket: Operation not permitted)
mtech@programminlab-H610M-K-DDR4:~/Desktop$ sudo iftop -i enp2s0
interface: enp2s0
IP address is: 10.10.1.105
MAC address is: 30:56:0f:55:64:7b

[1]+  Stopped                 sudo iftop -i enp2s0
mtech@programminlab-H610M-K-DDR4:~/Desktop$ 

mtech@programminlab-H610M-K-DDR4:~/Desktop$ ping 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=117 time=17.6 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=4 ttl=117 time=17.6 ms
64 bytes from 8.8.8.8: icmp_seq=5 ttl=117 time=17.6 ms
64 bytes from 8.8.8.8: icmp_seq=6 ttl=117 time=17.6 ms
64 bytes from 8.8.8.8: icmp_seq=7 ttl=117 time=17.6 ms
64 bytes from 8.8.8.8: icmp_seq=8 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=9 ttl=117 time=17.7 ms
64 bytes from 8.8.8.8: icmp_seq=10 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=11 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=12 ttl=117 time=17.6 ms
64 bytes from 8.8.8.8: icmp_seq=13 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=14 ttl=117 time=17.4 ms
^X64 bytes from 8.8.8.8: icmp_seq=15 ttl=117 time=17.6 ms
64 bytes from 8.8.8.8: icmp_seq=16 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=17 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=18 ttl=117 time=17.6 ms
^C
--- 8.8.8.8 ping statistics ---
18 packets transmitted, 18 received, 0% packet loss, time 17027ms
rtt min/avg/max/mdev = 17.441/17.550/17.650/0.050 ms
mtech@programminlab-H610M-K-DDR4:~/Desktop$ ping -c 10 8.8.8.8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=117 time=17.6 ms
64 bytes from 8.8.8.8: icmp_seq=3 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=4 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=5 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=6 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=7 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=8 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=9 ttl=117 time=17.5 ms
64 bytes from 8.8.8.8: icmp_seq=10 ttl=117 time=17.6 ms

--- 8.8.8.8 ping statistics ---
10 packets transmitted, 10 received, 0% packet loss, time 9014ms
rtt min/avg/max/mdev = 17.481/17.527/17.579/0.029 ms
mtech@programminlab-H610M-K-DDR4:~/Desktop$ ip
Usage: ip [ OPTIONS ] OBJECT { COMMAND | help }
       ip [ -force ] -batch filename
where  OBJECT := { address | addrlabel | fou | help | ila | ioam | l2tp | link |
                   macsec | maddress | monitor | mptcp | mroute | mrule |
                   neighbor | neighbour | netconf | netns | nexthop | ntable |
                   ntbl | route | rule | sr | tap | tcpmetrics |
                   token | tunnel | tuntap | vrf | xfrm }
       OPTIONS := { -V[ersion] | -s[tatistics] | -d[etails] | -r[esolve] |
                    -h[uman-readable] | -iec | -j[son] | -p[retty] |
                    -f[amily] { inet | inet6 | mpls | bridge | link } |
                    -4 | -6 | -M | -B | -0 |
                    -l[oops] { maximum-addr-flush-attempts } | -br[ief] |
                    -o[neline] | -t[imestamp] | -ts[hort] | -b[atch] [filename] |
                    -rc[vbuf] [size] | -n[etns] name | -N[umeric] | -a[ll] |
                    -c[olor]}
mtech@programminlab-H610M-K-DDR4:~/Desktop$ ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host 
       valid_lft forever preferred_lft forever
2: enp2s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 30:56:0f:55:64:7b brd ff:ff:ff:ff:ff:ff
    inet 10.10.1.105/16 brd 10.10.255.255 scope global dynamic noprefixroute enp2s0
       valid_lft 40706sec preferred_lft 40706sec
    inet6 fe80::97a6:1457:7502:7f77/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever
mtech@programminlab-H610M-K-DDR4:~/Desktop$ ping -c 10 10.10.1.125
PING 10.10.1.125 (10.10.1.125) 56(84) bytes of data.
64 bytes from 10.10.1.125: icmp_seq=1 ttl=64 time=0.176 ms
64 bytes from 10.10.1.125: icmp_seq=2 ttl=64 time=0.246 ms
64 bytes from 10.10.1.125: icmp_seq=3 ttl=64 time=0.255 ms
64 bytes from 10.10.1.125: icmp_seq=4 ttl=64 time=0.251 ms
64 bytes from 10.10.1.125: icmp_seq=5 ttl=64 time=0.241 ms
64 bytes from 10.10.1.125: icmp_seq=6 ttl=64 time=0.234 ms
64 bytes from 10.10.1.125: icmp_seq=7 ttl=64 time=0.248 ms
64 bytes from 10.10.1.125: icmp_seq=8 ttl=64 time=0.188 ms
64 bytes from 10.10.1.125: icmp_seq=9 ttl=64 time=0.242 ms
64 bytes from 10.10.1.125: icmp_seq=10 ttl=64 time=0.179 ms

--- 10.10.1.125 ping statistics ---
10 packets transmitted, 10 received, 0% packet loss, time 9194ms
rtt min/avg/max/mdev = 0.176/0.226/0.255/0.030 ms
mtech@programminlab-H610M-K-DDR4:~/Desktop$ traceroute github.com
traceroute to github.com (20.207.73.82), 30 hops max, 60 byte packets
 1  _gateway (10.10.1.2)  0.993 ms  0.955 ms  0.938 ms
 2  * * *
 3  * * *
 4  * * *
 5  * * *
 6  * * *
 7  * * *
 8  * * *
 9  * * *
10  * * *
11  * * *
12  * * *
13  * * *
14  * * *
15  * * *
16  * * *
17  * * *
18  * * *
19  * * *
20  * * *
21  * * *
22  * * *
23  * * *
24  * * *
25  * * *
26  * * *
27  * * *
28  * * *
29  * * *
30  * * *
mtech@programminlab-H610M-K-DDR4:~/Desktop$ netstat
Active Internet connections (w/o servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
tcp        0      0 programminlab-H61:44380 nrt20s01-in-f130.:https TIME_WAIT  
tcp        0      0 programminlab-H61:54872 lb-140-82-114-26-:https ESTABLISHED
tcp        0      0 programminlab-H61:44412 nrt20s01-in-f130.:https TIME_WAIT  
tcp        0      0 programminlab-H61:36200 pt-in-f97.1e100.n:https TIME_WAIT  
tcp        0      0 programminlab-H61:36168 pt-in-f97.1e100.n:https TIME_WAIT  
tcp        0      0 programminlab-H61:59818 216.239.32.181:https    TIME_WAIT  
tcp        0      0 programminlab-H61:58656 pt-in-f101.1e100.:https ESTABLISHED
tcp        0      0 programminlab-H61:46382 142.251.156.119:https   TIME_WAIT  
tcp        0      0 programminlab-H61:46380 142.251.156.119:https   TIME_WAIT  
tcp        0      0 programminlab-H61:49232 pnmaaa-aq-in-f10.:https TIME_WAIT  
tcp        0      0 programminlab-H61:36462 93.243.107.34.bc.:https ESTABLISHED
tcp        0      0 programminlab-H61:58296 lcbome-in-f95.1e1:https ESTABLISHED
tcp        0      0 programminlab-H61:35410 cn-in-f139.1e100.:https TIME_WAIT  
tcp        0      0 programminlab-H61:49220 pnmaaa-aq-in-f10.:https TIME_WAIT  
tcp        0      0 programminlab-H61:59140 lcmaaa-az-in-f5.1:https ESTABLISHED
tcp        0      0 programminlab-H61:59826 216.239.32.181:https    TIME_WAIT  
tcp        0      0 programminlab-H61:56564 142.251.153.2:https     TIME_WAIT  
tcp        0      0 programminlab-H61:38576 lga34s40-in-f3.1e:https TIME_WAIT  
tcp        0      0 programminlab-H61:35404 cn-in-f139.1e100.:https TIME_WAIT  
tcp        0      0 programminlab-H61:37646 142.251.157.2:https     TIME_WAIT  
udp        0      0 programminlab-H6:bootpc _gateway:bootps         ESTABLISHED
Active UNIX domain sockets (w/o servers)
Proto RefCnt Flags       Type       State         I-Node   Path
unix  3      [ ]         STREAM     CONNECTED     45693    
unix  3      [ ]         STREAM     CONNECTED     45646    
unix  3      [ ]         SEQPACKET  CONNECTED     70044    
unix  3      [ ]         STREAM     CONNECTED     48442    
unix  3      [ ]         STREAM     CONNECTED     40744    
unix  3      [ ]         STREAM     CONNECTED     8644     
unix  3      [ ]         STREAM     CONNECTED     46175    
unix  3      [ ]         STREAM     CONNECTED     38713    
unix  3      [ ]         STREAM     CONNECTED     9184     /run/dbus/system_bus_socket
unix  3      [ ]         DGRAM      CONNECTED     4826     
unix  3      [ ]         DGRAM      CONNECTED     4824     /run/systemd/notify
unix  3      [ ]         STREAM     CONNECTED     45718    
unix  3      [ ]         STREAM     CONNECTED     45717    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     47307    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45639    
unix  3      [ ]         STREAM     CONNECTED     61024    
unix  3      [ ]         STREAM     CONNECTED     7709     
unix  3      [ ]         SEQPACKET  CONNECTED     66659    
unix  3      [ ]         STREAM     CONNECTED     38749    
unix  3      [ ]         SEQPACKET  CONNECTED     69921    
unix  3      [ ]         STREAM     CONNECTED     51997    
unix  3      [ ]         STREAM     CONNECTED     44710    
unix  3      [ ]         STREAM     CONNECTED     43784    
unix  3      [ ]         STREAM     CONNECTED     10579    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     45714    
unix  3      [ ]         STREAM     CONNECTED     7729     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     10379    /run/systemd/journal/stdout
unix  3      [ ]         SEQPACKET  CONNECTED     70102    
unix  3      [ ]         STREAM     CONNECTED     41912    
unix  3      [ ]         STREAM     CONNECTED     40714    
unix  3      [ ]         STREAM     CONNECTED     7715     
unix  3      [ ]         STREAM     CONNECTED     38725    
unix  3      [ ]         STREAM     CONNECTED     6859     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     9753     
unix  2      [ ]         DGRAM                    4838     /run/systemd/journal/syslog
unix  3      [ ]         STREAM     CONNECTED     44510    
unix  3      [ ]         STREAM     CONNECTED     9894     
unix  3      [ ]         STREAM     CONNECTED     45676    
unix  3      [ ]         STREAM     CONNECTED     45647    
unix  3      [ ]         SEQPACKET  CONNECTED     70178    
unix  3      [ ]         STREAM     CONNECTED     40743    
unix  3      [ ]         STREAM     CONNECTED     7644     
unix  20     [ ]         DGRAM      CONNECTED     4847     /run/systemd/journal/dev-log
unix  2      [ ]         DGRAM                    48439    
unix  3      [ ]         STREAM     CONNECTED     8017     /run/dbus/system_bus_socket
unix  2      [ ]         DGRAM                    11379    
unix  9      [ ]         DGRAM      CONNECTED     4849     /run/systemd/journal/socket
unix  3      [ ]         STREAM     CONNECTED     38719    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     12347    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     3697     
unix  3      [ ]         STREAM     CONNECTED     51155    
unix  3      [ ]         STREAM     CONNECTED     43376    /run/user/1003/pipewire-0
unix  2      [ ]         DGRAM      CONNECTED     3456     
unix  3      [ ]         STREAM     CONNECTED     61025    
unix  3      [ ]         SEQPACKET  CONNECTED     70112    
unix  3      [ ]         SEQPACKET  CONNECTED     54635    
unix  3      [ ]         STREAM     CONNECTED     41929    
unix  3      [ ]         STREAM     CONNECTED     47316    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     40762    
unix  3      [ ]         STREAM     CONNECTED     11384    
unix  3      [ ]         DGRAM      CONNECTED     7783     
unix  3      [ ]         STREAM     CONNECTED     47231    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44305    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     40444    
unix  3      [ ]         STREAM     CONNECTED     10125    
unix  3      [ ]         STREAM     CONNECTED     45715    
unix  3      [ ]         STREAM     CONNECTED     41944    
unix  3      [ ]         STREAM     CONNECTED     40735    
unix  3      [ ]         SEQPACKET  CONNECTED     50071    
unix  3      [ ]         STREAM     CONNECTED     39801    
unix  3      [ ]         STREAM     CONNECTED     6793     
unix  3      [ ]         STREAM     CONNECTED     9888     /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     46179    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     39883    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     42688    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     47235    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     41923    
unix  3      [ ]         STREAM     CONNECTED     45666    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     46202    /run/user/1003/bus
unix  3      [ ]         DGRAM      CONNECTED     39841    
unix  3      [ ]         STREAM     CONNECTED     8654     
unix  3      [ ]         STREAM     CONNECTED     6589     
unix  3      [ ]         STREAM     CONNECTED     44304    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     9875     
unix  3      [ ]         STREAM     CONNECTED     55468    
unix  3      [ ]         SEQPACKET  CONNECTED     70177    
unix  3      [ ]         STREAM     CONNECTED     61049    
unix  3      [ ]         STREAM     CONNECTED     41900    
unix  3      [ ]         STREAM     CONNECTED     40763    
unix  3      [ ]         STREAM     CONNECTED     40429    
unix  3      [ ]         STREAM     CONNECTED     11348    
unix  3      [ ]         STREAM     CONNECTED     38764    
unix  3      [ ]         STREAM     CONNECTED     44217    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     6651     
unix  3      [ ]         STREAM     CONNECTED     7725     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     7720     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     43791    
unix  3      [ ]         STREAM     CONNECTED     8021     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     47347    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     3720     /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     70116    
unix  3      [ ]         SEQPACKET  CONNECTED     54634    
unix  3      [ ]         STREAM     CONNECTED     45677    @/home/mtech/.cache/ibus/dbus-dKRWYnve
unix  3      [ ]         STREAM     CONNECTED     40752    
unix  3      [ ]         STREAM     CONNECTED     43940    /run/snapd-snap.socket
unix  3      [ ]         STREAM     CONNECTED     46172    
unix  3      [ ]         STREAM     CONNECTED     11460    
unix  3      [ ]         STREAM     CONNECTED     57894    
unix  3      [ ]         SEQPACKET  CONNECTED     64824    
unix  3      [ ]         SEQPACKET  CONNECTED     49556    
unix  3      [ ]         STREAM     CONNECTED     43943    
unix  3      [ ]         STREAM     CONNECTED     7722     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     55467    
unix  3      [ ]         STREAM     CONNECTED     50736    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     47297    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45631    
unix  3      [ ]         STREAM     CONNECTED     39891    /run/dbus/system_bus_socket
unix  2      [ ]         DGRAM      CONNECTED     9913     
unix  3      [ ]         STREAM     CONNECTED     7628     
unix  3      [ ]         STREAM     CONNECTED     42745    /run/user/1003/wayland-0
unix  2      [ ]         DGRAM      CONNECTED     11409    
unix  3      [ ]         STREAM     CONNECTED     9523     
unix  3      [ ]         STREAM     CONNECTED     45203    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     45684    
unix  3      [ ]         STREAM     CONNECTED     40736    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     11365    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     48443    
unix  3      [ ]         STREAM     CONNECTED     56512    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     50099    
unix  3      [ ]         STREAM     CONNECTED     46287    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     46155    
unix  3      [ ]         STREAM     CONNECTED     38690    
unix  3      [ ]         STREAM     CONNECTED     9890     /run/systemd/journal/stdout
unix  2      [ ]         DGRAM      CONNECTED     8643     
unix  3      [ ]         STREAM     CONNECTED     9924     
unix  2      [ ]         DGRAM                    43773    
unix  3      [ ]         STREAM     CONNECTED     45643    
unix  3      [ ]         STREAM     CONNECTED     44430    /run/systemd/journal/stdout
unix  2      [ ]         DGRAM                    39839    /run/user/1003/systemd/notify
unix  3      [ ]         STREAM     CONNECTED     60481    
unix  3      [ ]         STREAM     CONNECTED     40430    
unix  3      [ ]         STREAM     CONNECTED     39844    
unix  3      [ ]         STREAM     CONNECTED     38607    
unix  2      [ ]         DGRAM      CONNECTED     4895     
unix  3      [ ]         STREAM     CONNECTED     42781    
unix  3      [ ]         STREAM     CONNECTED     44511    
unix  3      [ ]         STREAM     CONNECTED     7717     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     45635    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     61027    
unix  3      [ ]         SEQPACKET  CONNECTED     70045    
unix  3      [ ]         STREAM     CONNECTED     44464    /run/systemd/journal/stdout
unix  3      [ ]         SEQPACKET  CONNECTED     66926    
unix  3      [ ]         STREAM     CONNECTED     48405    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     40853    /run/user/1003/bus
unix  3      [ ]         DGRAM      CONNECTED     7782     
unix  2      [ ]         DGRAM                    11401    
unix  3      [ ]         STREAM     CONNECTED     6620     
unix  3      [ ]         STREAM     CONNECTED     43922    
unix  3      [ ]         STREAM     CONNECTED     39902    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     3686     
unix  3      [ ]         STREAM     CONNECTED     43786    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     54639    
unix  3      [ ]         STREAM     CONNECTED     41933    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     40780    
unix  3      [ ]         SEQPACKET  CONNECTED     66927    
unix  3      [ ]         STREAM     CONNECTED     53860    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     1892     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     6702     
unix  3      [ ]         DGRAM      CONNECTED     4825     
unix  3      [ ]         STREAM     CONNECTED     44512    
unix  3      [ ]         STREAM     CONNECTED     11696    
unix  3      [ ]         STREAM     CONNECTED     51156    
unix  3      [ ]         STREAM     CONNECTED     7727     /run/dbus/system_bus_socket
unix  3      [ ]         DGRAM      CONNECTED     3461     
unix  3      [ ]         STREAM     CONNECTED     54638    
unix  3      [ ]         STREAM     CONNECTED     41898    
unix  3      [ ]         STREAM     CONNECTED     45649    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     40781    
unix  3      [ ]         STREAM     CONNECTED     40428    
unix  2      [ ]         DGRAM      CONNECTED     9747     
unix  3      [ ]         STREAM     CONNECTED     42735    /run/user/1003/bus
unix  3      [ ]         SEQPACKET  CONNECTED     64823    
unix  3      [ ]         STREAM     CONNECTED     51996    
unix  3      [ ]         STREAM     CONNECTED     38714    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45640    
unix  3      [ ]         STREAM     CONNECTED     10380    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     50106    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45664    
unix  3      [ ]         DGRAM      CONNECTED     9842     
unix  3      [ ]         STREAM     CONNECTED     45780    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     11461    
unix  2      [ ]         DGRAM      CONNECTED     7713     
unix  3      [ ]         STREAM     CONNECTED     9895     /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44708    
unix  3      [ ]         STREAM     CONNECTED     45765    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     44427    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     42728    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     45634    /run/systemd/journal/stdout
unix  3      [ ]         SEQPACKET  CONNECTED     66660    
unix  3      [ ]         STREAM     CONNECTED     47359    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     38717    
unix  3      [ ]         STREAM     CONNECTED     8019     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     8663     /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     9858     
unix  3      [ ]         STREAM     CONNECTED     41930    /run/user/1003/pulse/native
unix  3      [ ]         STREAM     CONNECTED     45681    
unix  3      [ ]         STREAM     CONNECTED     45630    
unix  3      [ ]         STREAM     CONNECTED     42342    /run/systemd/journal/stdout
unix  3      [ ]         DGRAM      CONNECTED     3460     
unix  3      [ ]         STREAM     CONNECTED     40713    
unix  3      [ ]         STREAM     CONNECTED     7649     
unix  3      [ ]         STREAM     CONNECTED     48979    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     46178    
unix  3      [ ]         SEQPACKET  CONNECTED     57907    
unix  3      [ ]         STREAM     CONNECTED     44250    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     11622    
unix  3      [ ]         STREAM     CONNECTED     49138    /run/user/1003/pulse/native
unix  3      [ ]         STREAM     CONNECTED     55466    
unix  3      [ ]         STREAM     CONNECTED     41913    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     7728     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     43712    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     40385    
unix  3      [ ]         STREAM     CONNECTED     38748    
unix  3      [ ]         SEQPACKET  CONNECTED     50049    
unix  3      [ ]         STREAM     CONNECTED     3696     
unix  3      [ ]         STREAM     CONNECTED     9524     /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     55481    
unix  3      [ ]         STREAM     CONNECTED     47325    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45648    
unix  3      [ ]         STREAM     CONNECTED     41873    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     10381    /run/systemd/journal/stdout
unix  3      [ ]         DGRAM      CONNECTED     9841     
unix  3      [ ]         STREAM     CONNECTED     45769    /run/snapd-snap.socket
unix  3      [ ]         STREAM     CONNECTED     38763    
unix  3      [ ]         STREAM     CONNECTED     54768    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     51998    
unix  3      [ ]         STREAM     CONNECTED     55479    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     9900     
unix  3      [ ]         STREAM     CONNECTED     55469    
unix  3      [ ]         STREAM     CONNECTED     52290    /run/user/1003/snap.firefox/wayland-proxy-7557
unix  2      [ ]         DGRAM                    44548    
unix  3      [ ]         STREAM     CONNECTED     10369    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     70117    
unix  3      [ ]         STREAM     CONNECTED     46242    
unix  3      [ ]         STREAM     CONNECTED     40782    
unix  3      [ ]         STREAM     CONNECTED     41887    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     8683     
unix  3      [ ]         STREAM     CONNECTED     66577    
unix  3      [ ]         STREAM     CONNECTED     44713    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     46181    
unix  3      [ ]         SEQPACKET  CONNECTED     49558    
unix  3      [ ]         STREAM     CONNECTED     46176    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     10127    
unix  3      [ ]         STREAM     CONNECTED     11411    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     41922    
unix  3      [ ]         STREAM     CONNECTED     40756    
unix  2      [ ]         DGRAM      CONNECTED     39929    
unix  3      [ ]         STREAM     CONNECTED     40391    
unix  3      [ ]         STREAM     CONNECTED     9199     
unix  3      [ ]         STREAM     CONNECTED     38684    
unix  3      [ ]         SEQPACKET  CONNECTED     50054    
unix  3      [ ]         STREAM     CONNECTED     44943    
unix  3      [ ]         STREAM     CONNECTED     44705    
unix  3      [ ]         STREAM     CONNECTED     45721    /run/user/1003/pipewire-0
unix  3      [ ]         STREAM     CONNECTED     42726    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     45653    
unix  3      [ ]         STREAM     CONNECTED     44426    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     47337    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45675    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     46169    
unix  3      [ ]         STREAM     CONNECTED     6588     
unix  2      [ ]         DGRAM      CONNECTED     7531     
unix  3      [ ]         STREAM     CONNECTED     6051     /run/systemd/journal/stdout
unix  3      [ ]         SEQPACKET  CONNECTED     50053    
unix  3      [ ]         STREAM     CONNECTED     45695    
unix  3      [ ]         STREAM     CONNECTED     40783    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     43375    /run/user/1003/pipewire-0
unix  3      [ ]         STREAM     CONNECTED     48136    
unix  3      [ ]         STREAM     CONNECTED     46191    @/tmp/.ICE-unix/6801
unix  3      [ ]         STREAM     CONNECTED     50098    
unix  3      [ ]         STREAM     CONNECTED     43938    /run/snapd-snap.socket
unix  3      [ ]         STREAM     CONNECTED     47193    
unix  3      [ ]         SEQPACKET  CONNECTED     54599    
unix  3      [ ]         STREAM     CONNECTED     7719     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     45636    
unix  3      [ ]         STREAM     CONNECTED     10117    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     7652     /run/systemd/journal/stdout
unix  2      [ ]         DGRAM      CONNECTED     3307     
unix  3      [ ]         STREAM     CONNECTED     45682    /run/user/1003/gvfsd/socket-eQyGQukG
unix  3      [ ]         STREAM     CONNECTED     40715    
unix  2      [ ]         DGRAM      CONNECTED     39811    
unix  3      [ ]         STREAM     CONNECTED     56513    /run/systemd/journal/stdout
unix  2      [ ]         DGRAM                    41936    
unix  3      [ ]         STREAM     CONNECTED     38628    
unix  3      [ ]         STREAM     CONNECTED     10195    
unix  3      [ ]         STREAM     CONNECTED     55477    
unix  2      [ ]         STREAM     CONNECTED     45660    
unix  3      [ ]         STREAM     CONNECTED     7721     /run/dbus/system_bus_socket
unix  3      [ ]         SEQPACKET  CONNECTED     70111    
unix  3      [ ]         STREAM     CONNECTED     41899    
unix  3      [ ]         STREAM     CONNECTED     40716    
unix  3      [ ]         STREAM     CONNECTED     11402    
unix  3      [ ]         STREAM     CONNECTED     12457    
unix  3      [ ]         STREAM     CONNECTED     7724     /run/dbus/system_bus_socket
unix  3      [ ]         SEQPACKET  CONNECTED     49557    
unix  3      [ ]         STREAM     CONNECTED     40525    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     40445    
unix  2      [ ]         STREAM     CONNECTED     11686    
unix  3      [ ]         STREAM     CONNECTED     1824     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     47308    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     61048    
unix  3      [ ]         STREAM     CONNECTED     41945    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     39897    
unix  2      [ ]         DGRAM      CONNECTED     39821    
unix  3      [ ]         STREAM     CONNECTED     46239    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     43663    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     11691    
unix  3      [ ]         STREAM     CONNECTED     10128    
unix  3      [ ]         STREAM     CONNECTED     9982     /run/systemd/journal/stdout
unix  2      [ ]         DGRAM                    44706    
unix  3      [ ]         STREAM     CONNECTED     40833    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     45665    
unix  3      [ ]         STREAM     CONNECTED     41872    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44219    /run/user/1003/bus
unix  2      [ ]         DGRAM      CONNECTED     18618    
unix  2      [ ]         DGRAM      CONNECTED     9873     
unix  3      [ ]         STREAM     CONNECTED     8638     
unix  3      [ ]         STREAM     CONNECTED     47194    
unix  3      [ ]         STREAM     CONNECTED     57893    
unix  3      [ ]         STREAM     CONNECTED     43792    
unix  3      [ ]         STREAM     CONNECTED     37838    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     3675     /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     40807    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     61026    
unix  3      [ ]         STREAM     CONNECTED     41932    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     40766    
unix  3      [ ]         STREAM     CONNECTED     46186    
unix  3      [ ]         DGRAM      CONNECTED     39840    
unix  3      [ ]         SEQPACKET  CONNECTED     57906    
unix  3      [ ]         STREAM     CONNECTED     40689    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     3703     
unix  3      [ ]         STREAM     CONNECTED     5104     /run/systemd/io.system.ManagedOOM
unix  3      [ ]         STREAM     CONNECTED     44197    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     9893     /run/systemd/journal/stdout
unix  3      [ ]         SEQPACKET  CONNECTED     70101    
unix  3      [ ]         STREAM     CONNECTED     46240    
unix  3      [ ]         STREAM     CONNECTED     45694    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     45650    /run/systemd/journal/stdout
unix  3      [ ]         SEQPACKET  CONNECTED     50070    
unix  2      [ ]         DGRAM                    48142    
unix  3      [ ]         STREAM     CONNECTED     41949    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     38638    
unix  3      [ ]         SEQPACKET  CONNECTED     69922    
unix  3      [ ]         SEQPACKET  CONNECTED     54598    
unix  3      [ ]         STREAM     CONNECTED     55480    /run/systemd/journal/stdout
unix  3      [ ]         SEQPACKET  CONNECTED     49559    
unix  3      [ ]         STREAM     CONNECTED     47233    /run/systemd/journal/stdout
unix  2      [ ]         STREAM     CONNECTED     11695    
unix  3      [ ]         STREAM     CONNECTED     55478    
unix  3      [ ]         STREAM     CONNECTED     41950    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     42718    @/home/mtech/.cache/ibus/dbus-dKRWYnve
unix  3      [ ]         STREAM     CONNECTED     41885    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     47310    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     8675     
unix  3      [ ]         STREAM     CONNECTED     52000    
unix  3      [ ]         STREAM     CONNECTED     40436    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     10065    
unix  3      [ ]         STREAM     CONNECTED     3704     
unix  3      [ ]         STREAM     CONNECTED     45580    /run/user/1003/bus
unix  2      [ ]         DGRAM      CONNECTED     9953     
unix  3      [ ]         STREAM     CONNECTED     41924    
unix  3      [ ]         STREAM     CONNECTED     47352    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     7714     
unix  3      [ ]         STREAM     CONNECTED     66576    
unix  3      [ ]         STREAM     CONNECTED     42742    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     6687     
unix  3      [ ]         SEQPACKET  CONNECTED     50050    
unix  3      [ ]         STREAM     CONNECTED     47200    /run/user/1003/pulse/native
unix  3      [ ]         STREAM     CONNECTED     3447     
unix  3      [ ]         SEQPACKET  CONNECTED     52349    
unix  3      [ ]         STREAM     CONNECTED     52344    
unix  2      [ ]         DGRAM                    47336    
unix  3      [ ]         STREAM     CONNECTED     40799    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     43732    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     41682    
unix  3      [ ]         STREAM     CONNECTED     42780    
unix  3      [ ]         STREAM     CONNECTED     41935    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     55551    
unix  3      [ ]         STREAM     CONNECTED     43736    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     3552     /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     46168    /run/dbus/system_bus_socket
unix  2      [ ]         DGRAM      CONNECTED     6806     
unix  3      [ ]         STREAM     CONNECTED     57643    
unix  3      [ ]         SEQPACKET  CONNECTED     48581    
unix  3      [ ]         STREAM     CONNECTED     46222    
unix  3      [ ]         STREAM     CONNECTED     10397    
unix  3      [ ]         STREAM     CONNECTED     44662    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     42724    
unix  3      [ ]         STREAM     CONNECTED     47289    
unix  3      [ ]         STREAM     CONNECTED     39889    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     43766    
unix  3      [ ]         STREAM     CONNECTED     44450    
unix  3      [ ]         STREAM     CONNECTED     44431    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     42617    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     46198    
unix  3      [ ]         STREAM     CONNECTED     40761    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     10460    
unix  3      [ ]         STREAM     CONNECTED     42753    
unix  3      [ ]         STREAM     CONNECTED     47207    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     42227    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     10673    /run/dbus/system_bus_socket
unix  3      [ ]         SEQPACKET  CONNECTED     52368    
unix  3      [ ]         STREAM     CONNECTED     45591    
unix  3      [ ]         STREAM     CONNECTED     44439    
unix  3      [ ]         STREAM     CONNECTED     47232    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     1966     
unix  3      [ ]         STREAM     CONNECTED     47361    
unix  3      [ ]         STREAM     CONNECTED     46221    
unix  3      [ ]         STREAM     CONNECTED     47353    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     47335    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     10468    
unix  3      [ ]         STREAM     CONNECTED     44714    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     43925    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     42341    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44473    
unix  3      [ ]         STREAM     CONNECTED     46203    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     38726    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     40836    
unix  3      [ ]         STREAM     CONNECTED     46220    
unix  3      [ ]         STREAM     CONNECTED     41917    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     44331    
unix  3      [ ]         STREAM     CONNECTED     42747    
unix  3      [ ]         STREAM     CONNECTED     43385    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44216    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     38815    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45115    
unix  3      [ ]         STREAM     CONNECTED     40723    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     44440    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     57763    
unix  3      [ ]         STREAM     CONNECTED     46297    
unix  3      [ ]         STREAM     CONNECTED     44711    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     42746    
unix  3      [ ]         STREAM     CONNECTED     47222    
unix  3      [ ]         STREAM     CONNECTED     8558     /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     45596    
unix  3      [ ]         STREAM     CONNECTED     43407    
unix  3      [ ]         STREAM     CONNECTED     47349    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     47807    
unix  3      [ ]         STREAM     CONNECTED     40854    
unix  2      [ ]         DGRAM      CONNECTED     1765     
unix  3      [ ]         STREAM     CONNECTED     40749    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     47287    
unix  3      [ ]         STREAM     CONNECTED     42394    
unix  3      [ ]         STREAM     CONNECTED     39748    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     55550    
unix  3      [ ]         STREAM     CONNECTED     52364    
unix  3      [ ]         STREAM     CONNECTED     52291    
unix  3      [ ]         STREAM     CONNECTED     41862    
unix  3      [ ]         STREAM     CONNECTED     1819     
unix  3      [ ]         STREAM     CONNECTED     40800    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     41681    
unix  3      [ ]         SEQPACKET  CONNECTED     70678    
unix  3      [ ]         STREAM     CONNECTED     42779    
unix  3      [ ]         STREAM     CONNECTED     40795    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     47317    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     44335    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44443    
unix  3      [ ]         STREAM     CONNECTED     7934     
unix  2      [ ]         DGRAM      CONNECTED     10292    
unix  3      [ ]         STREAM     CONNECTED     43230    
unix  2      [ ]         DGRAM      CONNECTED     1702     
unix  3      [ ]         STREAM     CONNECTED     46269    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     46217    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     42704    
unix  3      [ ]         STREAM     CONNECTED     47294    
unix  3      [ ]         STREAM     CONNECTED     47288    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     52363    
unix  3      [ ]         STREAM     CONNECTED     45588    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     43664    
unix  3      [ ]         STREAM     CONNECTED     67896    
unix  3      [ ]         STREAM     CONNECTED     46180    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     46283    
unix  3      [ ]         STREAM     CONNECTED     46205    
unix  3      [ ]         STREAM     CONNECTED     43387    
unix  3      [ ]         STREAM     CONNECTED     65742    
unix  3      [ ]         STREAM     CONNECTED     40806    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     47329    
unix  3      [ ]         STREAM     CONNECTED     45143    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     42397    
unix  3      [ ]         STREAM     CONNECTED     6684     /run/dbus/system_bus_socket
unix  3      [ ]         SEQPACKET  CONNECTED     52356    
unix  3      [ ]         STREAM     CONNECTED     42623    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     43668    
unix  3      [ ]         STREAM     CONNECTED     1578     
unix  3      [ ]         STREAM     CONNECTED     57644    
unix  3      [ ]         STREAM     CONNECTED     40857    
unix  3      [ ]         STREAM     CONNECTED     45688    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     46209    
unix  3      [ ]         STREAM     CONNECTED     10343    
unix  3      [ ]         SEQPACKET  CONNECTED     70677    
unix  3      [ ]         STREAM     CONNECTED     65633    
unix  3      [ ]         STREAM     CONNECTED     47293    
unix  2      [ ]         DGRAM      CONNECTED     7937     
unix  3      [ ]         SEQPACKET  CONNECTED     52355    
unix  3      [ ]         STREAM     CONNECTED     43765    
unix  3      [ ]         STREAM     CONNECTED     44476    
unix  3      [ ]         STREAM     CONNECTED     6803     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     46284    
unix  3      [ ]         STREAM     CONNECTED     41919    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     40759    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     43926    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45692    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     9892     /run/systemd/journal/stdout
unix  3      [ ]         SEQPACKET  CONNECTED     52367    
unix  3      [ ]         STREAM     CONNECTED     44494    
unix  3      [ ]         STREAM     CONNECTED     6610     /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     41888    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     43489    /run/dbus/system_bus_socket
unix  3      [ ]         SEQPACKET  CONNECTED     48496    
unix  3      [ ]         STREAM     CONNECTED     46223    
unix  3      [ ]         STREAM     CONNECTED     44214    
unix  3      [ ]         STREAM     CONNECTED     8001     
unix  3      [ ]         STREAM     CONNECTED     42740    
unix  3      [ ]         STREAM     CONNECTED     47330    
unix  3      [ ]         STREAM     CONNECTED     40796    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44222    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     44507    
unix  3      [ ]         STREAM     CONNECTED     43723    /run/systemd/journal/stdout
unix  3      [ ]         DGRAM      CONNECTED     10296    
unix  3      [ ]         STREAM     CONNECTED     57498    
unix  3      [ ]         STREAM     CONNECTED     40852    
unix  3      [ ]         STREAM     CONNECTED     46282    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     65634    
unix  3      [ ]         STREAM     CONNECTED     47350    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     47290    
unix  3      [ ]         STREAM     CONNECTED     58855    
unix  3      [ ]         SEQPACKET  CONNECTED     52348    
unix  3      [ ]         STREAM     CONNECTED     52345    
unix  3      [ ]         STREAM     CONNECTED     10593    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     45590    /run/user/1003/bus
unix  2      [ ]         DGRAM      CONNECTED     44213    
unix  3      [ ]         STREAM     CONNECTED     10637    
unix  3      [ ]         STREAM     CONNECTED     46225    
unix  3      [ ]         STREAM     CONNECTED     44715    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     42226    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     7726     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     44493    
unix  3      [ ]         STREAM     CONNECTED     43680    
unix  3      [ ]         STREAM     CONNECTED     41876    
unix  3      [ ]         STREAM     CONNECTED     45686    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     40832    
unix  3      [ ]         STREAM     CONNECTED     41680    
unix  3      [ ]         STREAM     CONNECTED     41914    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     47223    
unix  3      [ ]         STREAM     CONNECTED     44310    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     39893    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     58854    
unix  3      [ ]         STREAM     CONNECTED     43683    
unix  3      [ ]         STREAM     CONNECTED     44446    
unix  3      [ ]         SEQPACKET  CONNECTED     53691    
unix  3      [ ]         STREAM     CONNECTED     49824    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     1751     
unix  3      [ ]         DGRAM      CONNECTED     10297    
unix  3      [ ]         STREAM     CONNECTED     46237    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45585    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     6899     
unix  3      [ ]         STREAM     CONNECTED     46201    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     39909    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     43478    
unix  3      [ ]         STREAM     CONNECTED     44437    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     6807     /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     57764    
unix  3      [ ]         STREAM     CONNECTED     43762    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44262    
unix  3      [ ]         STREAM     CONNECTED     43288    
unix  3      [ ]         STREAM     CONNECTED     70694    
unix  3      [ ]         STREAM     CONNECTED     43942    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     47334    
unix  3      [ ]         STREAM     CONNECTED     40747    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45118    
unix  3      [ ]         STREAM     CONNECTED     41916    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     44463    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     40805    
unix  3      [ ]         STREAM     CONNECTED     47296    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45586    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     43380    
unix  3      [ ]         STREAM     CONNECTED     70695    
unix  3      [ ]         STREAM     CONNECTED     45748    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     42734    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     13364    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     52343    
unix  3      [ ]         STREAM     CONNECTED     44498    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     47309    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     43669    
unix  3      [ ]         STREAM     CONNECTED     40512    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     1696     
unix  3      [ ]         STREAM     CONNECTED     57497    
unix  3      [ ]         STREAM     CONNECTED     40859    
unix  3      [ ]         STREAM     CONNECTED     41918    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     46200    
unix  3      [ ]         STREAM     CONNECTED     43715    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     43228    
unix  3      [ ]         STREAM     CONNECTED     7718     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     44497    
unix  3      [ ]         STREAM     CONNECTED     43728    
unix  3      [ ]         STREAM     CONNECTED     40793    
unix  2      [ ]         DGRAM      CONNECTED     41724    
unix  3      [ ]         STREAM     CONNECTED     44220    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     43291    
unix  3      [ ]         SEQPACKET  CONNECTED     48762    
unix  3      [ ]         STREAM     CONNECTED     47345    
unix  3      [ ]         STREAM     CONNECTED     45678    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     45183    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     43384    /run/systemd/journal/stdout
unix  3      [ ]         SEQPACKET  CONNECTED     53690    
unix  3      [ ]         STREAM     CONNECTED     53689    
unix  3      [ ]         STREAM     CONNECTED     40778    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44449    /run/user/1003/bus
unix  3      [ ]         DGRAM      CONNECTED     10299    
unix  3      [ ]         STREAM     CONNECTED     42739    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44259    
unix  3      [ ]         SEQPACKET  CONNECTED     48763    
unix  3      [ ]         STREAM     CONNECTED     46224    @/home/mtech/.cache/ibus/dbus-dKRWYnve
unix  3      [ ]         STREAM     CONNECTED     42723    
unix  3      [ ]         STREAM     CONNECTED     40812    @/home/mtech/.cache/ibus/dbus-dKRWYnve
unix  3      [ ]         STREAM     CONNECTED     43676    
unix  3      [ ]         STREAM     CONNECTED     53861    
unix  3      [ ]         STREAM     CONNECTED     40948    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     45600    
unix  3      [ ]         SEQPACKET  CONNECTED     57771    
unix  3      [ ]         STREAM     CONNECTED     47318    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     43369    
unix  3      [ ]         STREAM     CONNECTED     47354    
unix  3      [ ]         STREAM     CONNECTED     45685    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     45691    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     47234    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     40738    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     1974     
unix  2      [ ]         DGRAM                    41776    
unix  3      [ ]         STREAM     CONNECTED     43229    
unix  3      [ ]         STREAM     CONNECTED     48978    
unix  3      [ ]         STREAM     CONNECTED     47346    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     42720    
unix  3      [ ]         STREAM     CONNECTED     47331    
unix  3      [ ]         STREAM     CONNECTED     43759    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     39919    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     43745    
unix  3      [ ]         STREAM     CONNECTED     46184    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     44442    
unix  3      [ ]         STREAM     CONNECTED     44218    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     46228    
unix  3      [ ]         STREAM     CONNECTED     42705    
unix  3      [ ]         STREAM     CONNECTED     47286    
unix  3      [ ]         STREAM     CONNECTED     53688    
unix  3      [ ]         STREAM     CONNECTED     45687    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     41879    
unix  2      [ ]         DGRAM      CONNECTED     43251    
unix  3      [ ]         SEQPACKET  CONNECTED     57772    
unix  3      [ ]         STREAM     CONNECTED     47808    
unix  3      [ ]         SEQPACKET  CONNECTED     48495    
unix  3      [ ]         STREAM     CONNECTED     46235    
unix  3      [ ]         STREAM     CONNECTED     47351    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     40794    
unix  3      [ ]         STREAM     CONNECTED     44433    
unix  3      [ ]         STREAM     CONNECTED     10276    
unix  3      [ ]         STREAM     CONNECTED     42725    
unix  3      [ ]         STREAM     CONNECTED     40750    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     7716     /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     43761    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44201    /run/dbus/system_bus_socket
unix  2      [ ]         DGRAM      CONNECTED     10429    
unix  3      [ ]         SEQPACKET  CONNECTED     48582    
unix  3      [ ]         SEQPACKET  CONNECTED     47817    
unix  3      [ ]         STREAM     CONNECTED     40834    
unix  3      [ ]         STREAM     CONNECTED     46218    
unix  3      [ ]         STREAM     CONNECTED     39901    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     65741    
unix  3      [ ]         STREAM     CONNECTED     44701    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     47312    
unix  2      [ ]         DGRAM                    43672    
unix  2      [ ]         DGRAM      CONNECTED     65632    
unix  3      [ ]         STREAM     CONNECTED     44460    
unix  3      [ ]         STREAM     CONNECTED     43720    
unix  3      [ ]         STREAM     CONNECTED     40851    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     40811    
unix  3      [ ]         STREAM     CONNECTED     41915    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     46187    
unix  3      [ ]         STREAM     CONNECTED     38602    @/tmp/dbus-6sVF4D5K
unix  3      [ ]         STREAM     CONNECTED     45595    
unix  3      [ ]         STREAM     CONNECTED     53684    
unix  3      [ ]         STREAM     CONNECTED     45702    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     44432    /run/systemd/journal/stdout
unix  3      [ ]         SEQPACKET  CONNECTED     57506    
unix  3      [ ]         STREAM     CONNECTED     46288    
unix  3      [ ]         STREAM     CONNECTED     42741    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     42717    @/home/mtech/.cache/ibus/dbus-dKRWYnve
unix  3      [ ]         STREAM     CONNECTED     44436    
unix  3      [ ]         STREAM     CONNECTED     10426    
unix  3      [ ]         STREAM     CONNECTED     47509    /run/user/1003/wayland-0
unix  3      [ ]         STREAM     CONNECTED     45689    /run/user/1003/at-spi/bus
unix  3      [ ]         STREAM     CONNECTED     44503    
unix  3      [ ]         STREAM     CONNECTED     43748    
unix  3      [ ]         STREAM     CONNECTED     14337    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     67895    
unix  3      [ ]         STREAM     CONNECTED     46188    
unix  3      [ ]         STREAM     CONNECTED     41867    /run/user/1003/gvfsd/socket-Gn3wvMpY
unix  3      [ ]         STREAM     CONNECTED     44215    
unix  3      [ ]         STREAM     CONNECTED     43231    
unix  3      [ ]         STREAM     CONNECTED     42719    
unix  3      [ ]         STREAM     CONNECTED     9980     /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     44496    
unix  3      [ ]         STREAM     CONNECTED     10052    /run/dbus/system_bus_socket
unix  3      [ ]         STREAM     CONNECTED     45594    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     47225    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     41788    
unix  3      [ ]         DGRAM      CONNECTED     10298    
unix  3      [ ]         SEQPACKET  CONNECTED     57505    
unix  3      [ ]         STREAM     CONNECTED     52703    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     40801    /run/systemd/journal/stdout
unix  3      [ ]         STREAM     CONNECTED     43282    
unix  3      [ ]         STREAM     CONNECTED     45703    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     42711    
unix  3      [ ]         STREAM     CONNECTED     44486    
unix  3      [ ]         STREAM     CONNECTED     43679    
unix  3      [ ]         STREAM     CONNECTED     45223    
unix  3      [ ]         STREAM     CONNECTED     53685    
unix  3      [ ]         SEQPACKET  CONNECTED     47816    
unix  3      [ ]         STREAM     CONNECTED     40858    
unix  3      [ ]         STREAM     CONNECTED     46219    
unix  3      [ ]         STREAM     CONNECTED     45611    /run/user/1003/bus
unix  3      [ ]         STREAM     CONNECTED     44309    
unix  3      [ ]         STREAM     CONNECTED     42748    
unix  2      [ ]         STREAM     CONNECTED     41533    @/tmp/dbus-rN2KLlge
mtech@programminlab-H610M-K-DDR4:~/Desktop$ man netstat
mtech@programminlab-H610M-K-DDR4:~/Desktop$ netstat -t
Active Internet connections (w/o servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
tcp        0      0 programminlab-H61:56790 bkk03s01-in-f10.1:https ESTABLISHED
tcp        0      0 programminlab-H61:39546 bkk03s01-in-f10.1:https TIME_WAIT  
tcp        0      0 programminlab-H61:58656 pt-in-f101.1e100.:https ESTABLISHED
tcp        0      0 programminlab-H61:36462 93.243.107.34.bc.:https ESTABLISHED
tcp        0      0 programminlab-H61:58296 lcbome-in-f95.1e1:https ESTABLISHED
tcp        0      0 programminlab-H61:53068 lb-140-82-114-25-:https ESTABLISHED
tcp        0      0 programminlab-H61:59140 cgk03s03-in-f5.1e:https TIME_WAIT  
tcp        0      0 programminlab-H61:41482 hkg07s52-in-f10.1:https ESTABLISHED
mtech@programminlab-H610M-K-DDR4:~/Desktop$ netstat -ut
Active Internet connections (w/o servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
tcp        0      0 programminlab-H61:56790 lcmaaa-aq-in-f10.:https ESTABLISHED
tcp        0      0 programminlab-H61:39546 lcmaaa-aq-in-f10.:https TIME_WAIT  
tcp        0      0 programminlab-H61:58656 pt-in-f101.1e100.:https ESTABLISHED
tcp        0      0 programminlab-H61:36462 93.243.107.34.bc.:https ESTABLISHED
tcp        0      0 programminlab-H61:58296 lcbome-in-f95.1e1:https ESTABLISHED
tcp        0      0 programminlab-H61:53068 lb-140-82-114-25-:https ESTABLISHED
tcp        0      0 programminlab-H61:59140 cgk03s03-in-f5.1e:https TIME_WAIT  
tcp        0      0 programminlab-H61:41482 pnmaaa-be-in-f10.:https ESTABLISHED
udp        0      0 programminlab-H6:bootpc _gateway:bootps         ESTABLISHED
mtech@programminlab-H610M-K-DDR4:~/Desktop$ netstat -u
Active Internet connections (w/o servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State      
udp        0      0 programminlab-H6:bootpc _gateway:bootps         ESTABLISHED
mtech@programminlab-H610M-K-DDR4:~/Desktop$ whois nssce.com
   Domain Name: NSSCE.COM
   Registry Domain ID: 1881501226_DOMAIN_COM-VRSN
   Registrar WHOIS Server: whois.namebright.com
   Registrar URL: http://www.NameBright.com
   Updated Date: 2025-10-22T07:36:55Z
   Creation Date: 2014-10-21T18:26:36Z
   Registry Expiry Date: 2026-10-21T18:26:36Z
   Registrar: TurnCommerce, Inc. DBA NameBright.com
   Registrar IANA ID: 1441
   Registrar Abuse Contact Email: support@namebright.com
   Registrar Abuse Contact Phone: 17204960020
   Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
   Name Server: NSG1.NAMEBRIGHTDNS.COM
   Name Server: NSG2.NAMEBRIGHTDNS.COM
   DNSSEC: unsigned
   URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
>>> Last update of whois database: 2026-07-13T04:28:09Z <<<

For more information on Whois status codes, please visit https://icann.org/epp

NOTICE: The expiration date displayed in this record is the date the
registrar's sponsorship of the domain name registration in the registry is
currently set to expire. This date does not necessarily reflect the expiration
date of the domain name registrant's agreement with the sponsoring
registrar.  Users may consult the sponsoring registrar's Whois database to
view the registrar's reported date of expiration for this registration.

TERMS OF USE: You are not authorized to access or query our Whois
database through the use of electronic processes that are high-volume and
automated except as reasonably necessary to register domain names or
modify existing registrations; the Data in VeriSign Global Registry
Services' ("VeriSign") Whois database is provided by VeriSign for
information purposes only, and to assist persons in obtaining information
about or related to a domain name registration record. VeriSign does not
guarantee its accuracy. By submitting a Whois query, you agree to abide
by the following terms of use: You agree that you may use this Data only
for lawful purposes and that under no circumstances will you use this Data
to: (1) allow, enable, or otherwise support the transmission of mass
unsolicited, commercial advertising or solicitations via e-mail, telephone,
or facsimile; or (2) enable high volume, automated, electronic processes
that apply to VeriSign (or its computer systems). The compilation,
repackaging, dissemination or other use of this Data is expressly
prohibited without the prior written consent of VeriSign. You agree not to
use electronic processes that are automated and high-volume to access or
query the Whois database except as reasonably necessary to register
domain names or modify existing registrations. VeriSign reserves the right
to restrict your access to the Whois database in its sole discretion to ensure
operational stability.  VeriSign may restrict or terminate your access to the
Whois database for failure to abide by these terms of use. VeriSign
reserves the right to modify these terms at any time.

The Registry database contains ONLY .COM, .NET, .EDU domains and
Registrars.
Domain Name: NSSCE.COM
Registry Domain ID: 1881501226_DOMAIN_COM-VRSN
Registrar WHOIS Server: whois.NameBright.com
Registrar URL: https://www.NameBright.com
Updated Date: 2020-10-15T07:07:53.712Z
Creation Date: 2014-10-21T18:26:36.000Z
Registrar Registration Expiration Date: 2026-10-21T18:26:36.000Z
Registrar: TurnCommerce, Inc. DBA NameBright.com
Registrar IANA ID: 1441
Registrar Abuse Contact Email: abuse@NameBright.com
Registrar Abuse Contact Phone: +1.7204960020
Domain Status: clientTransferProhibited https://www.icann.org/epp#clientTransferProhibited
Registry Registrant ID: Not Available From Registry
Registrant Name: Domain Admin / This Domain is For Sale
Registrant Organization: HugeDomains.com
Registrant Street: 2635 Walnut Street
Registrant City: Denver
Registrant State/Province: CO
Registrant Postal Code: 80205
Registrant Country: US
Registrant Phone: +1.3038930552
Registrant Phone Ext: 
Registrant Fax: 
Registrant Fax Ext: 
Registrant Email: domains@hugedomains.com
Registry Admin ID: Not Available From Registry
Admin Name: Domain Admin / This Domain is For Sale
Admin Organization: HugeDomains.com
Admin Street: 2635 Walnut Street
Admin City: Denver
Admin State/Province: CO
Admin Postal Code: 80205
Admin Country: US
Admin Phone: +1.3038930552
Admin Phone Ext: 
Admin Fax: 
Admin Fax Ext: 
Admin Email: domains@hugedomains.com
Registry Tech ID: Not Available From Registry
Tech Name: Domain Admin / This Domain is For Sale
Tech Organization: HugeDomains.com
Tech Street: 2635 Walnut Street
Tech City: Denver
Tech State/Province: CO
Tech Postal Code: 80205
Tech Country: US
Tech Phone: +1.3038930552
Tech Phone Ext: 
Tech Fax: 
Tech Fax Ext: 
Tech Email: domains@hugedomains.com
Name Server: NSG1.NAMEBRIGHTDNS.COM
Name Server: NSG2.NAMEBRIGHTDNS.COM
DNSSEC: unsigned
URL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/
>>> Last update of WHOIS database: 2020-10-15T07:07:53.712Z <<<
mtech@programminlab-H610M-K-DDR4:~/Desktop$ sudo nmap -A 10.10.1.125
Starting Nmap 7.80 ( https://nmap.org ) at 2026-07-13 10:05 IST
Nmap scan report for 10.10.1.125
Host is up (0.00018s latency).
All 1000 scanned ports on 10.10.1.125 are closed
MAC Address: 30:56:0F:55:64:74 (Unknown)
Too many fingerprints match this host to give specific OS details
Network Distance: 1 hop

TRACEROUTE
HOP RTT     ADDRESS
1   0.18 ms 10.10.1.125

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 12.37 seconds
mtech@programminlab-H610M-K-DDR4:~/Desktop$ sudo tcpdump -i any
[sudo] password for mtech: 
tcpdump: data link type LINUX_SLL2
tcpdump: verbose output suppressed, use -v[v]... for full protocol decode
listening on any, link-type LINUX_SLL2 (Linux cooked v2), snapshot length 262144 bytes
10:26:34.078823 enp2s0 M   IP 192.168.1.216.mdns > mdns.mcast.net.mdns: 0- [0q] 1/0/0 TXT "type=0" "version=1" "refresh-age-timeout=0" "priority=6" "refresh-flag=0" "root-mac-address=20:cf:ae:12:7e:5f" "cost=0" "transm-address=192.168.1.216" "transm-interface=100000" "voice-vlan-id=1" "voice-vlan-vpt=5" "voice-vlan-dscp=46" "md5-auth=01acf7396d224da8a0f1c3974eb6fb5216" (321)
10:26:34.135075 lo    In  IP localhost.52284 > localhost.domain: 37714+ [1au] PTR? 251.0.0.224.in-addr.arpa. (53)
10:26:34.135530 enp2s0 Out IP programminlab-H610M-K-DDR4.44349 > dns.google.domain: 19167+ [1au] PTR? 251.0.0.224.in-addr.arpa. (53)
10:26:34.150152 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.44349: 19167 1/0/1 PTR mdns.mcast.net. (81)
10:26:34.150456 lo    In  IP localhost.domain > localhost.52284: 37714 1/0/1 PTR mdns.mcast.net. (81)
10:26:34.150733 lo    In  IP localhost.51698 > localhost.domain: 16719+ [1au] PTR? 216.1.168.192.in-addr.arpa. (55)
10:26:34.150975 enp2s0 Out IP programminlab-H610M-K-DDR4.43917 > dns.google.domain: 58602+ [1au] PTR? 216.1.168.192.in-addr.arpa. (55)
10:26:34.165345 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.43917: 58602 NXDomain 0/0/1 (55)
10:26:34.165478 enp2s0 Out IP programminlab-H610M-K-DDR4.43917 > dns.google.domain: 58602+ PTR? 216.1.168.192.in-addr.arpa. (44)
10:26:34.179683 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.43917: 58602 NXDomain 0/0/0 (44)
10:26:34.179988 lo    In  IP localhost.domain > localhost.51698: 16719 NXDomain 0/0/1 (55)
10:26:34.235861 lo    In  IP localhost.54167 > localhost.domain: 17278+ [1au] PTR? 53.0.0.127.in-addr.arpa. (52)
10:26:34.236082 lo    In  IP localhost.domain > localhost.54167: 17278*$ 1/0/1 PTR localhost. (75)
10:26:34.236319 lo    In  IP localhost.35374 > localhost.domain: 40332+ [1au] PTR? 8.8.8.8.in-addr.arpa. (49)
10:26:34.236596 enp2s0 Out IP programminlab-H610M-K-DDR4.43846 > dns.google.domain: 46110+ [1au] PTR? 8.8.8.8.in-addr.arpa. (49)
10:26:34.251413 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.43846: 46110 1/0/1 PTR dns.google. (73)
10:26:34.251749 lo    In  IP localhost.domain > localhost.35374: 40332 1/0/1 PTR dns.google. (73)
10:26:34.252011 lo    In  IP localhost.42893 > localhost.domain: 14057+ [1au] PTR? 105.1.10.10.in-addr.arpa. (53)
10:26:34.252245 enp2s0 Out IP programminlab-H610M-K-DDR4.45144 > dns.google.domain: 45672+ [1au] PTR? 105.1.10.10.in-addr.arpa. (53)
10:26:34.266780 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.45144: 45672 NXDomain 0/0/1 (53)
10:26:34.266970 enp2s0 Out IP programminlab-H610M-K-DDR4.45144 > dns.google.domain: 45672+ PTR? 105.1.10.10.in-addr.arpa. (42)
10:26:34.280923 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.45144: 45672 NXDomain 0/0/0 (42)
10:26:34.281384 lo    In  IP localhost.domain > localhost.42893: 14057*$ 2/0/1 PTR programminlab-H610M-K-DDR4., PTR programminlab-H610M-K-DDR4.local. (139)
10:26:34.455208 enp2s0 B   ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:26:34.547819 lo    In  IP localhost.41969 > localhost.domain: 22958+ [1au] PTR? 5.1.10.10.in-addr.arpa. (51)
10:26:34.548149 enp2s0 Out IP programminlab-H610M-K-DDR4.55471 > dns.google.domain: 6933+ [1au] PTR? 5.1.10.10.in-addr.arpa. (51)
10:26:34.563910 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.55471: 6933 NXDomain 0/0/1 (51)
10:26:34.564097 enp2s0 Out IP programminlab-H610M-K-DDR4.55471 > dns.google.domain: 6933+ PTR? 5.1.10.10.in-addr.arpa. (40)
10:26:34.578978 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.55471: 6933 NXDomain 0/0/0 (40)
10:26:34.579310 lo    In  IP localhost.domain > localhost.41969: 22958 NXDomain 0/0/1 (51)
10:26:34.579603 lo    In  IP localhost.37194 > localhost.domain: 156+ [1au] PTR? 2.1.10.10.in-addr.arpa. (51)
10:26:34.579976 enp2s0 Out IP programminlab-H610M-K-DDR4.56950 > dns.google.domain: 49106+ [1au] PTR? 2.1.10.10.in-addr.arpa. (51)
10:26:34.594395 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.56950: 49106 NXDomain 0/0/1 (51)
10:26:34.594553 enp2s0 Out IP programminlab-H610M-K-DDR4.56950 > dns.google.domain: 49106+ PTR? 2.1.10.10.in-addr.arpa. (40)
10:26:34.608325 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.56950: 49106 NXDomain 0/0/0 (40)
10:26:34.608737 lo    In  IP localhost.domain > localhost.37194: 156*$ 1/0/1 PTR _gateway. (73)
10:26:35.371781 enp2s0 B   IP 10.10.1.53.53755 > 255.255.255.255.29810: UDP, length 366
10:26:35.379791 lo    In  IP localhost.41714 > localhost.domain: 16981+ [1au] PTR? 255.255.255.255.in-addr.arpa. (57)
10:26:35.380047 lo    In  IP localhost.domain > localhost.41714: 16981 NXDomain*$ 0/0/1 (57)
10:26:35.380149 lo    In  IP localhost.37255 > localhost.domain: 27994+ [1au] PTR? 53.1.10.10.in-addr.arpa. (52)
10:26:35.380546 enp2s0 Out IP programminlab-H610M-K-DDR4.34900 > dns.google.domain: 12888+ [1au] PTR? 53.1.10.10.in-addr.arpa. (52)
10:26:35.409633 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.34900: 12888 NXDomain 0/0/1 (52)
10:26:35.409785 enp2s0 Out IP programminlab-H610M-K-DDR4.34900 > dns.google.domain: 12888+ PTR? 53.1.10.10.in-addr.arpa. (41)
10:26:35.424029 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.34900: 12888 NXDomain 0/0/0 (41)
10:26:35.424342 lo    In  IP localhost.domain > localhost.37255: 27994 NXDomain 0/0/1 (52)
10:26:35.458500 enp2s0 B   ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:26:36.451046 lo    In  IP localhost.58501 > localhost.domain: 64695+ [1au] A? ssl.gstatic.com. (44)
10:26:36.451356 enp2s0 Out IP programminlab-H610M-K-DDR4.35825 > dns.google.domain: 31608+ [1au] A? ssl.gstatic.com. (44)
10:26:36.452959 enp2s0 Out IP programminlab-H610M-K-DDR4.43112 > lcbomp-in-f94.1e100.net.https: Flags [P.], seq 2963018200:2963018300, ack 4147492794, win 717, options [nop,nop,TS val 4099387487 ecr 183305], length 100
10:26:36.453121 enp2s0 In  IP lcbomp-in-f94.1e100.net.https > programminlab-H610M-K-DDR4.43112: Flags [.], ack 100, win 1540, options [nop,nop,TS val 192409 ecr 4099387487], length 0
10:26:36.461836 enp2s0 B   ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:26:36.477324 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.35825: 31608 1/0/1 A 142.251.43.35 (60)
10:26:36.477435 lo    In  IP localhost.domain > localhost.58501: 64695 1/0/1 A 142.251.43.35 (60)
10:26:36.477488 lo    In  IP localhost.60343 > localhost.domain: 59057+ [1au] AAAA? ssl.gstatic.com. (44)
10:26:36.477586 enp2s0 Out IP programminlab-H610M-K-DDR4.56614 > dns.google.domain: 2161+ [1au] AAAA? ssl.gstatic.com. (44)
10:26:36.508268 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.56614: 2161 1/0/1 AAAA 2404:6800:4007:805::2003 (72)
10:26:36.508521 lo    In  IP localhost.domain > localhost.60343: 59057 1/0/1 AAAA 2404:6800:4007:805::2003 (72)
10:26:36.523980 lo    In  IP localhost.52495 > localhost.domain: 25560+ [1au] PTR? 94.211.178.192.in-addr.arpa. (56)
10:26:36.524287 enp2s0 Out IP programminlab-H610M-K-DDR4.59812 > dns.google.domain: 26146+ [1au] PTR? 94.211.178.192.in-addr.arpa. (56)
10:26:36.553985 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.59812: 26146 1/0/1 PTR lcbomp-in-f94.1e100.net. (93)
10:26:36.554260 lo    In  IP localhost.domain > localhost.52495: 25560 1/0/1 PTR lcbomp-in-f94.1e100.net. (93)
10:26:36.556221 enp2s0 In  IP lcbomp-in-f94.1e100.net.https > programminlab-H610M-K-DDR4.43112: Flags [P.], seq 1:173, ack 100, win 1540, options [nop,nop,TS val 192440 ecr 4099387487], length 172
10:26:36.596582 enp2s0 Out IP programminlab-H610M-K-DDR4.43112 > lcbomp-in-f94.1e100.net.https: Flags [.], ack 173, win 717, options [nop,nop,TS val 4099387631 ecr 192440], length 0
10:26:36.596781 enp2s0 In  IP lcbomp-in-f94.1e100.net.https > programminlab-H610M-K-DDR4.43112: Flags [P.], seq 173:243, ack 100, win 1540, options [nop,nop,TS val 192452 ecr 4099387631], length 70
10:26:36.596817 enp2s0 Out IP programminlab-H610M-K-DDR4.43112 > lcbomp-in-f94.1e100.net.https: Flags [.], ack 243, win 717, options [nop,nop,TS val 4099387631 ecr 192452], length 0
10:26:36.597113 enp2s0 Out IP programminlab-H610M-K-DDR4.43112 > lcbomp-in-f94.1e100.net.https: Flags [P.], seq 100:139, ack 243, win 717, options [nop,nop,TS val 4099387631 ecr 192452], length 39
10:26:36.597336 enp2s0 In  IP lcbomp-in-f94.1e100.net.https > programminlab-H610M-K-DDR4.43112: Flags [.], ack 139, win 1540, options [nop,nop,TS val 192452 ecr 4099387631], length 0
10:26:36.625288 enp2s0 B   IP 10.10.1.52.59217 > 255.255.255.255.29810: UDP, length 366
10:26:36.628194 lo    In  IP localhost.44608 > localhost.domain: 42604+ [1au] PTR? 52.1.10.10.in-addr.arpa. (52)
10:26:36.628609 enp2s0 Out IP programminlab-H610M-K-DDR4.33591 > dns.google.domain: 26137+ [1au] PTR? 52.1.10.10.in-addr.arpa. (52)
10:26:36.684078 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.33591: 26137 NXDomain 0/0/1 (52)
10:26:36.684247 enp2s0 Out IP programminlab-H610M-K-DDR4.33591 > dns.google.domain: 26137+ PTR? 52.1.10.10.in-addr.arpa. (41)
10:26:36.699690 enp2s0 In  IP dns.google.domain > programminlab-H610M-K-DDR4.33591: 26137 NXDomain 0/0/0 (41)
10:26:36.700014 lo    In  IP localhost.domain > localhost.44608: 42604 NXDomain 0/0/1 (52)
10:26:37.468573 enp2s0 B   ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:26:38.471913 enp2s0 B   ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:26:39.078979 enp2s0 M   IP 192.168.1.216.mdns > mdns.mcast.net.mdns: 0- [0q] 1/0/0 TXT "type=0" "version=1" "refresh-age-timeout=0" "priority=6" "refresh-flag=0" "root-mac-address=20:cf:ae:12:7e:5f" "cost=0" "transm-address=192.168.1.216" "transm-interface=100000" "voice-vlan-id=1" "voice-vlan-vpt=5" "voice-vlan-dscp=46" "md5-auth=01acf7396d224da8a0f1c3974eb6fb5216" (321)
10:26:39.475251 enp2s0 B   ARP, Request who-has 10.10.1.5 tell _gateway, length 46
^C10:26:40.212440 enp2s0 In  IP pt-in-f95.1e100.net.https > programminlab-H610M-K-DDR4.49114: UDP, length 280

79 packets captured
145 packets received by filter
13 packets dropped by kernel
mtech@programminlab-H610M-K-DDR4:~/Desktop$ sudo tcpdump -i enp2s0
tcpdump: verbose output suppressed, use -v[v]... for full protocol decode
listening on enp2s0, link-type EN10MB (Ethernet), snapshot length 262144 bytes
10:27:09.772257 ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:27:09.844761 IP programminlab-H610M-K-DDR4.53662 > b.resolvers.level3.net.domain: 23042+ [1au] PTR? 5.1.10.10.in-addr.arpa. (51)
10:27:10.071512 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.53662: 23042 NXDomain* 0/1/1 (110)
10:27:10.071681 IP programminlab-H610M-K-DDR4.53662 > b.resolvers.level3.net.domain: 23042+ PTR? 5.1.10.10.in-addr.arpa. (40)
10:27:10.298155 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.53662: 23042 NXDomain* 0/1/0 (99)
10:27:10.299245 IP programminlab-H610M-K-DDR4.43325 > b.resolvers.level3.net.domain: 32390+ [1au] PTR? 2.1.10.10.in-addr.arpa. (51)
10:27:10.368870 IP programminlab-H610M-K-DDR4.33713 > b.resolvers.level3.net.domain: 1077+ [1au] Type65? accounts.google.com. (48)
10:27:10.369023 IP programminlab-H610M-K-DDR4.53899 > b.resolvers.level3.net.domain: 28399+ [1au] A? accounts.google.com. (48)
10:27:10.369906 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [S], seq 762428860, win 64240, options [mss 1460,sackOK,TS val 2873181498 ecr 0,nop,wscale 7], length 0
10:27:10.370279 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [S.], seq 3115385634, ack 762428861, win 32768, options [mss 1400,sackOK,TS val 202584 ecr 2873181498,nop,wscale 5], length 0
10:27:10.370333 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [.], ack 1, win 502, options [nop,nop,TS val 2873181498 ecr 202584], length 0
10:27:10.372395 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [.], seq 1:1389, ack 1, win 502, options [nop,nop,TS val 2873181500 ecr 202584], length 1388
10:27:10.372400 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [P.], seq 1389:2474, ack 1, win 502, options [nop,nop,TS val 2873181500 ecr 202584], length 1085
10:27:10.372611 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [P.], seq 2474:2480, ack 1, win 502, options [nop,nop,TS val 2873181501 ecr 202584], length 6
10:27:10.372631 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [P.], seq 2480:2572, ack 1, win 502, options [nop,nop,TS val 2873181501 ecr 202584], length 92
10:27:10.372692 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [.], ack 1389, win 1540, options [nop,nop,TS val 202585 ecr 2873181500], length 0
10:27:10.372695 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [.], ack 2474, win 1540, options [nop,nop,TS val 202585 ecr 2873181500], length 0
10:27:10.372748 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [.], ack 2480, win 1540, options [nop,nop,TS val 202585 ecr 2873181501], length 0
10:27:10.372779 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [.], ack 2572, win 1540, options [nop,nop,TS val 202585 ecr 2873181501], length 0
10:27:10.421037 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.33713: 1077 0/1/1 (98)
10:27:10.435582 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [P.], seq 1:1859, ack 2572, win 1540, options [nop,nop,TS val 202603 ecr 2873181501], length 1858
10:27:10.435614 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [.], ack 1859, win 532, options [nop,nop,TS val 2873181564 ecr 202603], length 0
10:27:10.435803 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [P.], seq 1859:1921, ack 2572, win 1540, options [nop,nop,TS val 202604 ecr 2873181564], length 62
10:27:10.435831 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [.], ack 1921, win 532, options [nop,nop,TS val 2873181564 ecr 202604], length 0
10:27:10.436586 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [P.], seq 1921:1952, ack 2572, win 1540, options [nop,nop,TS val 202604 ecr 2873181564], length 31
10:27:10.436608 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [.], ack 1952, win 532, options [nop,nop,TS val 2873181565 ecr 202604], length 0
10:27:10.438223 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [P.], seq 2572:2656, ack 1952, win 532, options [nop,nop,TS val 2873181566 ecr 202604], length 84
10:27:10.438457 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [.], ack 2656, win 1540, options [nop,nop,TS val 202604 ecr 2873181566], length 0
10:27:10.439153 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [P.], seq 2656:2687, ack 1952, win 532, options [nop,nop,TS val 2873181567 ecr 202604], length 31
10:27:10.439274 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [.], ack 2687, win 1540, options [nop,nop,TS val 202605 ecr 2873181567], length 0
10:27:10.439683 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [.], seq 2687:4075, ack 1952, win 532, options [nop,nop,TS val 2873181568 ecr 202605], length 1388
10:27:10.439685 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [.], seq 4075:5463, ack 1952, win 532, options [nop,nop,TS val 2873181568 ecr 202605], length 1388
10:27:10.439687 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [P.], seq 5463:5956, ack 1952, win 532, options [nop,nop,TS val 2873181568 ecr 202605], length 493
10:27:10.439751 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [P.], seq 5956:6014, ack 1952, win 532, options [nop,nop,TS val 2873181568 ecr 202605], length 58
10:27:10.439924 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [.], ack 5956, win 1540, options [nop,nop,TS val 202605 ecr 2873181568], length 0
10:27:10.439956 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [.], ack 6014, win 1540, options [nop,nop,TS val 202605 ecr 2873181568], length 0
10:27:10.523848 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.43325: 32390 NXDomain* 0/1/1 (110)
10:27:10.524073 IP programminlab-H610M-K-DDR4.43325 > b.resolvers.level3.net.domain: 32390+ PTR? 2.1.10.10.in-addr.arpa. (40)
10:27:10.596827 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.53899: 28399 1/0/1 A 192.178.211.84 (64)
10:27:10.597558 IP programminlab-H610M-K-DDR4.46039 > b.resolvers.level3.net.domain: 20052+ [1au] AAAA? accounts.google.com. (48)
10:27:10.602078 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [P.], seq 1952:3838, ack 6014, win 1540, options [nop,nop,TS val 202653 ecr 2873181568], length 1886
10:27:10.602113 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [.], ack 3838, win 561, options [nop,nop,TS val 2873181730 ecr 202653], length 0
10:27:10.602763 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [P.], seq 3838:3931, ack 6014, win 1540, options [nop,nop,TS val 202654 ecr 2873181730], length 93
10:27:10.643584 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [.], ack 3931, win 561, options [nop,nop,TS val 2873181772 ecr 202654], length 0
10:27:10.643786 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [P.], seq 3931:4001, ack 6014, win 1540, options [nop,nop,TS val 202666 ecr 2873181772], length 70
10:27:10.643818 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [.], ack 4001, win 561, options [nop,nop,TS val 2873181772 ecr 202666], length 0
10:27:10.644110 IP programminlab-H610M-K-DDR4.35796 > lcbomp-in-f84.1e100.net.https: Flags [P.], seq 6014:6053, ack 4001, win 561, options [nop,nop,TS val 2873181772 ecr 202666], length 39
10:27:10.644297 IP lcbomp-in-f84.1e100.net.https > programminlab-H610M-K-DDR4.35796: Flags [.], ack 6053, win 1540, options [nop,nop,TS val 202666 ecr 2873181772], length 0
10:27:10.649679 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.46039: 20052 1/0/1 AAAA 2404:6800:4000:1025::54 (76)
10:27:10.748143 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.43325: 32390 NXDomain* 0/1/0 (99)
10:27:10.749440 IP programminlab-H610M-K-DDR4.36609 > b.resolvers.level3.net.domain: 198+ [1au] PTR? 2.2.2.4.in-addr.arpa. (49)
10:27:10.802251 ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:27:11.433331 IP programminlab-H610M-K-DDR4.40945 > b.resolvers.level3.net.domain: 31380+ [1au] PTR? 84.211.178.192.in-addr.arpa. (56)
10:27:11.486019 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.40945: 31380 1/0/1 PTR lcbomp-in-f84.1e100.net. (93)
10:27:11.803642 IP programminlab-H610M-K-DDR4.36252 > dclaxb-ax-in-f14.1e100.net.https: UDP, length 1252
10:27:11.803647 IP programminlab-H610M-K-DDR4.36252 > dclaxb-ax-in-f14.1e100.net.https: UDP, length 1252
10:27:11.803648 IP programminlab-H610M-K-DDR4.36252 > dclaxb-ax-in-f14.1e100.net.https: UDP, length 851
10:27:11.805582 ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:27:11.852305 IP programminlab-H610M-K-DDR4.40849 > b.resolvers.level3.net.domain: 24081+ [1au] PTR? 14.45.251.142.in-addr.arpa. (55)
10:27:11.904137 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.40849: 24081 2/0/1 PTR dclaxb-ax-in-f14.1e100.net., PTR iad66s01-in-f14.1e100.net. (125)
10:27:12.041785 IP dclaxb-ax-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.36252: UDP, length 36
10:27:12.042022 IP programminlab-H610M-K-DDR4.36252 > dclaxb-ax-in-f14.1e100.net.https: UDP, length 33
10:27:12.093036 IP dclaxb-ax-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.36252: UDP, length 312
10:27:12.093553 IP programminlab-H610M-K-DDR4.36252 > dclaxb-ax-in-f14.1e100.net.https: UDP, length 34
10:27:12.113184 IP programminlab-H610M-K-DDR4.36252 > dclaxb-ax-in-f14.1e100.net.https: UDP, length 34
10:27:12.332625 IP dclaxb-ax-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.36252: UDP, length 29
10:27:12.808969 ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:27:12.853290 IP 10.10.1.54.54124 > 255.255.255.255.29810: UDP, length 366
10:27:12.892687 IP programminlab-H610M-K-DDR4.52434 > b.resolvers.level3.net.domain: 20038+ [1au] PTR? 54.1.10.10.in-addr.arpa. (52)
10:27:12.992241 STP 802.1w, Rapid STP, Flags [Learn, Forward, Agreement], bridge-id 8000.20:cf:ae:12:6f:31.800c, length 36
10:27:13.115882 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.52434: 20038 NXDomain* 0/1/1 (111)
10:27:13.116124 IP programminlab-H610M-K-DDR4.52434 > b.resolvers.level3.net.domain: 20038+ PTR? 54.1.10.10.in-addr.arpa. (41)
10:27:13.337914 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.52434: 20038 NXDomain* 0/1/0 (100)
10:27:13.526288 IP 10.10.1.55.51531 > 255.255.255.255.29810: UDP, length 366
10:27:13.620282 IP programminlab-H610M-K-DDR4.54533 > b.resolvers.level3.net.domain: 32461+ [1au] PTR? 55.1.10.10.in-addr.arpa. (52)
10:27:13.672207 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.54533: 32461 NXDomain* 0/1/1 (111)
10:27:13.672387 IP programminlab-H610M-K-DDR4.54533 > b.resolvers.level3.net.domain: 32461+ PTR? 55.1.10.10.in-addr.arpa. (41)
10:27:13.723788 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.54533: 32461 NXDomain* 0/1/0 (100)
10:27:13.882285 ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:27:14.078922 IP 192.168.1.216.mdns > mdns.mcast.net.mdns: 0- [0q] 1/0/0 TXT "type=0" "version=1" "refresh-age-timeout=0" "priority=6" "refresh-flag=0" "root-mac-address=20:cf:ae:12:7e:5f" "cost=0" "transm-address=192.168.1.216" "transm-interface=100000" "voice-vlan-id=1" "voice-vlan-vpt=5" "voice-vlan-dscp=46" "md5-auth=01acf7396d224da8a0f1c3974eb6fb5216" (321)
10:27:14.140283 IP programminlab-H610M-K-DDR4.43313 > b.resolvers.level3.net.domain: 29121+ [1au] PTR? 251.0.0.224.in-addr.arpa. (53)
10:27:14.373384 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.43313: 29121 1/0/1 PTR mdns.mcast.net. (81)
10:27:14.374428 IP programminlab-H610M-K-DDR4.36250 > b.resolvers.level3.net.domain: 49299+ [1au] PTR? 216.1.168.192.in-addr.arpa. (55)
10:27:14.607197 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.36250: 49299 NXDomain* 0/1/1 (114)
10:27:14.607421 IP programminlab-H610M-K-DDR4.36250 > b.resolvers.level3.net.domain: 49299+ PTR? 216.1.168.192.in-addr.arpa. (44)
10:27:14.839668 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.36250: 49299 NXDomain* 0/1/0 (103)
10:27:14.885627 ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:27:14.992287 STP 802.1w, Rapid STP, Flags [Learn, Forward, Agreement], bridge-id 8000.20:cf:ae:12:6f:31.800c, length 36
10:27:15.587199 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [P.], seq 1465443207:1465443487, ack 3679468011, win 618, options [nop,nop,TS val 3947139020 ecr 201847], length 280
10:27:15.587437 IP pnmaaa-ba-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.44766: Flags [.], ack 280, win 1540, options [nop,nop,TS val 204149 ecr 3947139020], length 0
10:27:15.596109 IP programminlab-H610M-K-DDR4.36617 > b.resolvers.level3.net.domain: 21767+ [1au] PTR? 206.221.251.142.in-addr.arpa. (57)
10:27:15.682032 IP pnmaaa-ba-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.44766: Flags [P.], seq 1:86, ack 280, win 1540, options [nop,nop,TS val 204177 ecr 3947139020], length 85
10:27:15.682466 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [P.], seq 280:319, ack 86, win 618, options [nop,nop,TS val 3947139115 ecr 204177], length 39
10:27:15.682614 IP pnmaaa-ba-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.44766: Flags [.], ack 319, win 1540, options [nop,nop,TS val 204178 ecr 3947139115], length 0
10:27:15.683770 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [.], seq 319:1707, ack 86, win 618, options [nop,nop,TS val 3947139117 ecr 204178], length 1388
10:27:15.683776 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [P.], seq 1707:2558, ack 86, win 618, options [nop,nop,TS val 3947139117 ecr 204178], length 851
10:27:15.683818 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [.], seq 2558:3946, ack 86, win 618, options [nop,nop,TS val 3947139117 ecr 204178], length 1388
10:27:15.683820 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [.], seq 3946:5334, ack 86, win 618, options [nop,nop,TS val 3947139117 ecr 204178], length 1388
10:27:15.683821 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [.], seq 5334:6722, ack 86, win 618, options [nop,nop,TS val 3947139117 ecr 204178], length 1388
10:27:15.683822 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [.], seq 6722:8110, ack 86, win 618, options [nop,nop,TS val 3947139117 ecr 204178], length 1388
10:27:15.683823 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [P.], seq 8110:9498, ack 86, win 618, options [nop,nop,TS val 3947139117 ecr 204178], length 1388
10:27:15.683831 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [P.], seq 9498:9865, ack 86, win 618, options [nop,nop,TS val 3947139117 ecr 204178], length 367
10:27:15.684214 IP pnmaaa-ba-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.44766: Flags [.], ack 1707, win 1540, options [nop,nop,TS val 204178 ecr 3947139117], length 0
10:27:15.684217 IP pnmaaa-ba-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.44766: Flags [.], ack 2558, win 1540, options [nop,nop,TS val 204178 ecr 3947139117], length 0
10:27:15.684218 IP pnmaaa-ba-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.44766: Flags [.], ack 9498, win 1540, options [nop,nop,TS val 204178 ecr 3947139117], length 0
10:27:15.684219 IP pnmaaa-ba-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.44766: Flags [.], ack 9865, win 1540, options [nop,nop,TS val 204178 ecr 3947139117], length 0
10:27:15.757611 IP 10.10.1.53.53755 > 255.255.255.255.29810: UDP, length 366
10:27:15.787197 IP 10.10.1.50 > igmp.mcast.net: igmp v3 report, 1 group record(s)
10:27:15.806545 IP pnmaaa-ba-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.44766: Flags [P.], seq 86:852, ack 9865, win 1540, options [nop,nop,TS val 204215 ecr 3947139117], length 766
10:27:15.835667 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.36617: 21767 1/0/1 PTR pnmaaa-ba-in-f14.1e100.net. (97)
10:27:15.837112 IP programminlab-H610M-K-DDR4.49247 > b.resolvers.level3.net.domain: 60180+ [1au] PTR? 53.1.10.10.in-addr.arpa. (52)
10:27:15.847529 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [.], ack 852, win 618, options [nop,nop,TS val 3947139281 ecr 204215], length 0
10:27:15.847698 IP pnmaaa-ba-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.44766: Flags [P.], seq 852:922, ack 9865, win 1540, options [nop,nop,TS val 204227 ecr 3947139281], length 70
10:27:15.847719 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [.], ack 922, win 618, options [nop,nop,TS val 3947139281 ecr 204227], length 0
10:27:15.848025 IP programminlab-H610M-K-DDR4.44766 > pnmaaa-ba-in-f14.1e100.net.https: Flags [P.], seq 9865:9904, ack 922, win 618, options [nop,nop,TS val 3947139281 ecr 204227], length 39
10:27:15.848182 IP pnmaaa-ba-in-f14.1e100.net.https > programminlab-H610M-K-DDR4.44766: Flags [.], ack 9904, win 1540, options [nop,nop,TS val 204227 ecr 3947139281], length 0
10:27:15.888968 ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:27:15.889232 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.49247: 60180 NXDomain* 0/1/1 (111)
10:27:15.889394 IP programminlab-H610M-K-DDR4.49247 > b.resolvers.level3.net.domain: 60180+ PTR? 53.1.10.10.in-addr.arpa. (41)
10:27:15.940770 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.49247: 60180 NXDomain* 0/1/0 (100)
10:27:15.942029 IP programminlab-H610M-K-DDR4.57884 > b.resolvers.level3.net.domain: 30159+ [1au] PTR? 22.0.0.224.in-addr.arpa. (52)
10:27:15.945116 IP 10.10.1.50 > igmp.mcast.net: igmp v3 report, 1 group record(s)
10:27:15.994346 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.57884: 30159 1/0/1 PTR igmp.mcast.net. (80)
10:27:15.995224 IP programminlab-H610M-K-DDR4.39398 > b.resolvers.level3.net.domain: 50763+ [1au] PTR? 50.1.10.10.in-addr.arpa. (52)
10:27:16.223183 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.39398: 50763 NXDomain* 0/1/1 (111)
10:27:16.223436 IP programminlab-H610M-K-DDR4.39398 > b.resolvers.level3.net.domain: 50763+ PTR? 50.1.10.10.in-addr.arpa. (41)
10:27:16.450876 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.39398: 50763 NXDomain* 0/1/0 (100)
10:27:16.803781 IP 10.10.1.50 > igmp.mcast.net: igmp v3 report, 1 group record(s)
10:27:16.922331 ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:27:16.945169 IP 10.10.1.50 > igmp.mcast.net: igmp v3 report, 1 group record(s)
10:27:16.992122 STP 802.1w, Rapid STP, Flags [Learn, Forward, Agreement], bridge-id 8000.20:cf:ae:12:6f:31.800c, length 36
10:27:17.058454 IP 10.10.1.52.59217 > 255.255.255.255.29810: UDP, length 366
10:27:17.156285 IP programminlab-H610M-K-DDR4.33524 > b.resolvers.level3.net.domain: 27156+ [1au] PTR? 52.1.10.10.in-addr.arpa. (52)
10:27:17.209758 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.33524: 27156 NXDomain* 0/1/1 (111)
10:27:17.209964 IP programminlab-H610M-K-DDR4.33524 > b.resolvers.level3.net.domain: 27156+ PTR? 52.1.10.10.in-addr.arpa. (41)
10:27:17.263421 IP b.resolvers.level3.net.domain > programminlab-H610M-K-DDR4.33524: 27156 NXDomain* 0/1/0 (100)
10:27:17.925675 ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:27:18.929032 ARP, Request who-has 10.10.1.5 tell _gateway, length 46
10:27:18.992272 STP 802.1w, Rapid STP, Flags [Learn, Forward, Agreement], bridge-id 8000.20:cf:ae:12:6f:31.800c, length 36
10:27:19.078948 IP 192.168.1.216.mdns > mdns.mcast.net.mdns: 0- [0q] 1/0/0 TXT "type=0" "version=1" "refresh-age-timeout=0" "priority=6" "refresh-flag=0" "root-mac-address=20:cf:ae:12:7e:5f" "cost=0" "transm-address=192.168.1.216" "transm-interface=100000" "voice-vlan-id=1" "voice-vlan-vpt=5" "voice-vlan-dscp=46" "md5-auth=01acf7396d224da8a0f1c3974eb6fb5216" (321)
^C
140 packets captured
146 packets received by filter
6 packets dropped by kernel



mtech@programminlab-H610M-K-DDR4:~/Desktop$ python3 -m venv venv
mtech@programminlab-H610M-K-DDR4:~/Desktop$ source venv/bin/activate


(venv) mtech@programminlab-H610M-K-DDR4:~/Desktop$ speedtest-cli
Retrieving speedtest.net configuration...
Testing from BSNL (117.250.233.252)...
Retrieving speedtest.net server list...
Selecting best server based on ping...
Hosted by Cherrinet - K Net Solutions Pvt Ltd (Salem) [268.27 km]: 2626.804 ms
Testing download speed................................................................................
Download: 27.72 Mbit/s
Testing upload speed......................................................................................................
Upload: 27.83 Mbit/s


