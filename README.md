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


![os1](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/c73faa54-2dca-4e2b-8477-7d845f912ecf)


cat < file2
## OUTPUT

![os2](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/cb162366-bebd-4b08-9f58-079af8eed8fd)

# Comparing Files
cmp file1 file2

## OUTPUT

 ![os3](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/aea1ed1a-42d6-4294-bba8-c8be61bc8577)

comm file1 file2
 ## OUTPUT

 
![os4](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/83c356b4-72a9-49bb-b74b-622be4c9b69c) 


diff file1 file2
## OUTPUT


![0s5](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/bb2a3c95-ea33-4b38-8d33-152918a2c74c)
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

![os6](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/86c959c0-4ae9-4453-8d7f-f779b0ffa009)



cut -d "|" -f 1 file22
## OUTPUT
![os7](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/bb52c18a-30fb-4e23-b3df-214a333a565b)



cut -d "|" -f 2 file22
## OUTPUT

![os8](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/6db1936c-a251-4614-8c9f-be5a8dddfab3)


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

![os9](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/d8a237c4-1eea-4708-84bf-c532feda4ab8)


grep hello newfile 
## OUTPUT

![os10](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/d78a31fd-a022-4e8a-b612-3781b7d64e12)



grep -v hello newfile 
## OUTPUT

![os11](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/0311d9b1-e411-44a8-a54d-2dbf53df79e6)


cat newfile | grep -i "hello"
## OUTPUT

![os12](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/96114f56-062c-493e-8e67-2e6e4161059a)



cat newfile | grep -i -c "hello"
## OUTPUT
![os13](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/7d333b8d-c11f-45f3-8f30-07e5af1a1a64)




grep -R ubuntu /etc
## OUTPUT
![os14](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/e44e7459-85c0-4829-9459-4c05797e7f68)



grep -w -n world newfile   
## OUTPUT

![os15](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/5598e17f-0a3b-4445-9335-91e021d1e677)

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
![os16](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/0c30856f-79e8-4aa7-bd78-6219a63efc10)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![os17](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/7285c16a-9882-4357-a614-2783329fc9b5)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![os18](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/5d9f35f1-e5d9-48f8-92c0-779866e04b54)



egrep '(^hello)' newfile 
## OUTPUT

![os19](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/4985b72e-82f9-4e29-93cb-ae2878b8874e)


egrep '(world$)' newfile 
## OUTPUT
![0s20](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/b93c5bc6-dadc-4b4d-86f6-47596064d1ae)



egrep '(World$)' newfile 
## OUTPUT
![0s21](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/a565db7f-9dee-4c4c-adb4-f0f4454c2fcc)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![os21](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/0fb76f84-ead8-4c6f-9e87-0d3f88298430)


egrep '[1-9]' newfile 
## OUTPUT

![os22](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/56066b5c-f7c3-4922-8a12-16d1c5c370db)


egrep 'Linux.*world' newfile 
## OUTPUT
![os23](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/63a99081-f9b2-4562-ac77-db35584a0e71)


egrep 'Linux.*World' newfile 
## OUTPUT
![os24](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/c69b41e3-dec1-4461-8399-f147155dd220)


egrep l{2} newfile
## OUTPUT

![os25](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/86d058d2-d00d-4602-af00-cc267a49c0da)


egrep 's{1,2}' newfile
## OUTPUT 
![os26](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/e4b86d92-e202-4835-b76f-648247b6bba4)


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

![os27](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/96b52756-4d66-4ce1-ab38-28ffae0f3b23)


sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![os29](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/adbad8dc-efe8-46ac-a1cc-5ceb0b1460b3)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![os30](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/22999dfc-464b-4d3c-a96a-11cac96b0fe1)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![os31](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/a0013d85-40cb-461a-9c7c-3ebba995b400)


sed -n -e '1,5p' file23
## OUTPUT
![os32](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/d7bd4a58-fc49-413a-a367-71bded087406)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![os33](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/939309c9-c63f-4b21-94e0-902f747bc67e)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![os34](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/39be6778-9817-4968-841e-75755a943972)


seq 10 
## OUTPUT

![os35](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/966555ca-fa09-48db-bad8-5df65852c7c6)


seq 10 | sed -n '4,6p'
## OUTPUT

![os36](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/7550bd1e-8452-4aa6-b4bc-cdc9b7b81fbf)


seq 10 | sed -n '2,~4p'
## OUTPUT


![os37](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/1ea5f5a8-c4e5-4c97-869d-d0e83d31ef1a)

seq 3 | sed '2a hello'
## OUTPUT

![os38](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/1ea2a5a0-f2d9-4203-9b69-677798cf04f8)


seq 2 | sed '2i hello'
## OUTPUT
![os39](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/e5c39e07-1f32-40b6-aa89-fccd01a8b14d)


seq 10 | sed '2,9c hello'
## OUTPUT
![os40](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/b08858e8-a3c3-4f1a-b23f-ba251a5fd30b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![os41](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/b7aaec45-63ba-45cf-a726-b0ed9ebad30e)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![os42](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/1dd5d713-bd83-490f-92ad-81d809f23c8e)

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
![os43](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/6990a411-7939-4024-aacf-dd143904109b)


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
![os44](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/ae1af7ec-8686-4bb8-8ea6-ab7b6cf865ee)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![os45](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/cd1de49a-8df1-4179-b1fa-32da3148e900)

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
![os46](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/041fd93c-b613-4284-9287-975feb9f9246)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![os47](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/efe0e07e-c52e-4bc1-83bf-23ce865ee41e)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![os48](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/80c17029-f17b-442d-8ef7-f2f7a56ef5cc)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
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
![os49](https://github.com/POZHILANVD/OS-Linux-commands-Shell-script/assets/144870498/0fb345b2-8299-40df-98cd-7434e5f36339)


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

 
ls file1
## OUTPUT

echo $?
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
