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

![1 cat file1](https://github.com/user-attachments/assets/0e353b13-eeaf-4ff5-a421-79ef8d6ffad1)


cat < file2
## OUTPUT

![2 cat file2](https://github.com/user-attachments/assets/af02205a-6b1c-4a7e-9488-805965503583)

# Comparing Files
cmp file1 file2
## OUTPUT
![3 cmp file](https://github.com/user-attachments/assets/9634662b-fd00-4532-86df-e551bcdea3bc)

 
comm file1 file2
 ## OUTPUT
![4 comm file](https://github.com/user-attachments/assets/0c2e6a71-99c5-4d78-9b41-d88d9390f0de)

 
diff file1 file2
## OUTPUT
![5 diff file](https://github.com/user-attachments/assets/8a159fb4-315c-41b3-9375-1a473f5fabb9)


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

![6 cut c1 file](https://github.com/user-attachments/assets/98f1d3ed-9c6e-4c1f-b4b6-5b2df0c6b180)



cut -d "|" -f 1 file22
## OUTPUT

![7 cut  -d file](https://github.com/user-attachments/assets/131720eb-9c46-4c34-8ec2-afe37886986a)


cut -d "|" -f 2 file22
## OUTPUT
![8 cut -f file 2nd](https://github.com/user-attachments/assets/6acba39a-d3d3-4fd3-a127-83fadaaea14b)


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
![9 grep Hello](https://github.com/user-attachments/assets/66532a1b-3a53-414f-b18d-a77c06aa1a46)



grep hello newfile 
## OUTPUT

![10 grep hello](https://github.com/user-attachments/assets/458ebc0f-a9b9-40da-8315-738a5d998ea7)



grep -v hello newfile 
## OUTPUT
![11 grep -v hello](https://github.com/user-attachments/assets/9fc7dfd5-4021-4ea2-af29-50e201ddbd47)



cat newfile | grep -i "hello"
## OUTPUT
![12  grep -i](https://github.com/user-attachments/assets/47225876-f9a8-4407-9126-bd65b2db089c)




cat newfile | grep -i -c "hello"
## OUTPUT
![13 grep -i -c](https://github.com/user-attachments/assets/8659bc53-5dcf-4792-9fa7-48731bca8a1f)




grep -R ubuntu /etc
## OUTPUT
![14 grep -R](https://github.com/user-attachments/assets/a4ec6fe3-ff11-4cf1-96b4-c6516d8a912b)



grep -w -n world newfile   
## OUTPUT
![15  grep-w -n](https://github.com/user-attachments/assets/b4db8029-d900-4cad-a9d9-ece31c3c6e14)


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
![16 egrep -w](https://github.com/user-attachments/assets/8c2aacd8-7aba-4490-ac11-a2ef312167ce)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![17 egrep -w 2nd](https://github.com/user-attachments/assets/364c46a0-9253-46bd-86ef-55d9aa2eb2a8)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![18 egrep -w 3rd](https://github.com/user-attachments/assets/a260c1dc-0d2e-4f09-8577-82a86f9625d3)




egrep '(^hello)' newfile 
## OUTPUT
![19 egrep hello](https://github.com/user-attachments/assets/03d40347-4b33-4401-a77f-36c790904ac8)



egrep '(world$)' newfile 
## OUTPUT
![20 egrep world](https://github.com/user-attachments/assets/3dc9f033-7ac9-4993-bd0b-e35bca9245e3)



egrep '(World$)' newfile 
## OUTPUT
![21 egrep World](https://github.com/user-attachments/assets/f49e88f8-076e-4fd5-9c32-03e5f397e3d4)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![22 egrep Ww](https://github.com/user-attachments/assets/09d57169-1169-4696-bcc8-183e869d9a8d)



egrep '[1-9]' newfile 
## OUTPUT
![23 egrep 1-9](https://github.com/user-attachments/assets/8f85fc45-66e7-4cf9-8404-9e473e20d17d)



egrep 'Linux.*world' newfile 
## OUTPUT
![24 egrep Linux](https://github.com/user-attachments/assets/c3385727-0a7e-46b5-acf6-15ea529e4624)


egrep 'Linux.*World' newfile 
## OUTPUT
![25 egrep ll](https://github.com/user-attachments/assets/3d960bc9-8aef-44c0-80b8-18de7c51410e)


egrep l{2} newfile
## OUTPUT
![25 egrep ll](https://github.com/user-attachments/assets/b856d0ae-628c-4c49-a1eb-1341a139f3f1)



egrep 's{1,2}' newfile
## OUTPUT 
![26 egrep s](https://github.com/user-attachments/assets/bbf057dd-f503-473b-9be3-b3ccc034b3ec)


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
![27 sed -n-e 3p](https://github.com/user-attachments/assets/744b0d59-c6dc-49f1-9fa7-ab80f3aeae61)



sed -n -e '$p' file23
## OUTPUT
![28 sed -n-e p](https://github.com/user-attachments/assets/605bb896-e8e4-4bb4-b361-d58273c78871)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![29 sed -e s](https://github.com/user-attachments/assets/c0cabc59-ecc5-46da-b329-a2c8fa5f2032)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![30 sed -e 2s](https://github.com/user-attachments/assets/8bc29be0-4cdc-49ea-aece-0cc81998ddb7)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![31 sed tom replace](https://github.com/user-attachments/assets/81891efa-f5ec-418e-9ca1-b6eea843c066)



sed -n -e '1,5p' file23
## OUTPUT
![32 sed -n-e 1,5](https://github.com/user-attachments/assets/d8c3c9b2-4e2d-4256-87d7-1507e64d320f)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![33 sed -n-e 2,Joe](https://github.com/user-attachments/assets/f2fdba4e-656a-4636-abe8-4e2e28e65eb4)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![34 sed -n-e tom](https://github.com/user-attachments/assets/204a8979-853c-4a43-aa20-d0602d25b9a4)



seq 10 
## OUTPUT
![35 seq 10](https://github.com/user-attachments/assets/2ac0a351-58da-498f-a144-f4e07003ffe2)



seq 10 | sed -n '4,6p'
## OUTPUT
![36 seq 10 sed -n](https://github.com/user-attachments/assets/90947ed8-3b4d-4597-a2fe-ad3ddf544910)



seq 10 | sed -n '2,~4p'
## OUTPUT
![37 seq 10 sed -n](https://github.com/user-attachments/assets/4cd6cff1-d4da-43de-8701-05ac90491058)



seq 3 | sed '2a hello'
## OUTPUT
![38 seq 3 2a hello](https://github.com/user-attachments/assets/b4d6f415-c42f-4e40-8ee8-9563d24e0c5d)



seq 2 | sed '2i hello'
## OUTPUT
![39 seq 2 2i hello](https://github.com/user-attachments/assets/3687ab7b-ae8e-4431-82a1-31fd0fb3b9f0)


seq 10 | sed '2,9c hello'
## OUTPUT
![40 seq 10 2,9](https://github.com/user-attachments/assets/2ba61bbd-b71e-4c44-9698-213d65f5c795)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![41 sed prev](https://github.com/user-attachments/assets/c4d95396-c018-40ac-8a4f-657c4976c6d3)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![42 sed post](https://github.com/user-attachments/assets/05f03d5f-9073-4e3a-b431-f50516b0d100)


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
![42 5 sort file](https://github.com/user-attachments/assets/bd045b01-bdbb-43a5-b906-d2284cce914e)


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
![43 uniq file22](https://github.com/user-attachments/assets/bcc410b1-fd24-4e51-ad07-ffe11f9a2e1d)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![44 cat tr](https://github.com/user-attachments/assets/506bb2bd-03cb-4e3c-8004-d5f0d0917498)


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
![45 cat tr space](https://github.com/user-attachments/assets/526f0d0e-fcef-47a9-bb57-7bfb4384a064)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![46 cat tr dot](https://github.com/user-attachments/assets/4492aada-eb4f-413d-a3bf-cd2e9bf047bc)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![47 tar cvf](https://github.com/user-attachments/assets/137930f3-a4f9-41eb-89cb-9108b9aa9dbe)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![48 tar tvf](https://github.com/user-attachments/assets/9f4b626c-7567-42ff-8791-8d44f0a75837)


tar -xvf backup.tar
## OUTPUT
![49 tar xvf](https://github.com/user-attachments/assets/bfe58497-45ae-4d89-99ac-59b9172fc169)


gzip backup.tar

ls .gz
## OUTPUT
 ![50  ls gz](https://github.com/user-attachments/assets/76f58932-c00c-4980-b9a2-a9dd1adec18c)

gunzip backup.tar.gz
## OUTPUT
![51 gunzip](https://github.com/user-attachments/assets/e219a857-77ad-49f6-affe-d55144465d09)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![52 shell scripting](https://github.com/user-attachments/assets/71ea55a1-46c7-4976-bfae-8bb02ac55efa)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![53 heredoc](https://github.com/user-attachments/assets/7584649b-bb13-450e-a308-5d65e515a8e4)


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
![54 shell scriptest](https://github.com/user-attachments/assets/41fcec91-3dc0-471c-af96-3abeffc0a3dd)

 
ls file1
## OUTPUT
![55 ls file1](https://github.com/user-attachments/assets/b5765ac3-e54d-4cb9-a426-d2b9d817d268)

echo $?
## OUTPUT 
![56 echo](https://github.com/user-attachments/assets/14aaeb58-596b-4662-bdc6-5ed796ab7be3)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![57 echo 2nd](https://github.com/user-attachments/assets/d26218b0-23ec-43ec-adbf-c316c2233bd3)

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
