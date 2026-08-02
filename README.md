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
<img width="638" height="93" alt="001" src="https://github.com/user-attachments/assets/1e99ddab-0d97-4e87-bf98-8fb1611d4b21" />

cat < file2
## OUTPUT
<img width="610" height="108" alt="Screenshot 2026-08-02 at 13 29 31" src="https://github.com/user-attachments/assets/1b6e7e48-2c6a-4a87-8cd6-7d76d7cadef3" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="630" height="52" alt="Screenshot 2026-08-02 at 13 31 09" src="https://github.com/user-attachments/assets/baa21619-2812-4115-974c-fcc99713c262" />

comm file1 file2
 ## OUTPUT
<img width="619" height="185" alt="Screenshot 2026-08-02 at 13 31 37" src="https://github.com/user-attachments/assets/976aa73d-bc0e-450a-81ed-6a29795b7fc0" />

 
diff file1 file2
## OUTPUT
<img width="610" height="173" alt="diff file1 file2" src="https://github.com/user-attachments/assets/e9184c9d-b2ca-408a-a10a-d03da74fd595" />


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


<img width="591" height="51" alt="cut -c1-3 file11" src="https://github.com/user-attachments/assets/b8831a81-3042-41b2-b385-9cf7f535b29e" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="624" height="75" alt="Screenshot 2026-08-02 at 13 41 15" src="https://github.com/user-attachments/assets/e65e1486-a2a6-44c3-9684-e3458117882a" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="591" height="79" alt="Screenshot 2026-08-02 at 13 41 52" src="https://github.com/user-attachments/assets/4420072c-0b62-4647-820f-6cb3b631cc13" />


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

<img width="604" height="51" alt="Screenshot 2026-08-02 at 13 53 43" src="https://github.com/user-attachments/assets/afdd5b7b-4b0f-4af0-ac08-560b6a507316" />


grep hello newfile 
## OUTPUT


<img width="617" height="46" alt="Screenshot 2026-08-02 at 13 54 07" src="https://github.com/user-attachments/assets/6e1272d4-cef3-4e80-a6de-736f5b825f05" />


grep -v hello newfile 
## OUTPUT

<img width="638" height="46" alt="Screenshot 2026-08-02 at 13 54 33" src="https://github.com/user-attachments/assets/bfd19f1f-8c30-4daf-90b9-8f773f8daf09" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="613" height="64" alt="Screenshot 2026-08-02 at 13 55 01" src="https://github.com/user-attachments/assets/9b898651-5cb5-4645-9c77-aa1a3475ff72" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="659" height="47" alt="Screenshot 2026-08-02 at 13 55 26" src="https://github.com/user-attachments/assets/e7972915-3441-4e83-bdf2-8100fa5ba029" />



grep -R ubuntu /etc
## OUTPUT

<img width="1128" height="335" alt="Screenshot 2026-08-02 at 13 56 12" src="https://github.com/user-attachments/assets/2c95ffc1-fa6c-476a-ae0a-9a14f0c6ce57" />



grep -w -n world newfile   
## OUTPUT
<img width="599" height="60" alt="Screenshot 2026-08-02 at 14 00 22" src="https://github.com/user-attachments/assets/6f1d18f5-2874-4a71-953f-83bd9610742d" />


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

<img width="620" height="64" alt="Screenshot 2026-08-02 at 14 05 40" src="https://github.com/user-attachments/assets/d86e19e8-f2af-497e-bc70-7d5a9ba79598" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="604" height="66" alt="Screenshot 2026-08-02 at 14 06 07" src="https://github.com/user-attachments/assets/c95cb10e-9560-4a20-9351-1d5ce639d7cc" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="609" height="59" alt="Screenshot 2026-08-02 at 14 06 29" src="https://github.com/user-attachments/assets/7dce8ed9-a846-4f6b-a7b6-e498e49d914a" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="600" height="43" alt="Screenshot 2026-08-02 at 14 06 51" src="https://github.com/user-attachments/assets/1af60b97-bcf2-47f7-84ec-e04545353494" />


egrep '(world$)' newfile 
## OUTPUT

<img width="617" height="59" alt="Screenshot 2026-08-02 at 14 07 23" src="https://github.com/user-attachments/assets/02c01305-6f60-4687-85ad-2575cbf6ebf9" />


egrep '(World$)' newfile 
## OUTPUT

<img width="616" height="44" alt="Screenshot 2026-08-02 at 14 08 04" src="https://github.com/user-attachments/assets/4b0d7382-ef8a-44b8-a73d-0e2a8776ed73" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="624" height="77" alt="Screenshot 2026-08-02 at 14 08 43" src="https://github.com/user-attachments/assets/5bb54625-017a-4942-9ac3-3379842ab4b1" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="628" height="46" alt="Screenshot 2026-08-02 at 14 09 34" src="https://github.com/user-attachments/assets/06b826d4-406e-4ca2-8601-9112b60dcab7" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="595" height="44" alt="Screenshot 2026-08-02 at 14 10 05" src="https://github.com/user-attachments/assets/37aa1482-6ae7-4544-862e-871aba409f12" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="595" height="44" alt="Screenshot 2026-08-02 at 14 10 05" src="https://github.com/user-attachments/assets/4cb26270-1fc7-4e24-96d4-33f954f6065d" />

egrep l{2} newfile
## OUTPUT

<img width="630" height="61" alt="Screenshot 2026-08-02 at 14 10 36" src="https://github.com/user-attachments/assets/14f474ca-50f8-4ed3-97a1-fdb82801b767" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="588" height="80" alt="Screenshot 2026-08-02 at 14 11 32" src="https://github.com/user-attachments/assets/16a476ad-8095-49d1-9b59-5892ecff6243" />

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

<img width="619" height="46" alt="Screenshot 2026-08-02 at 14 46 30" src="https://github.com/user-attachments/assets/a011836f-96cd-4a3e-9982-1efa92d9c82e" />


sed -n -e '$p' file23
## OUTPUT

<img width="650" height="48" alt="Screenshot 2026-08-02 at 14 46 56" src="https://github.com/user-attachments/assets/5344097c-fcb5-4593-bb13-4da150b4334d" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="610" height="154" alt="Screenshot 2026-08-02 at 14 47 16" src="https://github.com/user-attachments/assets/a4faa2a8-6a4c-4579-ab4e-ee2c243af718" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="630" height="152" alt="Screenshot 2026-08-02 at 14 47 39" src="https://github.com/user-attachments/assets/17d2d785-b721-4a32-828d-cdeb6ce24a5e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="627" height="149" alt="Screenshot 2026-08-02 at 14 49 18" src="https://github.com/user-attachments/assets/b22cb71d-77d1-4dba-83fd-1343b2944c3d" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="610" height="104" alt="Screenshot 2026-08-02 at 14 49 39" src="https://github.com/user-attachments/assets/191a9cbe-36bc-4a58-9077-6ceb0d2cd68b" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="610" height="104" alt="Screenshot 2026-08-02 at 14 49 39" src="https://github.com/user-attachments/assets/e21042c1-ac5f-4bc8-91f6-1ff5bdecc582" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="596" height="61" alt="Screenshot 2026-08-02 at 14 50 30" src="https://github.com/user-attachments/assets/6c136f5b-eae5-4ed9-bf2b-080aed57be50" />


seq 10 
## OUTPUT

<img width="628" height="185" alt="Screenshot 2026-08-02 at 14 51 13" src="https://github.com/user-attachments/assets/dd754df5-e8f9-425a-8214-070a633ee7e4" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="633" height="76" alt="Screenshot 2026-08-02 at 14 51 42" src="https://github.com/user-attachments/assets/0e4072af-2862-4ece-ac9f-aad7283f1436" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="629" height="76" alt="Screenshot 2026-08-02 at 14 52 02" src="https://github.com/user-attachments/assets/74ef58b7-d812-4938-9825-431cba9e5bd2" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="553" height="93" alt="Screenshot 2026-08-02 at 14 52 29" src="https://github.com/user-attachments/assets/437d4d6b-bc52-4a5b-8a44-86dcdaf8287c" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="574" height="77" alt="Screenshot 2026-08-02 at 14 52 56" src="https://github.com/user-attachments/assets/8ebd7e54-f423-4313-8ecd-7bd21a31fa4d" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="575" height="75" alt="Screenshot 2026-08-02 at 14 53 17" src="https://github.com/user-attachments/assets/800b0602-7f13-45f3-85aa-039726e1d7c6" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="614" height="80" alt="Screenshot 2026-08-02 at 14 53 44" src="https://github.com/user-attachments/assets/57fc1742-dd21-4fdb-8b3e-89248823fc29" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="620" height="77" alt="Screenshot 2026-08-02 at 14 54 06" src="https://github.com/user-attachments/assets/b81ea874-bf83-4c07-af30-8d78a40031db" />


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

<img width="622" height="109" alt="Screenshot 2026-08-02 at 15 41 47" src="https://github.com/user-attachments/assets/49849162-c00e-4c89-b9e2-0875667e322b" />


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

<img width="630" height="110" alt="Screenshot 2026-08-02 at 15 42 21" src="https://github.com/user-attachments/assets/6f787347-b081-4877-bb9f-e570f168201a" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="624" height="152" alt="Screenshot 2026-08-02 at 15 43 14" src="https://github.com/user-attachments/assets/d4f318e0-e6b7-4f0b-9578-856effa111da" />


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

<img width="451" height="76" alt="Screenshot 2026-08-02 at 15 43 38" src="https://github.com/user-attachments/assets/54bb4b5a-bd66-4270-a621-fd488423bdac" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="560" height="76" alt="Screenshot 2026-08-02 at 15 44 39" src="https://github.com/user-attachments/assets/4a3f1dbb-11c6-4851-99fe-16566f2b6f8e" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="598" height="544" alt="Screenshot 2026-08-02 at 15 45 33" src="https://github.com/user-attachments/assets/d00814eb-0ec9-48fe-89cd-9301c00508d5" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="712" height="346" alt="Screenshot 2026-08-02 at 15 46 36" src="https://github.com/user-attachments/assets/62af6fe1-fc6b-41ee-9e18-7fac0a15fafb" />


tar -xvf backup.tar
## OUTPUT

<img width="637" height="365" alt="Screenshot 2026-08-02 at 15 47 08" src="https://github.com/user-attachments/assets/25cf8f63-3626-42c0-8c7c-4758ffdaf309" />


gzip backup.tar

ls .gz
## OUTPUT

<img width="604" height="48" alt="Screenshot 2026-08-02 at 15 47 47" src="https://github.com/user-attachments/assets/aff2bcbd-b2c7-4453-8465-3e5c6dd0c33f" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="657" height="64" alt="Screenshot 2026-08-02 at 16 09 07" src="https://github.com/user-attachments/assets/9ffe6d9c-a2b6-46d4-88ea-cf0cd4b1c97f" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="599" height="64" alt="Screenshot 2026-08-02 at 15 50 38" src="https://github.com/user-attachments/assets/c75fd57d-1f6c-4036-ab9d-b464045f4058" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="650" height="75" alt="Screenshot 2026-08-02 at 15 51 30" src="https://github.com/user-attachments/assets/dccfc4f1-6e6a-442b-b71f-b8e9e8dbb3b7" />


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

<img width="633" height="291" alt="Screenshot 2026-08-02 at 15 52 47" src="https://github.com/user-attachments/assets/fb03e48d-8d5b-4a0a-baf6-e33b066bb74f" />


 
ls file1
## OUTPUT

<img width="600" height="43" alt="Screenshot 2026-08-02 at 15 53 15" src="https://github.com/user-attachments/assets/7e9cd02e-81be-47ca-8450-9256d69d8f38" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="599" height="48" alt="Screenshot 2026-08-02 at 15 54 27" src="https://github.com/user-attachments/assets/e17d9aeb-2788-4a44-bbb6-6623666c5b1c" />

 
abcd

echo $?
 ## OUTPUT

<img width="465" height="48" alt="Screenshot 2026-08-02 at 15 54 56" src="https://github.com/user-attachments/assets/310e7d56-e48a-4973-b3a4-e2d7fb261370" />

 
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

chmod 755 strcomp.sh 
./strcomp.sh 

## OUTPUT

<img width="586" height="61" alt="Screenshot 2026-08-02 at 16 26 47" src="https://github.com/user-attachments/assets/03ab48d9-5bfb-437e-9017-b02d8a825068" />


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

<img width="665" height="65" alt="Screenshot 2026-08-02 at 16 27 26" src="https://github.com/user-attachments/assets/b9c1c339-5c21-4d5a-8475-4e1eece2b349" />


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

<img width="649" height="92" alt="Screenshot 2026-08-02 at 16 28 46" src="https://github.com/user-attachments/assets/687d2de6-a3f7-491e-a9d7-f4bb815f224c" />


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

<img width="652" height="77" alt="Screenshot 2026-08-02 at 16 29 21" src="https://github.com/user-attachments/assets/04ba0fe4-3798-42c1-b983-f97f4b19f4e0" />


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

<img width="676" height="95" alt="Screenshot 2026-08-02 at 16 30 00" src="https://github.com/user-attachments/assets/bab660ab-542e-4a56-ad99-b5f257821169" />


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

<img width="612" height="65" alt="Screenshot 2026-08-02 at 16 30 32" src="https://github.com/user-attachments/assets/e689a27f-5338-4c14-b25e-6fe19ba120ab" />


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

<img width="651" height="60" alt="Screenshot 2026-08-02 at 16 31 06" src="https://github.com/user-attachments/assets/125d86a9-4cf5-47de-ae8d-df620027006a" />


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

## output

<img width="627" height="46" alt="Screenshot 2026-08-02 at 17 15 06" src="https://github.com/user-attachments/assets/99d7e6a4-f5d4-47c6-bc7f-7a25305e527e" />

 
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
## output

<img width="624" height="184" alt="Screenshot 2026-08-02 at 17 15 43" src="https://github.com/user-attachments/assets/9847b1e0-50ac-4e36-93a4-bf9dd0df080e" />

 
 
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

## output

<img width="583" height="107" alt="Screenshot 2026-08-02 at 17 16 15" src="https://github.com/user-attachments/assets/87734bb5-149a-4921-a8ec-b2b51927047b" />

 
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
## output

<img width="619" height="151" alt="Screenshot 2026-08-02 at 17 16 51" src="https://github.com/user-attachments/assets/7f98cfa7-a57a-4c0b-8d00-7421f67b59f2" />

 
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
## output 

<img width="603" height="104" alt="Screenshot 2026-08-02 at 17 17 18" src="https://github.com/user-attachments/assets/08a65fc8-6cd2-4c56-8e0b-d1eed24e4ceb" />

 
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

## output 

$ ./forin2.sh 

<img width="603" height="104" alt="Screenshot 2026-08-02 at 17 17 18" src="https://github.com/user-attachments/assets/7630005d-f004-4471-ba26-7ca1a67462d7" />
 
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
## OUTPUT

<img width="620" height="153" alt="Screenshot 2026-08-02 at 17 18 00" src="https://github.com/user-attachments/assets/bc4ca701-d0ea-42d6-9b2a-37096c2f7df7" />

 
cat forin1.sh 
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

<img width="564" height="154" alt="Screenshot 2026-08-02 at 17 39 25" src="https://github.com/user-attachments/assets/c91b171b-0b59-4cce-b79e-2234f3884e65" />


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

<img width="619" height="151" alt="Screenshot 2026-08-02 at 17 16 51" src="https://github.com/user-attachments/assets/b3ce19c5-181f-4b6f-a600-aae4e37043e8" />



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

<img width="598" height="136" alt="Screenshot 2026-08-02 at 17 19 31" src="https://github.com/user-attachments/assets/f5ec8478-0180-4fd3-9738-119b04da8f73" />


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

<img width="621" height="105" alt="Screenshot 2026-08-02 at 17 20 01" src="https://github.com/user-attachments/assets/0ae6aacb-07bc-491b-b289-0acb16488f08" />


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

 <img width="620" height="209" alt="Screenshot 2026-08-02 at 17 21 02" src="https://github.com/user-attachments/assets/905c842f-8ac3-48f1-8611-87258c2b4862" />


 
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
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

<img width="609" height="79" alt="Screenshot 2026-08-02 at 17 21 30" src="https://github.com/user-attachments/assets/3b18d52d-4dc2-4b39-9abe-97634ccd9e10" />

 
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
 
$ ./forcontinue.sh 
## OUTPUT

<img width="595" height="107" alt="Screenshot 2026-08-02 at 17 21 59" src="https://github.com/user-attachments/assets/eb200d32-77b6-43a8-910f-b8a5da87f594" />

 
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

<img width="619" height="63" alt="Screenshot 2026-08-02 at 17 23 18" src="https://github.com/user-attachments/assets/e02ad191-be86-4903-80f3-5313145ddffe" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

$ ./exread1.sh 

<img width="619" height="63" alt="Screenshot 2026-08-02 at 17 23 18" src="https://github.com/user-attachments/assets/5e71db89-45b1-4b40-9fb7-dcba1781cbc6" />

 
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
 ./funcex.sh 1 2

 <img width="622" height="152" alt="Screenshot 2026-08-02 at 17 24 19" src="https://github.com/user-attachments/assets/2a6298dc-1d89-428c-b122-0ba05a24b7d2" />



 
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

<img width="589" height="74" alt="Screenshot 2026-08-02 at 17 25 43" src="https://github.com/user-attachments/assets/396d42c6-b5e7-4e52-99a0-1c986fa60c90" />

 
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

<img width="589" height="74" alt="Screenshot 2026-08-02 at 17 25 43" src="https://github.com/user-attachments/assets/c55d2b28-0e29-4b48-86c9-782aad700bab" />

 
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

 <img width="623" height="243" alt="Screenshot 2026-08-02 at 17 26 02" src="https://github.com/user-attachments/assets/b615f904-1929-4254-9b1e-61acd6e85e11" />

 
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

<img width="613" height="223" alt="Screenshot 2026-08-02 at 17 26 42" src="https://github.com/user-attachments/assets/d7348ef4-11d5-48fc-b113-016eae8af36f" />

 
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

<img width="600" height="79" alt="Screenshot 2026-08-02 at 17 27 18" src="https://github.com/user-attachments/assets/a43db9b1-6790-4208-8acd-c23f7f57e572" />


# RESULT:
The Commands are executed successfully.
