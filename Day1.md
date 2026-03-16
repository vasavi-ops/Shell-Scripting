
Shell = A program that lets you communicate with the operating system using commands.
DevOps engineers rely heavily on the shell because it helps to:

Automate tasks using shell scripts

Manage Linux servers

Run CI/CD pipelines

Control tools like Docker, Kubernetes, and Git

Perform system administration quickly

what all the shells configured in linux server>----cat /etc/shells

check which shell we are using --echo $SHELL
switch to another shell --- /bin/csh

**debug:**
vi first.sh---shell script file 
set -x--- startting point 
anycommand: uptime
set x ---ending point


run all the commands in debug mode ---sh -x first.sh

Varibales:
 its used to store a value and its  a name of a memory location .
 rules:
 letters: a - z and A - Z
 digits: 0 to 9 
 underscore :  _
types:
system defined variables:
enc or printenv
user/programer defind variables
	age =78
	name = "sai"
==Command line arguments:==
program:1
reading the values from command line 
vi commandline.sh 

echo $0
echo $1
echo $2

run---sh commandline.sh one java
result:
commandline.sh
one 
java

program:2

vi commandline.sh 

echo $0
echo $13---->it will read 1 value from cli first then add 3 value beside to it 
echo $2
echo ${11}--->it will display the 11 th value
echo $#----> total no of arguments passed through script count display 
echo $@--->all arguments display in the order or in single line 
echo $@--->all arguments display in the order or in single line as a string
echo ---->display the process id 

run---sh commandline.sh 1234567891011
result:
commandline.sh
13
2
11
4

$?---previous command status 
0 is success 
127--fail
