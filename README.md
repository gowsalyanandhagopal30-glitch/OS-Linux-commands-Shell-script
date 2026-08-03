# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

```
Name:N.Gowsalya
Register NO:212225230085
```

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT

<img width="440" height="151" alt="Screenshot 2026-08-02 174114" src="https://github.com/user-attachments/assets/b9596d09-b7b9-42f4-9779-b3b131d149ce" />


cat < file2
## OUTPUT

<img width="387" height="172" alt="Screenshot 2026-08-02 174147" src="https://github.com/user-attachments/assets/25461dd4-d8ac-4d1b-82f7-9a91cebb9a2d" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="372" height="77" alt="Screenshot 2026-08-02 175610" src="https://github.com/user-attachments/assets/04e01e6d-8b50-45e7-ab87-924eacc5c038" />

 
comm file1 file2
 ## OUTPUT

<img width="390" height="228" alt="Screenshot 2026-08-02 175632" src="https://github.com/user-attachments/assets/8cb129a2-6ea8-4442-92f2-05e4c1a2bc9b" />

 
diff file1 file2
## OUTPUT

<img width="287" height="273" alt="Screenshot 2026-08-02 175732" src="https://github.com/user-attachments/assets/853ea00f-ab77-40e7-ae8c-0e18b85539a4" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

<img width="286" height="96" alt="Screenshot 2026-08-02 175836" src="https://github.com/user-attachments/assets/8143bfed-6c6e-495d-8674-d07390b1593a" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="343" height="127" alt="Screenshot 2026-08-02 175931" src="https://github.com/user-attachments/assets/441563a1-22ea-4377-af10-cd9f9111d317" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="351" height="128" alt="Screenshot 2026-08-02 175903" src="https://github.com/user-attachments/assets/416892e7-62e9-48ad-a417-a5bce066c7e0" />

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="262" height="75" alt="Screenshot 2026-08-02 180114" src="https://github.com/user-attachments/assets/b6bb73ba-7a60-4d98-8ac1-233ff56c847e" />


grep hello newfile 
## OUTPUT

<img width="1600" height="240" alt="image" src="https://github.com/user-attachments/assets/80a2013a-7214-4553-b5b9-be14a940ee9c" />



grep -v hello newfile 
## OUTPUT

<img width="293" height="76" alt="Screenshot 2026-08-02 180131" src="https://github.com/user-attachments/assets/10ab4810-450c-4685-8078-e81ab480bea8" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="365" height="102" alt="Screenshot 2026-08-02 180148" src="https://github.com/user-attachments/assets/b105a2b1-eabe-4316-a247-4a54140dcb3a" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="393" height="76" alt="Screenshot 2026-08-02 180203" src="https://github.com/user-attachments/assets/4ac3bca9-70f6-45d0-a6ac-ac65036da25a" />



grep -R ubuntu /etc
## OUTPUT

<img width="1133" height="817" alt="Screenshot 2026-08-02 181031" src="https://github.com/user-attachments/assets/2c327810-fefc-4451-880f-e1fd433512b4" />


grep -w -n world newfile   
## OUTPUT

<img width="340" height="96" alt="Screenshot 2026-08-02 180223" src="https://github.com/user-attachments/assets/02c4ea7c-c46a-4ef4-92f5-e29ae383954a" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="421" height="92" alt="Screenshot 2026-08-02 181237" src="https://github.com/user-attachments/assets/350b917b-eeb9-4a31-b3e9-a871ebf924dd" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="367" height="97" alt="Screenshot 2026-08-02 181253" src="https://github.com/user-attachments/assets/b8be09ec-e1e0-4710-8562-5fd40a412195" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="422" height="105" alt="Screenshot 2026-08-02 181301" src="https://github.com/user-attachments/assets/18a65853-3371-46cb-b15d-cb73d3f42b10" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="317" height="73" alt="Screenshot 2026-08-02 181328" src="https://github.com/user-attachments/assets/cf85f7e6-a9f0-489a-a1ae-e3e11f2c6cae" />


egrep '(world$)' newfile 
## OUTPUT

<img width="330" height="95" alt="Screenshot 2026-08-02 181453" src="https://github.com/user-attachments/assets/efc1c6f3-804b-4e6c-8431-2083d9786686" />


egrep '(World$)' newfile 
## OUTPUT

<img width="1600" height="164" alt="image" src="https://github.com/user-attachments/assets/05d72e07-1ce8-40e3-8ea9-4fdc8b836f51" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="407" height="127" alt="Screenshot 2026-08-02 181554" src="https://github.com/user-attachments/assets/7746a1f0-7543-44f3-ac2b-4faa81608fff" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="300" height="77" alt="Screenshot 2026-08-02 181611" src="https://github.com/user-attachments/assets/6fc17c55-85bb-45d4-b59e-83543a1344f1" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="388" height="72" alt="image" src="https://github.com/user-attachments/assets/7b77b85b-d1d4-4380-9dce-c089caf004ec" />



egrep 'Linux.*World' newfile 
## OUTPUT

<img width="1600" height="232" alt="WhatsApp Image 2026-08-03 at 6 36 14 AM" src="https://github.com/user-attachments/assets/32fcccb7-a382-4140-a953-ff56dfe4e22d" />


egrep l{2} newfile
## OUTPUT

<img width="310" height="101" alt="Screenshot 2026-08-02 181711" src="https://github.com/user-attachments/assets/f8d51e64-dbf9-4fb9-b135-ba3603b8c003" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="377" height="127" alt="Screenshot 2026-08-02 181726" src="https://github.com/user-attachments/assets/45b30935-7730-4052-9945-14de3e8ad24c" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT

<img width="288" height="72" alt="Screenshot 2026-08-02 192937" src="https://github.com/user-attachments/assets/828491c2-c4c9-40f4-b03e-41e37ab96b21" />


sed -n -e '$p' file23
## OUTPUT

<img width="306" height="77" alt="Screenshot 2026-08-02 192951" src="https://github.com/user-attachments/assets/a0ccdde8-2645-4626-b953-578e4b932792" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="377" height="251" alt="Screenshot 2026-08-02 193012" src="https://github.com/user-attachments/assets/bf14acd5-a8a3-4006-808c-91eac81121c5" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="401" height="251" alt="Screenshot 2026-08-02 193026" src="https://github.com/user-attachments/assets/255f3b70-1b90-48e6-aa43-532b306d8163" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="441" height="252" alt="Screenshot 2026-08-02 193050" src="https://github.com/user-attachments/assets/7ffe5de3-15fb-496c-8cf7-98dd6a6d70fb" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="345" height="177" alt="Screenshot 2026-08-02 193108" src="https://github.com/user-attachments/assets/5961432f-e173-4a17-8b7f-d5abf42f56cc" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="357" height="130" alt="Screenshot 2026-08-02 193123" src="https://github.com/user-attachments/assets/10f5560c-1050-4728-b3e3-0ac1ffc2091b" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="402" height="101" alt="Screenshot 2026-08-02 193142" src="https://github.com/user-attachments/assets/9676c142-65bd-475b-bce0-d2b5049ca01d" />


seq 10 
## OUTPUT

<img width="353" height="288" alt="Screenshot 2026-08-02 193203" src="https://github.com/user-attachments/assets/d210562f-fd09-4a02-9880-c75ca0cf29d9" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="353" height="127" alt="Screenshot 2026-08-02 193214" src="https://github.com/user-attachments/assets/1b32f839-9821-46c4-95ac-d4f25d425b51" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="333" height="125" alt="Screenshot 2026-08-02 193223" src="https://github.com/user-attachments/assets/bd9363a3-89ee-4548-84d1-3cea1dddfffd" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="298" height="147" alt="Screenshot 2026-08-02 193239" src="https://github.com/user-attachments/assets/185c5b35-3f55-4509-ac1b-7f54e2153104" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="295" height="123" alt="Screenshot 2026-08-02 193312" src="https://github.com/user-attachments/assets/28b3d3e2-2e5e-418a-b00d-34025ff6396d" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="322" height="121" alt="Screenshot 2026-08-02 193330" src="https://github.com/user-attachments/assets/0194fef0-dc16-4463-a4f2-db9ebebfbd29" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="367" height="127" alt="Screenshot 2026-08-02 193353" src="https://github.com/user-attachments/assets/d727e9e4-03df-4445-b24f-f12615ba7ffe" />



sed -n '2,4{s/$/*/;p}' file23


<img width="377" height="127" alt="Screenshot 2026-08-02 193414" src="https://github.com/user-attachments/assets/36bce7f3-f76f-4817-80ee-4fd072183793" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT

<img width="312" height="175" alt="Screenshot 2026-08-02 204255" src="https://github.com/user-attachments/assets/8a407034-76ba-433d-b911-e98a1350ba63" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

<img width="321" height="172" alt="Screenshot 2026-08-02 204320" src="https://github.com/user-attachments/assets/1ee8e8a1-e4e5-491c-b4d1-d67b1053259a" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="448" height="250" alt="Screenshot 2026-08-02 204334" src="https://github.com/user-attachments/assets/fa5e0474-beb2-492e-9d9c-4c7867c14985" />


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="346" height="121" alt="Screenshot 2026-08-02 204427" src="https://github.com/user-attachments/assets/60d93d73-6c46-4ae2-aa53-d3f597ec20f6" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="453" height="122" alt="Screenshot 2026-08-02 204442" src="https://github.com/user-attachments/assets/0bf0e011-7574-43c3-9e42-37f53803ce0f" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="1600" height="560" alt="image" src="https://github.com/user-attachments/assets/48d7258c-a065-4dd0-b76c-791dfac7f138" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1599" height="787" alt="image" src="https://github.com/user-attachments/assets/2e5cb13c-2d7e-42f3-b0e2-6cb15ab0eb47" />



tar -xvf backup.tar
## OUTPUT

<img width="1600" height="709" alt="image" src="https://github.com/user-attachments/assets/2310d537-e046-4c6e-a781-cf0508f3b377" />



gzip backup.tar

ls .gz
## OUTPUT

<img width="341" height="72" alt="Screenshot 2026-08-02 204528" src="https://github.com/user-attachments/assets/75279897-fa56-4da1-865d-bf6c658fff7b" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="1145" height="102" alt="Screenshot 2026-08-02 204634" src="https://github.com/user-attachments/assets/476eeee8-18c2-479a-b0b9-513403c2b243" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="1600" height="864" alt="image" src="https://github.com/user-attachments/assets/36ae4c37-307f-4e9a-96de-e591128e2987" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="1600" height="800" alt="image" src="https://github.com/user-attachments/assets/511978f0-9e0f-491d-ab9b-9af399aef8f7" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

<img width="1600" height="885" alt="image" src="https://github.com/user-attachments/assets/94e0f132-1747-4822-a717-64dcb9672c41" />

 
ls file1
## OUTPUT

<img width="1599" height="592" alt="image" src="https://github.com/user-attachments/assets/cf99a181-3d32-4cfe-8747-7387aeb430ae" />


echo $?
## OUTPUT 

<img width="1600" height="790" alt="image" src="https://github.com/user-attachments/assets/3d09ce36-b180-4f97-baae-f94fa787184a" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="1600" height="675" alt="image" src="https://github.com/user-attachments/assets/8b21b441-e422-4bbf-9580-22349046fc11" />


 
abcd
 
echo $?
 ## OUTPUT

<img width="1600" height="675" alt="image" src="https://github.com/user-attachments/assets/d0baeaa4-c268-4d56-94dd-2074cc6d3cd0" />

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT

<img width="1599" height="787" alt="image" src="https://github.com/user-attachments/assets/be441b9d-17d2-49c6-af01-a7c56fa4368a" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="1599" height="712" alt="image" src="https://github.com/user-attachments/assets/9ab3f283-ba4a-4f31-a2d2-e847886a3f2a" />


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

<img width="1700" height="306" alt="image" src="https://github.com/user-attachments/assets/c638d48d-ca23-4a0d-bdd1-aa939abaa6ec" />



# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

<img width="1476" height="441" alt="image" src="https://github.com/user-attachments/assets/cca65afa-4b2d-4271-a948-1bb9c3e9d669" />


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

<img width="1600" height="256" alt="image" src="https://github.com/user-attachments/assets/4f978a3e-5c6f-4363-bf0c-f5d9094975ce" />


# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

<img width="1475" height="397" alt="image" src="https://github.com/user-attachments/assets/b8c52b1f-3638-4ac3-a42f-c30075985498" />


# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT

<img width="1600" height="224" alt="WhatsApp Image 2026-08-03 at 7 13 04 AM" src="https://github.com/user-attachments/assets/665cc346-3673-4ffa-8e7c-0a9b746a8ccb" />

# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

<img width="1517" height="232" alt="image" src="https://github.com/user-attachments/assets/3a23fce4-4731-4918-ba54-6fd885ad656a" />


# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 

##output

<img width="1600" height="220" alt="image" src="https://github.com/user-attachments/assets/7344bef0-4b4f-4be1-9b07-8bd874175dfe" />


 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
## Output

<img width="1600" height="677" alt="WhatsApp Image 2026-08-03 at 7 41 17 AM" src="https://github.com/user-attachments/assets/2c4c28ff-9134-471a-b41e-649946f4be8a" />

 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 ./untiltest.sh

 ##Output

 <img width="1600" height="504" alt="WhatsApp Image 2026-08-03 at 7 44 01 AM" src="https://github.com/user-attachments/assets/39dd6d39-d37c-4bb8-aa75-252b05d7ee5d" />

 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
./forin1.sh 
##Output

 <img width="1600" height="755" alt="image" src="https://github.com/user-attachments/assets/2ffaef76-af33-42d4-bf78-2d3fc687aa8a" />

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
##Output

<img width="1600" height="657" alt="image" src="https://github.com/user-attachments/assets/2993575c-5bc2-4068-b68b-887cdb336b78" />

 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 

##OUTPUT

<img width="1600" height="833" alt="image" src="https://github.com/user-attachments/assets/8dd1bc8c-5526-44f9-b666-fb2798e083e8" />

 
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT

<img width="1600" height="816" alt="image" src="https://github.com/user-attachments/assets/bceb1fe2-017e-42b6-86c1-f720a2cb2e6d" />



cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

<img width="1600" height="552" alt="image" src="https://github.com/user-attachments/assets/0c626110-4108-4c5c-a404-ad6d5413559d" />


cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

<img width="1600" height="624" alt="image" src="https://github.com/user-attachments/assets/8ed7f436-5dfd-46ee-a400-cd908b16e630" />


cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

<img width="1600" height="775" alt="image" src="https://github.com/user-attachments/assets/227879c1-8557-4c22-af86-2d9679a8f9e5" />

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
$ ./forbreak.sh
##OUTPUT

<img width="1600" height="711" alt="image" src="https://github.com/user-attachments/assets/7508c608-1631-467d-9b09-fec6297c9d15" />

 cat forcontinue.sh
```bash
 #!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
$chmod 755 forcontinue.sh
$ ./forcontinue.sh 
## OUTPUT

<img width="1600" height="736" alt="image" src="https://github.com/user-attachments/assets/b137b5df-b631-433f-8414-09fd4e9fa0d0" />

 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT

<img width="1600" height="711" alt="image" src="https://github.com/user-attachments/assets/caba5ae9-1b7e-4e92-ba22-584477683439" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="1600" height="684" alt="image" src="https://github.com/user-attachments/assets/bf0ccf9a-91ff-4a4f-806c-30abbf517a96" />


$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

<img width="1280" height="137" alt="image" src="https://github.com/user-attachments/assets/55a9db6d-473a-48f5-92b1-a677a09c801e" />

 
 ./funcex.sh 1 2

 <img width="1280" height="169" alt="image" src="https://github.com/user-attachments/assets/85f538b7-779c-494b-a507-db4d312eaa20" />


 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3

<img width="1599" height="810" alt="image" src="https://github.com/user-attachments/assets/4ae8cb36-0aac-4867-8086-5a15a1a30271" />

 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3

<img width="1600" height="320" alt="image" src="https://github.com/user-attachments/assets/da8a6655-e466-472e-83b5-1c1dc2800398" />

 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3

 <img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/3da9fc17-4fc6-4b1b-b912-91616e4e7472" />

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 

<img width="1600" height="845" alt="image" src="https://github.com/user-attachments/assets/e49eb796-1f53-4ae6-96f1-1fd0cd0116f7" />

 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 

<img width="1600" height="743" alt="image" src="https://github.com/user-attachments/assets/18dbb967-2c3a-4d4c-a55a-98561a11362b" />


# RESULT:
The Commands are executed successfully.
