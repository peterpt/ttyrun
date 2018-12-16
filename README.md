A simple tool to run commands on a different terminal
# Screenshot
<img src="https://i.postimg.cc/pd8q3ccX/nproj.jpg" width="55%"></img>

# How to run it
- You must find the tty of the terminal you want to run the command on
* example for metasploit framework :
- 1st run msfconsole
- 2nd then run the following command from another terminal 
* ps -aux |grep msfconsole | awk '{print$7}' | sed -n 1p

- in my case i got pts/0

to run a particular command from the current terminal to the msfconsole terminal just do it like this

* ./execute -n /dev/pts/0 show options

- where : 
- execute= is the current bin in this git 
- -n = new line after the command (this option simulates an enter after your text in other window
- show options = command to be execute on other terminal

## Original Code Source
http://www.humbug.in/2010/utility-to-send-commands-or-data-to-other-terminals-ttypts/

## Current files on this git

* execute.c = Source code
* execute = binary already compiled

