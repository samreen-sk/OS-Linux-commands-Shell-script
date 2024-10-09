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

![1](https://github.com/user-attachments/assets/ce8baab6-d0ad-47ab-a419-0dd8f1f9205a)


cat < file2
## OUTPUT

![2](https://github.com/user-attachments/assets/188a428a-28b9-4192-b7da-60f0c07559d8)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![3](https://github.com/user-attachments/assets/a98fbe5f-87c4-49d4-bf26-433faf480b94)

comm file1 file2
 ## OUTPUT
![4](https://github.com/user-attachments/assets/9c06a24b-e4a4-4bac-94b6-cea78aacd9ea)

 
diff file1 file2
## OUTPUT
![5](https://github.com/user-attachments/assets/12f9d8a1-7c32-4e91-ba14-01cafba26a86)


# Filters

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
![6](https://github.com/user-attachments/assets/94b4bf6e-4982-4e83-bded-c5839643fde1)




cut -d "|" -f 1 file22
## OUTPUT
![7](https://github.com/user-attachments/assets/4bd05fd8-f812-435a-b93d-57e0039116ad)



cut -d "|" -f 2 file22
## OUTPUT
![8](https://github.com/user-attachments/assets/e5f7ccee-3394-4026-ab64-fd425aad32e3)


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

![9](https://github.com/user-attachments/assets/77d1cde0-76b1-4b7a-b7af-ff760481ed50)


grep hello newfile 
## OUTPUT

![10](https://github.com/user-attachments/assets/782ed4bb-dda6-4517-98d6-4b4bb9d3292e)



grep -v hello newfile 
## OUTPUT
![11](https://github.com/user-attachments/assets/1244fd3a-ea2a-4880-929a-05e7c53aba42)



cat newfile | grep -i "hello"
## OUTPUT

![new](https://github.com/user-attachments/assets/98f30112-9250-4d9a-bee4-686ad92f4b8e)



cat newfile | grep -i -c "hello"
## OUTPUT

![12](https://github.com/user-attachments/assets/4b01d925-1963-4bec-86c8-a8505922fc27)



grep -R ubuntu /etc
## OUTPUT
![13](https://github.com/user-attachments/assets/4506221c-a55c-44d8-8200-185741d8b290)



grep -w -n world newfile   
## OUTPUT

![14](https://github.com/user-attachments/assets/e6870b70-43f4-4d3f-b6e8-ef9e5d681601)

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

![15](https://github.com/user-attachments/assets/f838ebd2-b1df-4ccd-8185-0d1bf70b557e)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![16](https://github.com/user-attachments/assets/8361bf36-9f14-49f9-8ca4-8d20fa0022c5)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![17](https://github.com/user-attachments/assets/af1a83b9-1f96-42b1-9130-7f4f258688c3)



egrep '(^hello)' newfile 
## OUTPUT

![new1](https://github.com/user-attachments/assets/86a461a0-c67e-41ad-b109-1541641ddaa7)


egrep '(world$)' newfile 
## OUTPUT

![18](https://github.com/user-attachments/assets/26f82089-7999-45ab-9757-a1f0aa75c221)


egrep '(World$)' newfile 
## OUTPUT
![19](https://github.com/user-attachments/assets/1a9c9954-237c-4ad7-908d-9ec7db292f4a)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![20](https://github.com/user-attachments/assets/ba295343-00de-4f10-8fc7-397f3d7c2449)


egrep '[1-9]' newfile 
## OUTPUT
![21](https://github.com/user-attachments/assets/c55e7c9a-4b17-406e-a8ed-7cbd397d25b9)



egrep 'Linux.*world' newfile 
## OUTPUT

![22](https://github.com/user-attachments/assets/67dfe62e-3ef1-4554-956a-e56825df90f0)

egrep 'Linux.*World' newfile 
## OUTPUT
![23](https://github.com/user-attachments/assets/8575ed00-61c5-47bf-a5dd-2e1787f551d8)


egrep l{2} newfile
## OUTPUT
![24](https://github.com/user-attachments/assets/d0258364-a5da-40f4-a694-c3511c8fc680)



egrep 's{1,2}' newfile
## OUTPUT 

![25](https://github.com/user-attachments/assets/72ea52a0-52a0-406f-baad-0804937730f7)

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

![26](https://github.com/user-attachments/assets/ecba1cbd-6685-4ee8-af1c-5707b5d20bce)


sed -n -e '$p' file23
## OUTPUT

![27](https://github.com/user-attachments/assets/d923be9b-e662-4279-9796-857a5ebc5ca6)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![28](https://github.com/user-attachments/assets/dcf8d069-d065-48a2-b883-f4f35c0eaadd)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![29](https://github.com/user-attachments/assets/7b0786f1-73db-4027-bb59-c20f1ab5558e)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![30](https://github.com/user-attachments/assets/fc2db2e6-fc00-41fe-8234-7f161b425841)


sed -n -e '1,5p' file23
## OUTPUT

![31](https://github.com/user-attachments/assets/c8fa6545-0d1e-47b3-b90b-e8e653be6b08)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![32](https://github.com/user-attachments/assets/3db508f5-fbf7-4714-9ae7-359e6ae8e2ac)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![33](https://github.com/user-attachments/assets/4964d862-aee9-4722-8ad4-d86a6d7a7ba1)


seq 10 
## OUTPUT
![34](https://github.com/user-attachments/assets/259ec4e9-3589-4a7e-b4e7-fc667becb430)



seq 10 | sed -n '4,6p'
## OUTPUT

![35](https://github.com/user-attachments/assets/1c6b96e5-cdb0-493f-a39e-ef97d26a2c40)


seq 10 | sed -n '2,~4p'
## OUTPUT

![36](https://github.com/user-attachments/assets/9af3fb99-d765-40de-bf53-632466f26f36)


seq 3 | sed '2a hello'
## OUTPUT

![37](https://github.com/user-attachments/assets/7c499e36-21f3-46e4-aed7-d416e7ff4a72)


seq 2 | sed '2i hello'
## OUTPUT

![38](https://github.com/user-attachments/assets/1b01ba07-89f0-44dd-b9ff-915fcd230da5)

seq 10 | sed '2,9c hello'
## OUTPUT

![39](https://github.com/user-attachments/assets/3077731e-f76e-4ee1-8d55-1cf1d94ab5ef)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![40](https://github.com/user-attachments/assets/ac80ae23-c163-4d0a-9fda-41c8900c6a5b)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![41](https://github.com/user-attachments/assets/3ab79179-33f8-4467-9e61-1189bf9e8aca)


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
![42](https://github.com/user-attachments/assets/07752c05-7a3e-4c26-b207-0cf17eebf082)


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

![43](https://github.com/user-attachments/assets/1eb7defb-513e-40c8-8699-86fb59654547)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![upper](https://github.com/user-attachments/assets/2e0b9cd1-76a0-41a7-b2e5-e747d4ca377d)

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

![44](https://github.com/user-attachments/assets/cde79d91-858d-43fc-a139-c86390738511)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![45](https://github.com/user-attachments/assets/42fc3eb5-75dc-4850-9ce5-2d2060f188af)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![46](https://github.com/user-attachments/assets/8e03fe10-2d91-43cb-98f6-d26943b8918b)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![47](https://github.com/user-attachments/assets/6e97789b-65fa-4034-9c09-4473de8dc484)


tar -xvf backup.tar
## OUTPUT
![48](https://github.com/user-attachments/assets/811e07da-51d3-421c-99a9-441ccbb0a484)

gzip backup.tar

ls .gz
## OUTPUT
 ![49](https://github.com/user-attachments/assets/8b80d6e1-a802-4510-8aa3-07dcceec369c)

gunzip backup.tar.gz
## OUTPUT
![50](https://github.com/user-attachments/assets/1021e6a1-fcbf-45fb-a9b1-cac2ac7d6585)


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![51](https://github.com/user-attachments/assets/61a543a6-e28e-4134-8cdd-ced64f571030)

 ![52](https://github.com/user-attachments/assets/405ee9db-9375-43a5-98fd-1086ddeec18f)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![53](https://github.com/user-attachments/assets/b8ca439d-77bb-4707-919a-c8665e8886b8)


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
![54](https://github.com/user-attachments/assets/59834dde-b698-4e36-80cb-466b668c1b1e)

 
ls file1
## OUTPUT
![ls](https://github.com/user-attachments/assets/baf803ce-dc95-4652-b8cb-aca068ed7484)

echo $?
 ## OUTPUT

![new2](https://github.com/user-attachments/assets/052bd65a-634f-4cb9-b6e3-447326af8166)

 
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
## OUTPUT

![55](https://github.com/user-attachments/assets/9c075d22-0cbf-4774-9587-bf792133da35)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![56](https://github.com/user-attachments/assets/b6c55895-b8e8-4a7c-ac13-0ebdeca15bf5)

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
![57](https://github.com/user-attachments/assets/2825f112-d0f7-4a53-a2de-5ff4e3fa7dd2)

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
![58](https://github.com/user-attachments/assets/cb14034e-a405-4aa1-af26-395c7028c533)



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
## OUTPUT
![59](https://github.com/user-attachments/assets/44f58cf7-b80d-4067-b3f1-d228f8de65a6)

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
## OUTPUT
![60](https://github.com/user-attachments/assets/43d4ffde-3080-4c08-8862-2e35dad74aa0)

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
![61](https://github.com/user-attachments/assets/b866ea46-b83a-4acb-9a55-02e4172917da)


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
![62](https://github.com/user-attachments/assets/c55fde25-08b9-4fc2-93b2-03808a128ca4)

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
 ## OUTPUT
 ![63](https://github.com/user-attachments/assets/8e583060-27ce-4f90-b089-9a840a427e64)

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
 
 ## OUTPUT
 ![64](https://github.com/user-attachments/assets/69eaa5fd-be8a-4f6d-adc8-534fbff858da)

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
 
 ## OUTPUT
 
 ![65](https://github.com/user-attachments/assets/8f879db6-4541-4365-9637-3e07000a624b)

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
 ## OUTPUT
 ![66](https://github.com/user-attachments/assets/451e2750-a136-4525-bc77-04ec57f3c92c)

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
 ## OUTPUT
 ![67](https://github.com/user-attachments/assets/c1809183-3619-42c8-8fc2-9d2d35296a12)

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
![68](https://github.com/user-attachments/assets/14f8c40b-3199-4934-a6ad-4a3048a26444)

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

![forinfile](https://github.com/user-attachments/assets/869b5123-b32b-41b3-8d60-a45022500b29)

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
![69](https://github.com/user-attachments/assets/857c9091-15d2-4684-9342-a751512eb62e)

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

![70](https://github.com/user-attachments/assets/e474de92-0d75-4cfe-bac5-3397128c89ce)
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

 ![71](https://github.com/user-attachments/assets/57265bef-faf9-4c6b-b046-c91cfa8d36da)

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
![72](https://github.com/user-attachments/assets/7d1cc7d1-7f25-46f4-bc84-d5e9129658b6)

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
 ![73](https://github.com/user-attachments/assets/594e7f9a-3998-4dcb-975a-3a88a0c2e974)

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

![74](https://github.com/user-attachments/assets/2eeff5a5-8219-411b-9eff-87a2c926e9f6)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![75](https://github.com/user-attachments/assets/5366d701-7ff6-486c-94ba-0d1868abdb93)


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
![76](https://github.com/user-attachments/assets/acee6209-c1ac-4a69-9d1b-50ce07a38a6f)

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
![77](https://github.com/user-attachments/assets/c77a3da9-e804-4458-b8ff-2067067d9b7f)

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
![78](https://github.com/user-attachments/assets/ad074646-ed24-4a93-a9f1-6a9afc0d351b)

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
![79](https://github.com/user-attachments/assets/184404ed-c1c9-466e-a710-61d5fe705351)

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
 ![80](https://github.com/user-attachments/assets/e6022673-a814-4c86-bc24-dfb8d87e7fe7)

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
![81](https://github.com/user-attachments/assets/a00adcf3-d0f5-4e34-9dcd-d0cd2d95c9d3)


# RESULT:
The Commands are executed successfully.
