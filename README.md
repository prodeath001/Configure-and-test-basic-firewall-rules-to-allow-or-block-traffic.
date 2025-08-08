the above documents shows the command for quick fire wall configuration 

 Linux (UFW)

**Open & List Rules**
```
sudo ufw status verbose
sudo ufw enable
sudo ufw status numbered
```

Block Port 23 (Telnet)
```
Copy code
sudo ufw deny 23/tcp
```

Test
```
Copy code
sudo apt install netcat -y
nc -l -p 23   # in one terminal
telnet 127.0.0.1 23   # in another
```

Allow SSH
```
Copy code
sudo ufw allow 22/tcp
```

Remove Rule
```
sudo ufw delete deny 23/tcp
```

UFW: Frontend for iptables, default deny incoming, allow outgoing, rules by port/IP/protocol.
