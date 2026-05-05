# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

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
<img width="359" height="160" alt="Screenshot 2026-04-20 141154" src="https://github.com/user-attachments/assets/f42c3f70-4a56-4da4-bfb6-c28efea3edd2" />

cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
<img width="355" height="153" alt="Screenshot 2026-04-20 141209" src="https://github.com/user-attachments/assets/276dbb91-6d6e-4af0-9da5-5cf9b159e161" />

### Display the content of the files
cat < file1
## OUTPUT



cat < file2
## OUTPUt


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="377" height="39" alt="Screenshot 2026-04-20 141457" src="https://github.com/user-attachments/assets/7ef7d127-4d92-4f37-b22e-fcd331535cb7" />
  

comm file1 file2
 ## OUTPUT

 
diff file1 file2
## OUTPUT
<img width="377" height="39" alt="Screenshot 2026-04-20 141457" src="https://github.com/user-attachments/assets/b82e83e8-ec6b-4469-bb0d-746dcf186894" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```

<img width="350" height="71" alt="Screenshot 2026-04-20 141726" src="https://github.com/user-attachments/assets/667f4659-5739-4c97-8c9d-a83a49fe525a" />


cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```

<img width="348" height="95" alt="Screenshot 2026-04-20 141821" src="https://github.com/user-attachments/assets/60b63487-94df-4e15-b808-81584b73bff5" />


cut -c1-3 file11
## OUTPUT


<img width="404" height="64" alt="Screenshot 2026-04-20 141922" src="https://github.com/user-attachments/assets/bc1eabf1-c905-43c7-a73d-6d5572229f00" />



cut -d "|" -f 1 file22
## OUTPUT


<img width="471" height="91" alt="Screenshot 2026-04-20 141952" src="https://github.com/user-attachments/assets/03f811be-9837-41c1-9f1c-7f0f7d98bc40" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="454" height="84" alt="Screenshot 2026-04-20 142122" src="https://github.com/user-attachments/assets/ec3c4ee2-dd2d-41df-ab32-1e986ef70e8b" />


cat < newfile 
```
Hello world
hello world
^d
````

<img width="364" height="69" alt="Screenshot 2026-04-20 142256" src="https://github.com/user-attachments/assets/7419b8a3-0b50-45d1-afa0-74391198b7aa" />

cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT


<img width="417" height="42" alt="Screenshot 2026-04-20 142330" src="https://github.com/user-attachments/assets/a8e76a7e-969c-46b9-97c1-eda1e205176c" />


grep -v hello newfile 
## OUTPUT


<img width="453" height="52" alt="Screenshot 2026-04-20 142357" src="https://github.com/user-attachments/assets/76cb11be-ce6e-4676-b128-dc5087d285a1" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="519" height="69" alt="Screenshot 2026-04-20 142424" src="https://github.com/user-attachments/assets/ebd32863-f3c6-42f2-9826-325495e54973" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="551" height="38" alt="Screenshot 2026-04-20 142453" src="https://github.com/user-attachments/assets/92fae105-4e4a-4656-8967-7920cc6c4b86" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

<img width="492" height="62" alt="Screenshot 2026-04-20 143621" src="https://github.com/user-attachments/assets/2419a0fb-c0c3-45f2-9403-f5fd8f9f8610" />


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

<img width="535" height="68" alt="Screenshot 2026-04-20 143901" src="https://github.com/user-attachments/assets/31158ead-34d3-46fd-98cc-742c14af5346" />



egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="526" height="63" alt="Screenshot 2026-04-20 143927" src="https://github.com/user-attachments/assets/ff4d5ed3-9fff-4020-bcc2-4c989cfe5f78" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="579" height="57" alt="Screenshot 2026-04-20 144004" src="https://github.com/user-attachments/assets/1cb9b888-64d9-4b5e-af92-212853021f7f" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="579" height="57" alt="Screenshot 2026-04-20 144004" src="https://github.com/user-attachments/assets/e0b94f88-e896-4488-8ed1-e7dc0de00f8d" />


egrep '(world$)' newfile 
## OUTPUT

<img width="579" height="57" alt="Screenshot 2026-04-20 144004" src="https://github.com/user-attachments/assets/c4e20751-e6b2-4f47-9e01-f578f8390f10" />



egrep '(World$)' newfile 
## OUTPUT


<img width="579" height="57" alt="Screenshot 2026-04-20 144004" src="https://github.com/user-attachments/assets/eb0590b4-f5bc-4580-a62b-1a82af236ab9" />

egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="541" height="93" alt="Screenshot 2026-04-20 144225" src="https://github.com/user-attachments/assets/456f72b7-e02f-4949-984f-3338de684729" />


egrep '[1-9]' newfile 
## OUTPUT


<img width="453" height="46" alt="Screenshot 2026-04-20 144251" src="https://github.com/user-attachments/assets/b022e4ec-2556-428a-a3e3-5f2c8acf41a1" />


egrep 'Linux.*world' newfile 
## OUTPUT


<img width="535" height="44" alt="Screenshot 2026-04-20 144317" src="https://github.com/user-attachments/assets/4965ae36-f565-423a-bb5a-d412f022b77f" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="524" height="44" alt="Screenshot 2026-04-20 144426" src="https://github.com/user-attachments/assets/18cb6d5c-6a70-4c7b-9911-bb2d1c66eb2b" />


egrep l{2} newfile
## OUTPUT

<img width="434" height="64" alt="Screenshot 2026-04-20 144457" src="https://github.com/user-attachments/assets/c348a8cf-56f8-425c-83f9-7e2cec72a8a6" />



egrep 's{1,2}' newfile
## OUTPUT 


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

<img width="442" height="192" alt="Screenshot 2026-05-05 093733" src="https://github.com/user-attachments/assets/7ed2b92b-0fd7-4b8d-bc16-c482d80e0c0b" />



sed -n -e '3p' file23
## OUTPUT


<img width="443" height="32" alt="Screenshot 2026-05-05 093741" src="https://github.com/user-attachments/assets/5ea75af9-5786-43ca-b064-8b45ede83f46" />


sed -n -e '$p' file23
## OUTPUT


<img width="444" height="46" alt="Screenshot 2026-05-05 093811" src="https://github.com/user-attachments/assets/896b0531-37d7-4b3a-b8d4-e7b05e4a3a29" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="523" height="202" alt="Screenshot 2026-05-05 093837" src="https://github.com/user-attachments/assets/4f043517-31c6-4f5e-b0ba-f70d1b36d18a" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="518" height="191" alt="Screenshot 2026-05-05 093855" src="https://github.com/user-attachments/assets/88bb9a2e-3b1b-459c-bac9-8b3e7592c452" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="572" height="197" alt="Screenshot 2026-05-05 093920" src="https://github.com/user-attachments/assets/f2690413-6c24-41ae-b33c-ce68ac03bf0a" />



sed -n -e '1,5p' file23
## OUTPUT


<img width="495" height="130" alt="Screenshot 2026-05-05 093939" src="https://github.com/user-attachments/assets/36de8bf5-ffcd-4b91-9405-be5081bf2acb" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="531" height="95" alt="Screenshot 2026-05-05 094018" src="https://github.com/user-attachments/assets/71d0f1c0-17d5-4640-93ae-c4071ae1169f" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="540" height="68" alt="Screenshot 2026-05-05 094035" src="https://github.com/user-attachments/assets/c8ae002b-7f9d-4ff6-ba7b-2bd1352b0a1f" />


seq 10 
## OUTPUT


<img width="378" height="247" alt="Screenshot 2026-05-05 094054" src="https://github.com/user-attachments/assets/82c11f74-b54b-4c31-b6c5-7ea35995d108" />


seq 10 | sed -n '4,6p'
## OUTPUT


<img width="458" height="90" alt="Screenshot 2026-05-05 094116" src="https://github.com/user-attachments/assets/61e96742-a41b-487f-a602-ecb006951745" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="519" height="90" alt="Screenshot 2026-05-05 094223" src="https://github.com/user-attachments/assets/a1aae45c-f956-410d-8d48-6aeb0416465d" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="494" height="114" alt="Screenshot 2026-05-05 094239" src="https://github.com/user-attachments/assets/218a6fd2-3b42-4967-b50e-c04159af4ca2" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="470" height="83" alt="Screenshot 2026-05-05 094259" src="https://github.com/user-attachments/assets/4b9f260b-026c-4ae0-91a5-da5e5c127ffa" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="546" height="92" alt="Screenshot 2026-05-05 094317" src="https://github.com/user-attachments/assets/bfd14c22-02af-4d10-86d2-a32f7230c822" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="582" height="91" alt="Screenshot 2026-05-05 094335" src="https://github.com/user-attachments/assets/986c2338-21b6-4343-9974-7731b569f404" />


sed -n '2,4{s/$/*/;p}' file23

<img width="537" height="93" alt="Screenshot 2026-05-05 094352" src="https://github.com/user-attachments/assets/ee4b57f1-c3c6-4c50-9c0f-2afeba03f80b" />


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

<img width="393" height="153" alt="Screenshot 2026-05-05 094448" src="https://github.com/user-attachments/assets/dad61d47-4667-4a83-9d65-e472dc29d791" />


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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="624" height="189" alt="Screenshot 2026-05-05 094524" src="https://github.com/user-attachments/assets/dcf8a423-bb4d-47f4-a338-6a0bcc284e28" />

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

<img width="419" height="88" alt="Screenshot 2026-05-05 094612" src="https://github.com/user-attachments/assets/34eb249a-b886-456d-a468-eaee73a83924" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="649" height="88" alt="Screenshot 2026-05-05 094634" src="https://github.com/user-attachments/assets/22a8f7a2-1a59-4300-b637-0aac8760da73" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="556" height="68" alt="Screenshot 2026-05-05 101525" src="https://github.com/user-attachments/assets/320b9f6a-4e64-42d4-8d4e-0088acec0a16" />


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT

 <img width="663" height="69" alt="Screenshot 2026-05-05 101902" src="https://github.com/user-attachments/assets/8366cc8d-d04d-459b-a1c9-27f8aec0d65d" />

gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```



cat herecheck.txt
## OUTPUT

<img width="476" height="118" alt="Screenshot 2026-05-05 101942" src="https://github.com/user-attachments/assets/7f71cf49-d2a5-4ba1-b44d-693f346afb1c" />


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

<img width="302" height="73" alt="Screenshot 2026-05-05 101847" src="https://github.com/user-attachments/assets/3ed6968d-c7a5-444c-bf30-61d4df21c928" />

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

 <img width="373" height="259" alt="Screenshot 2026-05-05 102047" src="https://github.com/user-attachments/assets/8523a3a2-4e52-4bdb-9a1d-2e5caa51ef0e" />

chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 
ls file1
## OUTPUT

echo $?

<img width="336" height="85" alt="Screenshot 2026-05-05 102253" src="https://github.com/user-attachments/assets/9faddc7c-fa18-43fe-82bb-9423f1a3e53c" />

## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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

<img width="471" height="221" alt="Screenshot 2026-05-05 102358" src="https://github.com/user-attachments/assets/8908caf2-b0c7-4785-bcf5-f0042b37e8d8" />

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

<img width="462" height="253" alt="Screenshot 2026-05-05 102406" src="https://github.com/user-attachments/assets/e204b1c0-b692-4117-ab8a-293d123fd385" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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

<img width="632" height="177" alt="Screenshot 2026-05-05 102553" src="https://github.com/user-attachments/assets/bac99b46-b66c-4fc6-9e0f-3725351ac571" />

<img width="628" height="198" alt="Screenshot 2026-05-05 102602" src="https://github.com/user-attachments/assets/608d0d47-7f38-46c2-8e86-4994dea82f36" />

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

<img width="514" height="396" alt="Screenshot 2026-05-05 102637" src="https://github.com/user-attachments/assets/1756f42d-fd60-4d0d-ab93-924f029b72da" />

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

<img width="553" height="399" alt="Screenshot 2026-05-05 102703" src="https://github.com/user-attachments/assets/2a57272c-7561-4ea1-83fd-d8771d823a95" />

./ifnested.sh 
## OUTPUT



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

<img width="492" height="308" alt="Screenshot 2026-05-05 102732" src="https://github.com/user-attachments/assets/4231a54c-482a-4097-8888-f37d55a352b0" />


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

<img width="513" height="308" alt="Screenshot 2026-05-05 102813" src="https://github.com/user-attachments/assets/7cc12c6f-02fa-4459-bef8-27705780f8bd" />

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

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

<img width="620" height="403" alt="Screenshot 2026-05-05 102845" src="https://github.com/user-attachments/assets/13b93686-3129-473e-9d34-e83192fe8424" />

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

<img width="574" height="398" alt="Screenshot 2026-05-05 102906" src="https://github.com/user-attachments/assets/223b6b34-f51a-4f3d-8025-5733969f45ee" />

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

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

<img width="613" height="420" alt="Screenshot 2026-05-05 102952" src="https://github.com/user-attachments/assets/7c54dac7-70da-4bf4-9d26-11414b821731" />

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


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

<img width="492" height="197" alt="Screenshot 2026-05-05 103040" src="https://github.com/user-attachments/assets/62c99762-1e93-47fd-b974-e8c87b81299f" />

$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

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

<img width="619" height="271" alt="Screenshot 2026-05-05 103105" src="https://github.com/user-attachments/assets/122c42db-e1d8-47cf-9baf-1760b55adba6" />

$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
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

<img width="499" height="199" alt="Screenshot 2026-05-05 103137" src="https://github.com/user-attachments/assets/5cc3e7c0-1329-4b33-90b4-85ca9e29f9a8" />

$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
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

<img width="485" height="185" alt="Screenshot 2026-05-05 103218" src="https://github.com/user-attachments/assets/fef1a7c8-afa5-4dc6-b6b9-b04121a55261" />

$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```

 <img width="670" height="192" alt="Screenshot 2026-05-05 103258" src="https://github.com/user-attachments/assets/7bb1412c-f43c-4ec6-9c20-c12c546f3cff" />

$ chmod 755 forin1.sh
 
 
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

<img width="594" height="159" alt="Screenshot 2026-05-05 103351" src="https://github.com/user-attachments/assets/dab59076-175e-4653-8249-07b8a0064a32" />

<img width="553" height="155" alt="Screenshot 2026-05-05 103417" src="https://github.com/user-attachments/assets/a5711a16-7ab8-4d35-aee2-5404ccd43e6d" />

$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```

<img width="609" height="157" alt="Screenshot 2026-05-05 103456" src="https://github.com/user-attachments/assets/3680a198-881f-4fbf-bb0d-c2d37dfcde05" />

$ ./forin3.sh 
 
cat forin1.sh 

<img width="666" height="156" alt="Screenshot 2026-05-05 103518" src="https://github.com/user-attachments/assets/684c96ef-b5af-48be-9c45-b6f17f866ceb" />

```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
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

<img width="520" height="181" alt="Screenshot 2026-05-05 103646" src="https://github.com/user-attachments/assets/6d83a8b4-c6fb-424e-adbf-f466dc09b524" />

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


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````

<img width="433" height="161" alt="Screenshot 2026-05-05 103857" src="https://github.com/user-attachments/assets/1bdc0d16-65bc-4653-8345-913857d4ddd3" />

$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```

<img width="493" height="156" alt="Screenshot 2026-05-05 103929" src="https://github.com/user-attachments/assets/2f802c1b-64e5-41e3-8d9f-9b5b1a8a2b96" />

$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

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

<img width="463" height="249" alt="Screenshot 2026-05-05 104002" src="https://github.com/user-attachments/assets/9f498efe-af57-4870-a955-fdbcbb17bd77" />

$ chmod 755 fornested1.sh

 <img width="662" height="313" alt="Screenshot 2026-05-05 104622" src="https://github.com/user-attachments/assets/01e9b6be-7e5f-4225-aa5e-ba2c599cd888" />

$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

<img width="461" height="267" alt="Screenshot 2026-05-05 104043" src="https://github.com/user-attachments/assets/10867175-1a4c-4236-ad2a-fc172b708399" />

## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
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

<img width="459" height="262" alt="Screenshot 2026-05-05 104109" src="https://github.com/user-attachments/assets/21a386c6-8f7b-46dd-bdf4-3cb72a8fa05c" />

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```

 <img width="480" height="136" alt="Screenshot 2026-05-05 104144" src="https://github.com/user-attachments/assets/b8b4443f-ed25-44b6-8525-2b2f85429878" />

$ chmod 755 exread.sh 

<img width="477" height="92" alt="Screenshot 2026-05-05 104442" src="https://github.com/user-attachments/assets/2f0a565b-c50e-429f-9f3d-c2451cd8356c" />
 
$ ./exread.sh 

<img width="433" height="111" alt="Screenshot 2026-05-05 104532" src="https://github.com/user-attachments/assets/a8042950-27f8-4749-99b0-1eccc982e779" />

## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
```

<img width="579" height="111" alt="Screenshot 2026-05-05 104223" src="https://github.com/user-attachments/assets/46e696af-3ecc-44c3-9cc3-75eb1c2765db" />
 
$ chmod 755 exread1.sh 

## OUTPUT



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

<img width="643" height="286" alt="Screenshot 2026-05-05 104735" src="https://github.com/user-attachments/assets/82736c23-665c-4aa4-a568-3b8058c30fe0" />

## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

<img width="571" height="250" alt="Screenshot 2026-05-05 104849" src="https://github.com/user-attachments/assets/92e6e7cc-600c-4e7e-9cff-5dc984cc31df" />

## OUTPUT
$ ./argshift.sh 1 2 3

<img width="543" height="94" alt="Screenshot 2026-05-05 104918" src="https://github.com/user-attachments/assets/cf230504-4885-41d9-aa3e-12dba1501cb8" />
 
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

<img width="433" height="184" alt="Screenshot 2026-05-05 105018" src="https://github.com/user-attachments/assets/7a4c01e5-b422-44aa-b93f-91bb1f4599df" />

$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
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

 <img width="502" height="326" alt="Screenshot 2026-05-05 105038" src="https://github.com/user-attachments/assets/89ba60ec-c1fd-4265-bec7-d5896d81258e" />

 
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

<img width="442" height="269" alt="Screenshot 2026-05-05 105149" src="https://github.com/user-attachments/assets/ad15b4d7-e435-4c9a-9eb7-6ec6f643d37e" />

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

<img width="414" height="246" alt="Screenshot 2026-05-05 105127" src="https://github.com/user-attachments/assets/c9c048c4-c06e-4533-ae0b-73f9cc356c7e" />

awk -f nc.awk data.dat
## OUTPUT 
 
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


# RESULT:
The Commands are executed successfully.
