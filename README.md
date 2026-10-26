<img width="386" height="127" alt="Screenshot 2026-10-22 081247" src="https://github.com/user-attachments/assets/2abf6167-53c8-4edc-b6a3-f5b649bfd749" />
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
<img width="386" height="127" alt="Screenshot 2026-10-22 081247" src="https://github.com/user-attachments/assets/9658e280-3963-42d3-9bc0-ead8acc1ee12" />

cat < file2
## OUTPUT
<img width="410" height="167" alt="Screenshot 2026-10-22 081339" src="https://github.com/user-attachments/assets/09fe33f7-48b4-47df-b3b9-b2b938c838e6" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="385" height="151" alt="Screenshot 2026-10-22 081353" src="https://github.com/user-attachments/assets/72809583-0c02-4c62-b1f2-bee6a63f5fb8" />

comm file1 file2
 ## OUTPUT
<img width="463" height="47" alt="Screenshot 2026-10-22 081434" src="https://github.com/user-attachments/assets/0689cb98-2646-4ad3-b6a3-6ce93c5a0be9" />

 
diff file1 file2
## OUTPUT
<img width="387" height="120" alt="Screenshot 2026-10-22 081733" src="https://github.com/user-attachments/assets/3f636d2f-eb20-4cb8-93d1-754e16c919d9" />


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
<img width="370" height="142" alt="Screenshot 2026-10-22 081756" src="https://github.com/user-attachments/assets/089007e8-add9-4c9f-a300-49d4297d3039" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="422" height="50" alt="Screenshot 2026-10-22 081948" src="https://github.com/user-attachments/assets/cd18a5f8-e7d6-41c5-8288-e1a3834efe8d" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="465" height="262" alt="Screenshot 2026-10-22 082024" src="https://github.com/user-attachments/assets/121720ae-c30c-46d3-831c-b3eddbbc1ba1" />


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

<img width="462" height="56" alt="Screenshot 2026-10-22 082605" src="https://github.com/user-attachments/assets/8b7d5aa9-51b1-43ca-b308-611379206c7c" />


grep hello newfile 
## OUTPUT

<img width="452" height="50" alt="Screenshot 2026-10-22 082637" src="https://github.com/user-attachments/assets/7087b062-7852-4bd4-b50b-17a64b21510d" />



grep -v hello newfile 
## OUTPUT
<img width="480" height="57" alt="Screenshot 2026-10-22 082702" src="https://github.com/user-attachments/assets/1b3fca3d-916a-4298-95b8-442c0be37058" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="557" height="75" alt="Screenshot 2026-10-22 082729" src="https://github.com/user-attachments/assets/fa9d7830-a876-4364-a82f-78a6c8a4c99b" />


cat newfile | grep -i -c "hello"
## OUTPUT
<img width="588" height="57" alt="Screenshot 2026-10-22 082749" src="https://github.com/user-attachments/assets/3197ef90-58bd-4725-bc66-fcedcfaa1793" />



grep -R ubuntu /etc
## OUTPUT

<img width="1552" height="570" alt="Screenshot 2026-10-22 082934" src="https://github.com/user-attachments/assets/68311c34-d12a-4ffa-8a15-7f0603774a2b" />


grep -w -n world newfile   
## OUTPUT
<img width="521" height="83" alt="Screenshot 2026-10-22 082958" src="https://github.com/user-attachments/assets/23554462-7271-4651-89b4-39412036b689" />


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
<img width="602" height="78" alt="Screenshot 2026-10-22 083156" src="https://github.com/user-attachments/assets/256ac9aa-5bf7-4826-91a2-5169bed9e58c" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="570" height="75" alt="Screenshot 2026-10-22 083219" src="https://github.com/user-attachments/assets/e363bbd4-a18f-4411-ab5b-73786cb2a8bb" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="630" height="70" alt="Screenshot 2026-10-22 083240" src="https://github.com/user-attachments/assets/2e2648a7-9d66-4c7c-a6d1-3cdbc2989512" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="533" height="55" alt="Screenshot 2026-10-22 083300" src="https://github.com/user-attachments/assets/30c161ad-b2c2-4f94-b4b2-3b39d3a205e3" />


egrep '(world$)' newfile 
## OUTPUT

<img width="512" height="76" alt="Screenshot 2026-10-22 083354" src="https://github.com/user-attachments/assets/b1853120-a437-42d8-b634-3c4dd1809cfb" />


egrep '(World$)' newfile 
## OUTPUT
<img width="552" height="55" alt="Screenshot 2026-10-22 083414" src="https://github.com/user-attachments/assets/b987cab1-d8ce-4756-8e71-81055b6d8dd3" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="596" height="96" alt="Screenshot 2026-10-22 083432" src="https://github.com/user-attachments/assets/cbbe1710-d240-4bbc-a735-dce1b840cc79" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="522" height="50" alt="Screenshot 2026-10-22 083452" src="https://github.com/user-attachments/assets/6b563fad-68c8-493b-9c15-f61f374e4606" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="600" height="58" alt="Screenshot 2026-10-22 083516" src="https://github.com/user-attachments/assets/9aab8b63-d3de-4531-a056-5de7c5cd478a" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="590" height="53" alt="Screenshot 2026-10-22 083531" src="https://github.com/user-attachments/assets/0822e919-c221-46f6-b10a-a3a8683f9fbe" />


egrep l{2} newfile
## OUTPUT
<img width="533" height="73" alt="Screenshot 2026-10-22 083603" src="https://github.com/user-attachments/assets/144df8e9-0bac-4daf-a9ef-30d8fde9726e" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="596" height="102" alt="Screenshot 2026-10-22 083623" src="https://github.com/user-attachments/assets/ac4ad64a-a7d1-4cd7-b90b-7c7afc2cf642" />


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
<img width="523" height="50" alt="Screenshot 2026-10-22 083842" src="https://github.com/user-attachments/assets/7f096f13-34f1-4df1-a7b4-725c129e6cf2" />



sed -n -e '$p' file23
## OUTPUT
<img width="505" height="45" alt="Screenshot 2026-10-22 083858" src="https://github.com/user-attachments/assets/9e77821c-14b3-4029-b9f2-d9084142f6fc" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="575" height="221" alt="Screenshot 2026-10-22 083922" src="https://github.com/user-attachments/assets/945e93be-986f-4edc-ac03-a1e4c92e5b7a" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="582" height="212" alt="Screenshot 2026-10-22 083947" src="https://github.com/user-attachments/assets/3eb32b14-5a24-4cb6-94f6-6f02f314b911" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="632" height="222" alt="Screenshot 2026-10-22 084013" src="https://github.com/user-attachments/assets/cae7a102-65ed-45ba-959c-49c66398d370" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="530" height="153" alt="Screenshot 2026-10-22 084042" src="https://github.com/user-attachments/assets/bb80e6c7-f03c-4c5d-a017-3df47230040c" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="566" height="97" alt="Screenshot 2026-10-22 084116" src="https://github.com/user-attachments/assets/d2a9e5e0-26f9-4f49-ba13-b8069c7f5abf" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="632" height="82" alt="Screenshot 2026-10-22 084136" src="https://github.com/user-attachments/assets/c4924bb1-8ff1-4d7a-9602-07748cf9d075" />



seq 10 
## OUTPUT
<img width="392" height="265" alt="Screenshot 2026-10-22 084152" src="https://github.com/user-attachments/assets/44575624-325c-4442-bce3-89291aea9091" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="562" height="102" alt="Screenshot 2026-10-22 084210" src="https://github.com/user-attachments/assets/79494a45-7108-4493-be23-b9bc1cbbeeee" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="562" height="92" alt="Screenshot 2026-10-22 084233" src="https://github.com/user-attachments/assets/7b5cdf6f-a702-4485-85c9-8478dcb051ff" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="516" height="120" alt="Screenshot 2026-10-22 084308" src="https://github.com/user-attachments/assets/d035ff04-3599-467e-9c6e-c7b2938592a0" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="500" height="105" alt="Screenshot 2026-10-22 084328" src="https://github.com/user-attachments/assets/e97ce74d-9604-4dc3-be81-c912f1d50ded" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="550" height="100" alt="Screenshot 2026-10-22 084348" src="https://github.com/user-attachments/assets/09ee2650-0a8e-4c67-97a6-c187c0308f45" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="608" height="100" alt="Screenshot 2026-10-22 084405" src="https://github.com/user-attachments/assets/3cafa6b5-d266-4d1d-a270-74b7e1234088" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="617" height="102" alt="Screenshot 2026-10-22 084459" src="https://github.com/user-attachments/assets/e29d8a87-d4c9-41e9-bef8-d5c7fb3b68cd" />


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
<img width="425" height="151" alt="Screenshot 2026-10-22 084551" src="https://github.com/user-attachments/assets/31d2d201-d99a-412c-8b38-7aa7da379c43" />


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
<img width="470" height="151" alt="Screenshot 2026-10-22 084643" src="https://github.com/user-attachments/assets/89daadbd-3806-4566-b018-7807d1063738" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="725" height="220" alt="Screenshot 2026-10-22 084819" src="https://github.com/user-attachments/assets/885e127f-1a19-4e61-9387-7dd9d50e4faa" />

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
<img width="581" height="96" alt="Screenshot 2026-10-22 084912" src="https://github.com/user-attachments/assets/2dae2314-142f-4bb1-b8dc-4f24a72283a3" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="767" height="97" alt="Screenshot 2026-10-22 084924" src="https://github.com/user-attachments/assets/b29b5075-baa7-4eb0-8679-bd913e5c245d" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="522" height="227" alt="Screenshot 2026-10-22 084936" src="https://github.com/user-attachments/assets/d08098be-5db7-47aa-8819-d3b0113a0fe5" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="572" height="213" alt="Screenshot 2026-10-22 085050" src="https://github.com/user-attachments/assets/57917661-75b1-40f2-a826-94ef4266f59a" />


tar -xvf backup.tar
## OUTPUT
<img width="738" height="330" alt="Screenshot 2026-10-22 085222" src="https://github.com/user-attachments/assets/14b22467-6e5d-461c-8405-f39fc4f0c2e7" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="632" height="320" alt="Screenshot 2026-10-22 085553" src="https://github.com/user-attachments/assets/bc779cce-7af0-4231-8f84-2a9bfe3fe82a" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="632" height="320" alt="Screenshot 2026-10-22 085553" src="https://github.com/user-attachments/assets/035b2616-e323-4f82-b523-7ff727ec9e0b" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="447" height="100" alt="Screenshot 2026-10-22 090230" src="https://github.com/user-attachments/assets/10e10804-8005-4b6f-a31b-a058f88ca8cc" />


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
<img width="502" height="290" alt="Screenshot 2026-10-22 090440" src="https://github.com/user-attachments/assets/c24293f9-422b-4026-acf3-a7b323c46922" />

 
ls file1
## OUTPUT
<img width="350" height="52" alt="Screenshot 2026-10-22 090521" src="https://github.com/user-attachments/assets/9a35de2a-bd71-48bd-8e44-056ed95abfda" />


echo $?
## OUTPUT 
<img width="337" height="56" alt="Screenshot 2026-10-22 090525" src="https://github.com/user-attachments/assets/6dbb684e-5f51-4d38-8ca9-46d3f42db113" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="356" height="53" alt="Screenshot 2026-10-22 090704" src="https://github.com/user-attachments/assets/f3b54386-3c4a-4567-8b48-410044ff3206" />

abcd
 
echo $?
 ## OUTPUT
<img width="356" height="53" alt="Screenshot 2026-10-22 090704" src="https://github.com/user-attachments/assets/ae6daac9-8ca5-4212-ad9e-5cbacae4f959" />


 
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
<img width="457" height="251" alt="Screenshot 2026-10-22 090802" src="https://github.com/user-attachments/assets/8973e471-2435-441a-a19e-93d52e43927a" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="510" height="52" alt="Screenshot 2026-10-22 090959" src="https://github.com/user-attachments/assets/d2ca373a-f173-462e-abbb-2cb0c9c8e7d9" />


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
<img width="506" height="52" alt="Screenshot 2026-10-22 091045" src="https://github.com/user-attachments/assets/072fe399-d0ba-40dc-be0c-6c83d2e7bfee" />

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

<img width="476" height="107" alt="Screenshot 2026-10-22 091133" src="https://github.com/user-attachments/assets/14f6557e-9473-4d10-a163-3fc24fe8f8f4" />

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
<img width="697" height="143" alt="Screenshot 2026-10-22 091244" src="https://github.com/user-attachments/assets/4ba38ad7-f1ed-4268-a1d9-bb29e34f850c" />

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
<img width="730" height="107" alt="Screenshot 2026-10-22 091343" src="https://github.com/user-attachments/assets/e6c30070-6eb7-47a9-b084-27ded2447f31" />

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
<img width="742" height="96" alt="Screenshot 2026-10-22 091432" src="https://github.com/user-attachments/assets/313e5c23-b482-4b11-aab7-9b4d4576d42f" />


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
<img width="510" height="92" alt="Screenshot 2026-10-22 091511" src="https://github.com/user-attachments/assets/5f7b73c0-d6b6-4eb0-9bcd-73b14eb0ba17" />

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
<img width="632" height="320" alt="Screenshot 2026-10-22 085553" src="https://github.com/user-attachments/assets/dbaaefba-3e00-4827-9ac2-823862095b27" />

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
<img width="767" height="97" alt="Screenshot 2026-10-22 084924" src="https://github.com/user-attachments/assets/66b9262a-8f71-44f0-af9a-ca7b2dddd006" />

 
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
<img width="445" height="143" alt="Screenshot 2026-10-22 084805" src="https://github.com/user-attachments/assets/d17dec25-c044-42fa-8778-3a25aeb95d13" />

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
 <img width="575" height="221" alt="Screenshot 2026-10-22 083922" src="https://github.com/user-attachments/assets/d17b5900-07b0-46ae-b1bf-b1d8e1f8bb93" />

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
<img width="512" height="76" alt="Screenshot 2026-10-22 083354" src="https://github.com/user-attachments/assets/c572b658-8601-4b39-b4d5-96d4ece7a050" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 


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
<img width="1552" height="570" alt="Screenshot 2026-10-22 082934" src="https://github.com/user-attachments/assets/0fbf803b-b58e-43f2-a452-22c5c632ec20" />

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
<img width="512" height="76" alt="Screenshot 2026-10-22 083354" src="https://github.com/user-attachments/assets/2eae6a89-8e1f-45f7-ae0a-9fb09b34ce94" />

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
 <img width="512" height="76" alt="Screenshot 2026-10-22 083354" src="https://github.com/user-attachments/assets/2d005dba-7891-4b98-ae1c-385c1a556578" />

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
<img width="750" height="390" alt="Screenshot 2026-10-22 090515" src="https://github.com/user-attachments/assets/58e6c997-dacc-4473-a797-da9b39edceb5" />


# RESULT:
The Commands are executed successfully.
