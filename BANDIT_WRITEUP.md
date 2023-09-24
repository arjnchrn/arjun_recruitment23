#**Bandit Level 0**

SSHed into bandit0 level using the command ssh bandit0@bandit.labs.overthewire.org -p 2220
Used the ls command and found readme file
Used cat command to reveal the password for next level NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL



#**Bandit Level 1**

SSHed into bandit1 
Found file named “-”
Used command cat < - to read contents of file with hyphenated name
Found password rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi



#**Bandit Level 2**
Spaces in file name
cat spaces\ in\ this\ filename 
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG



#**Bandit Level 3**
Cd inhere
Ls -a
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe



#**Bandit Level 4**

Command file ./-file* to list data types of all files in the directory
Found file07 as ASCII text
Pass lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR


#**Bandit Level 5**

Used command find -type f -size 1033c to find files with 1033 bytes

P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
-type f ⇒ files
-type d ⇒ directories 
etc



#**Bandit Level 6**
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password



#**Bandit 7**

Cat data.txt | grep millionth
TESKZC0XvTetK0S9xNwm25STk5iWrBvP



#**Bandit level 8** 

Sort data.txt | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t



#**Bandit level 9**

cat data.txt | grep "=="
grep: (standard input): binary file matches
bandit9@bandit:~$ strings data.txt | grep "=="
4========== the#
========== password
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

#**Bandit Level 10**

echo VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg== | base64 --decode
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM



#**Bandit Level 11**

echo "Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv



#**Bandit Level 12**

Annoying level with more compressions than necessary. Created a tmp folder with the name arjnchrn mkdir /tmp/arjnchrn and worked on it. Copied data.txt from home folder to here with “cp    ~/data.txt .”

Used file command to find out the compression method (bzip2, gzip and tar)

strings data8
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw  



#**Bandit Level 13**


SSH’ed into bandit13
Ls revealed sshkey.private (private key for bandit14 server)
SSHed into bandit14 without saving the private key to my machine by doing it directly from bandit13

Ssh -i sshkey.private bandit14@localhost -p 2220

Gained access to level 14

OR

Cat and copy contents of sshkey.private to local machine. Change permissions using chmod 700 and SSH into bandit 14



#**Bandit Level 14**

Found password for previous level with cat /etc/bandit_pass/bandit14 fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt (Password for level 15)



#**Bandit Level 15**

SSHed into bandit15 using password 
Man s_client
Openssl s_client -connect localhost:30001

Paste password to last level

jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1



#**Bandit Level 16**

SSH into bandit16
nmap -sV -p 31000-32000 localhost

-sV to display service version
p 31000-32000 defines port range to be scanned

PORT  	STATE SERVICE 	VERSION
31046/tcp open  echo
31518/tcp open  ssl/echo
31691/tcp open  echo
31790/tcp open  ssl/unknown
31960/tcp open  echo


Port 31518 only returns what we send
Port 31790 returned password

-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEdJpBZjANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwOTExMTQwMzI4WhcNMjMwOTExMTQwNDI4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCz
t2HtVeOTl4STW1YqPDHxE+S+IlxEQOnZwlt/gwPfAyhCZTbf9041Xr0yqfSAFXDO
kBsQYwWixjvmcHzlsi2ugHPIHQwoiQOUI6C+zLljBQRDvmKtD25YnEqd80hCSPL8
ue9ZXL8M9s2JkrurLUvl5VIVy/y0S6W+WrA3k8/z89DqCG1paIVOii8eAfVtze/z
S6aFQOEO9vlkwlwE7MDpDNgeZfKDHKQOwjubmqaQIc3YLuVF8kS4Jjiyoa2Cb0SM
rDsE1Cc86l8AIc64CcoDOvgG+aFAdPPuNlnY1PwN4tqML4e5zVTmZcuwWi/Dq9YA
yeXj9TmxI+zBKuuGvuxnAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBk
gfen2jyJ76fk8h9v3Uxh9eo8e5P8bhbQID191DGUxwDjLlsu1NbuL7amuuZQEnJw
+F/nQaLuNT3L90g0xRX7mL4nFmc5Vt3KdzeCwuxJ+26+Zi+3b6sJItV2Te07dpeW
qd11kkWSGcgGum67IUFIg1Ev+ne6N3rlgKaH38t8XDANRFYArUllO5++b6gth1BM
+TOUBHeL2G/WoWdA8oACGTSuI2ILj+sceAn3D4GCS1YsZ0aHXT9Dpfm/Wx3/+wGC
2dHqfIxB/Vws7TnfYpvQNwhibygjm3D80y2GIMoL7NEKu7cssK85xeODGURbYgml
UHz8d3Lr2Tt8/DwE0eFV
-----END CERTIFICATE-----

Saved to a bandit16 folder as sshkey.private and logged into bandit17 with ssh -i sshkey.private bandit17@bandit.labs.overthewire.org -p 2220



#**Bandit Level 17**

Ls showed password.new and old

Diff password.new password.old
< hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
---
> glZreTEH1V3cGKL6g4conYqZqaEj0mte


hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg belongs to password.net therefore its the password to level 18



#**Bandit Level 18**

ssh bandit18@bandit.labs.overthewire.org -p 2220 closes the connection as bash has been modified to automatically log out while using ssh

Find other shells with cat /etc/shells

cat /etc/shells
# /etc/shells: valid login shells
/bin/sh
/bin/bash
/usr/bin/bash
/bin/rbash
/usr/bin/rbash
/usr/bin/sh
/bin/dash
/usr/bin/dash

Using sh shell
ssh bandit18@bandit.labs.overthewire.org -p 2220 -t "/bin/sh"
Not logged out automatically 
Ls reveals readme file

cat readme
awhqfNnAbc1naukrpqDYcF95h7HoMTrC


#**Bandit Level 19**

SSHed into bandit19 
/bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT


#**Bandit Level 20**

SSH into bandit 20 
Setup a server for suconnect to connect to using 

Nc -l -p (random port number i chose 43000)

Run suconnect and connect to port 43000 in another terminal tab
./suconnect 43000

Input bandit20 password into the nc server
nc -l -p 43000
VxCazJaVykI6W36BkBU0mJTCM8rR95XT

Returns

NvEJF7oVjkddltPSrdKEFOllh9V1IBcq (pass for 21)

#**Bandit Level 21**

Access /etc/cron.d/ 
file cronjob_bandit22 reveals it to be an ASCII text
Cat cronjob_bandit22

@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null

Cat /usr/bin/cronjob_bandit22.sh to see what it does
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv

writes bandit 22 password to temp folder with permissions for users to read and write the ASCII text
cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv returns
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff (password for 22)


#**Bandit Level 22**

SSH into bandit22
Cd /etc/cron.d
cat cronjob_bandit23 (To find pass to next level)

Returns 
@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null

Runs script bandit23.sh
Cat bandit23.sh to find what the script does

#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget

Value of variable myname will be bandit23 since whoami command displays current user

Value of mytarget can be found by running the command echo I am user $myname | md5sum | cut -d ' ' -f 1 by switching up $myname with bandit23
Running this command will create a text file with bandit23 password and save it to /tmp in a file with its name given by an md5 hash of the string I am user bandit23 

cat /tmp/8ca319486bfbbc3663ea0fbe81326349
returns
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G (Password for next level)
