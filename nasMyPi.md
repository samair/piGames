## What ?
The whole point is to create a Network Attached Storage using your RaspPi.
What you need essentially to take off this project is 

 1. Raspberry PI (A pre-configured one, accessible via ssh)
 2. A wireless or wired network (internet access required) where the pi and a device (you connect to pi with) are in together
 3. bit of a anxiety
 

## Why?
Essentially this could be done as a hobby or a small home solution for you home office.
You could make all the external drives accessible via wifi/network.

## How?
This feat would be achieved using no additional hardware. Just follow the below step and you would set it up in a matter of minutes.

 - Login to your pi, i do via ssh using some ssh terminal. I use putty via my windows laptop.
 - first install vim or any other editor you are comfortable with.
	 - `sudo apt-get install vim `
 - Now install samba, which happens to be in a nutshell a software that allows you to share files across Linux and windows
	 - `sudo apt-get install samba samba-common-bin`
- Now lets try to first share a local internal folder on to the network, for this create a new directory namely "INTERNAL"  ( can be anything)
	- `sudo vi /etc/samba/smb.conf`
	-  Add below lines to the end of the file, note you must open the file with root access.
	- `## What ?
The whole point is to create a Network Attached Storage using your RaspPi.
What you need essentially to take off this project is 

 1. Raspberry PI (A pre-configured one, accessible via ssh)
 2. A wireless or wired network (internet access required) where the pi and a device (you connect to pi with) are in together
 3. bit of a anxiety
 

## Why?
Essentially this could be done as a hobby or a small home solution for you home office.
You could make all the external drives accessible via wifi/network.

## How?
This feat would be achieved using no additional hardware. Just follow the below step and you would set it up in a matter of minutes.

 - Login to your pi, i do via ssh using some ssh terminal. I use putty via my windows laptop.
 - first install vim or any other editor you are comfortable with.
	 - `sudo apt-get install vim `
 - Now install samba, which happens to be in a nutshell a software that allows you to share files across Linux and windows
	 - `sudo apt-get install samba samba-common-bin`
- Now lets try to first share a local internal folder on to the network, for this create a new directory namely "INTERNAL"  ( can be anything)
	- `sudo vi /etc/samba/smb.conf`
	-	Add below lines to the end of the file, note you must open the file with root access.
	- `[INTERNAL]
    	   comment = internal Files
    	   browseable = yes
           path = /home/pi/INTERNAL
           writeable = Yes
           create mask = 0777
           directory mask = 0777
           browseable = Yes
           public = yes`
`


