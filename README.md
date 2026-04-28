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
<img width="448" height="183" alt="image" src="https://github.com/user-attachments/assets/9e0c56b3-100d-4456-8b90-a491a89b564d" />



cat < file2
## OUTPUT
<img width="388" height="130" alt="image" src="https://github.com/user-attachments/assets/9c6424e6-531a-4c7a-b39c-139137f405ba" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="420" height="44" alt="image" src="https://github.com/user-attachments/assets/73155096-22b9-4f30-b667-6d4cc45346b0" />

comm file1 file2
 ## OUTPUT

 <img width="486" height="283" alt="image" src="https://github.com/user-attachments/assets/082f62cb-ce44-4087-a501-0f0c2a3eb27e" />

diff file1 file2
## OUTPUT

<img width="482" height="333" alt="image" src="https://github.com/user-attachments/assets/c0058406-4829-47b9-a162-65767c591927" />

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


<img width="457" height="130" alt="image" src="https://github.com/user-attachments/assets/ef620557-fe5f-49d2-989d-264f088d947c" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="462" height="133" alt="image" src="https://github.com/user-attachments/assets/27fea74e-2b2f-4d29-86e1-8bbfa720d718" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="634" height="157" alt="image" src="https://github.com/user-attachments/assets/9b490796-ec03-499e-9e3a-f31d89c9e931" />

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

<img width="447" height="72" alt="image" src="https://github.com/user-attachments/assets/89d2de1d-8397-4c04-ad48-fe579d30e316" />


grep hello newfile 
## OUTPUT



<img width="441" height="64" alt="image" src="https://github.com/user-attachments/assets/3692d213-ddfd-4604-9b5f-e4fc282751cf" />

grep -v hello newfile 
## OUTPUT


<img width="455" height="68" alt="image" src="https://github.com/user-attachments/assets/7aed9548-c103-4228-98df-9786f880a330" />

cat newfile | grep -i "hello"
## OUTPUT


<img width="598" height="96" alt="image" src="https://github.com/user-attachments/assets/741a205a-2606-4855-8a0d-e4fc98c47194" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="594" height="68" alt="image" src="https://github.com/user-attachments/assets/c59f1a6d-f6a8-42ab-a5f5-327f52e76cdb" />



grep -R ubuntu /etc
## OUTPUT

<img width="803" height="591" alt="image" src="https://github.com/user-attachments/assets/6d115507-b661-447c-9483-f4df0e7d8f22" />


grep -w -n world newfile   
## OUTPUT

<img width="577" height="104" alt="image" src="https://github.com/user-attachments/assets/6bd9d740-5afb-46a6-bf40-d35f5a2439f0" />

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

<img width="608" height="92" alt="image" src="https://github.com/user-attachments/assets/237dd3e0-0c93-4157-a579-bef33c889285" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

   0 <img width="540" height="131" alt="image" src="https://github.com/user-attachments/assets/c6bfc372-000c-4a74-8b76-dacfa6f4f40d" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="591" height="83" alt="image" src="https://github.com/user-attachments/assets/0c56968c-9889-4825-a37d-bf0f1391a944" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="526" height="72" alt="image" src="https://github.com/user-attachments/assets/ccb981ef-52a4-4dc5-ad15-23cb49d322a7" />


egrep '(world$)' newfile 
## OUTPUT

<img width="572" height="121" alt="image" src="https://github.com/user-attachments/assets/e547a220-127e-43ee-8ae2-aa0c5f71ae6e" />


egrep '(World$)' newfile 
## OUTPUT

<img width="528" height="68" alt="image" src="https://github.com/user-attachments/assets/d8b0d575-d9a0-44e7-bb6a-757d63221bb9" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="624" height="126" alt="image" src="https://github.com/user-attachments/assets/94a8e902-7662-4b6a-be46-31b48eb4ac4f" />



egrep '[1-9]' newfile 
## OUTPUT


<img width="480" height="79" alt="image" src="https://github.com/user-attachments/assets/96647f9b-7450-4b64-b486-74650cf7d233" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="541" height="68" alt="image" src="https://github.com/user-attachments/assets/347aa9a0-825e-40a9-b4e3-225debe55c53" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="562" height="64" alt="image" src="https://github.com/user-attachments/assets/3b011e95-2c26-4b4b-9333-649e6e693d5d" />

egrep l{2} newfile
## OUTPUT

<img width="469" height="89" alt="image" src="https://github.com/user-attachments/assets/8e1d179b-e6c9-470c-82d4-12b8b1571a07" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="464" height="101" alt="image" src="https://github.com/user-attachments/assets/10b4956c-6056-4724-bab8-6633005c7d7e" />

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

<img width="453" height="71" alt="image" src="https://github.com/user-attachments/assets/6a084526-c363-4d07-81ae-6515ff5a1bd0" />


sed -n -e '$p' file23
## OUTPUT

<img width="456" height="62" alt="image" src="https://github.com/user-attachments/assets/dcae7e42-90d4-4bc3-bf45-bdf65b84c0b3" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="645" height="234" alt="image" src="https://github.com/user-attachments/assets/582f62ba-4142-4017-9a17-a62b5d5e3c68" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="641" height="224" alt="image" src="https://github.com/user-attachments/assets/2e967a69-57e1-4c73-9763-631d1b9a31f7" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="619" height="224" alt="image" src="https://github.com/user-attachments/assets/4b2475ad-ef84-4036-b06f-91f284ea9f7b" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="475" height="150" alt="image" src="https://github.com/user-attachments/assets/dfd1af8d-08b4-4998-8b0d-84a2898956bc" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="544" height="116" alt="image" src="https://github.com/user-attachments/assets/73c5da8a-25b8-409e-90ff-546e86145039" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="578" height="71" alt="image" src="https://github.com/user-attachments/assets/ccec16fd-62ac-431a-ab2b-0cb378400121" />


seq 10 
## OUTPUT

<img width="349" height="283" alt="image" src="https://github.com/user-attachments/assets/e9e6b572-9e33-4efd-8f40-a0c5a8c610a5" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="506" height="104" alt="image" src="https://github.com/user-attachments/assets/9a81dc49-0731-4254-89ef-556072c318d0" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="482" height="47" alt="image" src="https://github.com/user-attachments/assets/79e3cd1c-dc0b-4168-9ddd-0338ec8f72c2" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="462" height="136" alt="image" src="https://github.com/user-attachments/assets/be6b07fe-18a9-4af9-9c2e-e2e66f9156ad" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="459" height="111" alt="image" src="https://github.com/user-attachments/assets/784e356d-3135-4435-bae6-15b0133a9df7" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="485" height="110" alt="image" src="https://github.com/user-attachments/assets/158a6d54-f6b5-40c1-b659-34460220dc97" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="630" height="120" alt="image" src="https://github.com/user-attachments/assets/d5795899-5f90-4f0d-afc7-73a12d055675" />


sed -n '2,4{s/$/*/;p}' file23

<img width="518" height="104" alt="image" src="https://github.com/user-attachments/assets/5d49983f-ab5e-490d-833c-67b10c7d8076" />

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

<img width="360" height="133" alt="image" src="https://github.com/user-attachments/assets/d2995e5e-1052-42ad-8003-347ede714ca3" />

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


<img width="410" height="141" alt="image" src="https://github.com/user-attachments/assets/a987b37d-aff1-4fd2-b689-e6391424716d" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="600" height="201" alt="image" src="https://github.com/user-attachments/assets/b4b45bce-ba9c-4ce5-8b7a-c87f1c570e42" />

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

<img width="536" height="125" alt="image" src="https://github.com/user-attachments/assets/a1aa089a-5478-4df6-b109-74bb0b64163f" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="653" height="102" alt="image" src="https://github.com/user-attachments/assets/6d8b4f49-443c-4f48-aba1-78bdb67addfa" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="507" height="198" alt="image" src="https://github.com/user-attachments/assets/e03dcf52-27f2-4166-8053-7c77abd9d4cc" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="719" height="200" alt="image" src="https://github.com/user-attachments/assets/dc1c9ef8-bde6-41c9-9677-bec45168a947" />


tar -xvf backup.tar
## OUTPUT
<img width="572" height="196" alt="image" src="https://github.com/user-attachments/assets/5718f792-82e2-4f08-a9d2-58383004e1c9" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
<img width="390" height="38" alt="image" src="https://github.com/user-attachments/assets/34063d8b-4eec-44b1-b464-9aa0563f087e" />

 
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
<img width="521" height="118" alt="image" src="https://github.com/user-attachments/assets/546c288a-5a71-4dda-8014-0a35b4ade053" />


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
<img width="669" height="640" alt="image" src="https://github.com/user-attachments/assets/54635bc2-972c-4aa1-876e-64de4f26cd13" />

 
ls file1
## OUTPUT
<img width="691" height="540" alt="image" src="https://github.com/user-attachments/assets/2a12334e-e0be-4e12-9ca8-36a781d4717a" />

echo $?
## OUTPUT 
<img width="418" height="45" alt="image" src="https://github.com/user-attachments/assets/27b0d70e-ac5c-4fba-a319-7abfbf18636a" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="420" height="43" alt="image" src="https://github.com/user-attachments/assets/8d6eb55a-e53d-43af-a775-68d6d75af736" />

abcd
 
echo $?
 ## OUTPUT
<img width="420" height="43" alt="image" src="https://github.com/user-attachments/assets/8d6eb55a-e53d-43af-a775-68d6d75af736" />


 
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
<img width="507" height="214" alt="image" src="https://github.com/user-attachments/assets/82afaff1-e0af-4eea-b738-08d01a207aff" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

cat<img width="462" height="50" alt="image" src="https://github.com/user-attachments/assets/db21d1af-b7fc-4288-a137-ddf52cc9c012" />

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
<img width="461" height="58" alt="image" src="https://github.com/user-attachments/assets/e7fb119d-d32a-45c4-9a00-be3d8155771f" />

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

<img width="454" height="93" alt="image" src="https://github.com/user-attachments/assets/4344a815-ac14-4823-a663-1c39f223c30e" />


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11cat iftest
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
 
$ ./if./test.sh 
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
