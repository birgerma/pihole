
# Original dns server:
DNS1: 103.86.96.100
DNS2: 103.86.99.100

Check used ports: sudo lsof -i -P -n | grep LISTEN

Stop local dns from using port 53:

sudo nano /etc/systemd/resolved.conf
andchange
#DNSStubListener=yes to DNSStubListener=no (make sure you uncomment the line).

$ sudo service systemd-resolved restart