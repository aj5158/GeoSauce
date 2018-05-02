# GeoSauce
GeoMap Source IP from Cisco syslog

eg
Cisco
Apr 30 06:31:27.798: %SEC-6-IPACCESSLOGNP: list 1 denied 0 180.97.106.163 -> 0.0.0.0, 1 packet  
logging host 192.168.1.localmachine

Local Machine
Local7 is the Cisco logging default
 /etc/syslog.conf
 local7.debug /usr/adm/logs/cisco.log

touch /var/log/cisco.log
chmod 666 /var/log/cisco.log
kill -HUP `cat /etc/syslog.pid`

using var/log/cisco.log, continual parse for new IP's denied
