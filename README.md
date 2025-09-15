<img width="398" height="85" alt="image" src="https://github.com/user-attachments/assets/3d77ec4a-b8bb-4a46-9ea2-4e490cf059e1" /># OS-Linux-commands-Shell-scripting
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

<img width="438" height="175" alt="image" src="https://github.com/user-attachments/assets/763f2947-18fd-4eac-badf-f1c1f24ff811" />



cat < file2
## OUTPUT

<img width="373" height="200" alt="image" src="https://github.com/user-attachments/assets/ab69654e-32b6-48ce-9ef9-9bd5ba2bc0d8" />


# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="420" height="84" alt="image" src="https://github.com/user-attachments/assets/44784e6f-e981-4bad-8db1-5f48026f9a77" />

comm file1 file2
 ## OUTPUT

<img width="401" height="382" alt="image" src="https://github.com/user-attachments/assets/c0643ca1-8613-4693-b70f-c8ce40a764a7" />

 
diff file1 file2
## OUTPUT



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

<img width="349" height="128" alt="image" src="https://github.com/user-attachments/assets/eed11cea-0f80-40cf-a58f-21d42a325ac7" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="340" height="147" alt="image" src="https://github.com/user-attachments/assets/1baf2ace-170a-4b81-8fce-cfdf3e1f02b4" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="416" height="152" alt="image" src="https://github.com/user-attachments/assets/c6601d06-699e-46ff-ac0f-7eb221ebe743" />


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

<img width="292" height="103" alt="image" src="https://github.com/user-attachments/assets/8d4a78d7-c339-4ce3-8240-d60afe7d492c" />


grep hello newfile 
## OUTPUT

<img width="292" height="103" alt="image" src="https://github.com/user-attachments/assets/326a3857-58a8-4061-bf4a-879b2a5f8fc1" />



grep -v hello newfile 
## OUTPUT

<img width="318" height="117" alt="image" src="https://github.com/user-attachments/assets/f3ed8120-916a-43dd-af7e-48fda095e1fc" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="423" height="105" alt="image" src="https://github.com/user-attachments/assets/134c1107-78eb-45fc-84fe-e4a2862e94ff" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="423" height="82" alt="image" src="https://github.com/user-attachments/assets/3724917e-cae4-4963-a17b-1076ee2cf74b" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

<img width="412" height="100" alt="image" src="https://github.com/user-attachments/assets/cfabf303-3439-464f-8cda-ed4777d8873d" />


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

<img width="392" height="99" alt="image" src="https://github.com/user-attachments/assets/33a7d4f5-9a87-4783-8677-590224846ed6" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="392" height="99" alt="image" src="https://github.com/user-attachments/assets/50ba1b30-791b-4de4-97da-5792d8a7ce0b" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="394" height="98" alt="image" src="https://github.com/user-attachments/assets/36ccae17-75da-4f1e-b788-42743bd4fe70" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="373" height="77" alt="image" src="https://github.com/user-attachments/assets/d1a37979-4067-4dea-a398-f1e355fcd03b" />


egrep '(world$)' newfile 
## OUTPUT

<img width="351" height="104" alt="image" src="https://github.com/user-attachments/assets/16823a23-d6c4-4f7a-a359-41da00481ec2" />


egrep '(World$)' newfile 
## OUTPUT

<img width="378" height="73" alt="image" src="https://github.com/user-attachments/assets/6efbe52f-2af0-4475-abf2-86bb4a7a0f0e" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="399" height="122" alt="image" src="https://github.com/user-attachments/assets/70a9fa8d-0a9f-439a-b70f-28104cd9705d" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="328" height="78" alt="image" src="https://github.com/user-attachments/assets/937ae7a7-cbae-48a3-8217-6e5c1a7d967c" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="396" height="74" alt="image" src="https://github.com/user-attachments/assets/313dd605-023a-4060-bc75-5ba362ec0906" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="405" height="79" alt="image" src="https://github.com/user-attachments/assets/68e4ddd8-5b26-41fc-a505-0599e7f1e6c3" />

egrep l{2} newfile
## OUTPUT

<img width="336" height="111" alt="image" src="https://github.com/user-attachments/assets/927b2271-fa4a-4070-8a7b-8dc3afa30907" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="353" height="129" alt="image" src="https://github.com/user-attachments/assets/e882d296-3440-4360-8225-77a6806597bb" />


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

<img width="381" height="75" alt="image" src="https://github.com/user-attachments/assets/3f1a775a-b5ba-4214-b577-0ba50358f69e" />


sed -n -e '$p' file23
## OUTPUT

<img width="330" height="105" alt="image" src="https://github.com/user-attachments/assets/e2f98bd4-f453-4d5f-bc23-ca6279b6f426" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="432" height="255" alt="image" src="https://github.com/user-attachments/assets/38dd751a-b7a5-409e-a749-e2b24e9851d7" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="436" height="217" alt="image" src="https://github.com/user-attachments/assets/f27b1e9f-63cb-44c6-aa03-4ee7903d6244" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="429" height="244" alt="image" src="https://github.com/user-attachments/assets/6657c976-50c7-4244-81d9-75467e1a031d" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="434" height="211" alt="image" src="https://github.com/user-attachments/assets/2a654c5b-d786-4833-a4d5-45a2cc0c244d" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="412" height="96" alt="image" src="https://github.com/user-attachments/assets/9257aa2d-bc2d-4014-8785-dfe1f0656547" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="464" height="175" alt="image" src="https://github.com/user-attachments/assets/77b1c953-b0e4-4221-83c2-c113d85ada5f" />


seq 10 
## OUTPUT

<img width="393" height="300" alt="image" src="https://github.com/user-attachments/assets/54ad5124-7b99-410f-8d1a-84461290a0fb" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="366" height="127" alt="image" src="https://github.com/user-attachments/assets/4f296285-f7d1-47f9-96b9-e234cf1cb6ff" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="336" height="122" alt="image" src="https://github.com/user-attachments/assets/6066e849-83e1-4cc5-b6f3-c953a64e990c" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="398" height="85" alt="image" src="https://github.com/user-attachments/assets/40aaba19-88ff-44c7-af4a-9cb898553ea8" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="349" height="79" alt="image" src="https://github.com/user-attachments/assets/c133bcf1-f425-46ac-8c09-ca84d419dde1" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="314" height="76" alt="image" src="https://github.com/user-attachments/assets/c158fa47-586d-427f-9ade-03dc9a204b11" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="460" height="131" alt="image" src="https://github.com/user-attachments/assets/c953ecf5-1461-45a4-82b6-40cc3183ea53" />


sed -n '2,4{s/$/*/;p}' file23

<img width="448" height="125" alt="image" src="https://github.com/user-attachments/assets/7d55f91c-4535-4f54-b2ce-5540b1894b32" />


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

<img width="369" height="154" alt="image" src="https://github.com/user-attachments/assets/946bbaa9-2706-4adf-8a79-5525cab7e371" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="468" height="231" alt="image" src="https://github.com/user-attachments/assets/7717e8d3-113b-458a-ae5a-35129a9797ac" />


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

<img width="399" height="129" alt="image" src="https://github.com/user-attachments/assets/3f36d68f-ddc0-4820-a368-757a7401b7d2" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="514" height="124" alt="image" src="https://github.com/user-attachments/assets/b91e7e1c-f29e-428c-87ca-c82785c94d45" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="397" height="279" alt="image" src="https://github.com/user-attachments/assets/c03afda5-cc9f-4f5f-9cfb-c7da7550ef3b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="802" height="125" alt="image" src="https://github.com/user-attachments/assets/1b596000-53c6-48f0-a0cf-d847ede9de30" />


tar -xvf backup.tar
## OUTPUT

<img width="543" height="279" alt="image" src="https://github.com/user-attachments/assets/beff1b90-5f6e-48d4-ae2d-52b0a3f9615b" />


gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

<img width="495" height="101" alt="image" src="https://github.com/user-attachments/assets/f45c8542-cce9-4460-9661-e59b8560611c" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="433" height="158" alt="image" src="https://github.com/user-attachments/assets/1354f197-41bc-441e-8c03-15a9b09cc610" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="443" height="132" alt="image" src="https://github.com/user-attachments/assets/9bdaf2c7-c12c-4dd0-88a0-6f446616089e" />


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

<img width="763" height="316" alt="image" src="https://github.com/user-attachments/assets/a532f356-1d14-4ebb-8613-3e34b764983f" />

 
ls file1
## OUTPUT

<img width="515" height="85" alt="image" src="https://github.com/user-attachments/assets/8a922926-1a37-4747-99cf-6311fb89187b" />


echo $?
## OUTPUT 

<img width="452" height="91" alt="image" src="https://github.com/user-attachments/assets/37ca7a28-b3c1-416d-b00a-8e5c4bb503c2" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="488" height="81" alt="image" src="https://github.com/user-attachments/assets/2ce34708-fe34-4a57-9f07-fc81becb7a97" />

 

 
echo $?
 ## OUTPUT

<img width="483" height="82" alt="image" src="https://github.com/user-attachments/assets/3988e979-aaf1-48e1-afc3-83ba43ab6fb9" />

 
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

<img width="560" height="340" alt="image" src="https://github.com/user-attachments/assets/37bcd2a6-e5e4-4941-80cc-bb60df01d2f9" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="639" height="163" alt="image" src="https://github.com/user-attachments/assets/1f6d3acb-8df1-4d00-a9a4-a5344567fc9c" />


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

<img width="450" height="130" alt="image" src="https://github.com/user-attachments/assets/a27e7b33-27ee-4747-813c-55eb9881c13f" />


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


<img width="421" height="83" alt="image" src="https://github.com/user-attachments/assets/0f708046-373b-4d82-b822-eff124452dba" />


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


<img width="624" height="235" alt="image" src="https://github.com/user-attachments/assets/de9ecb6d-9b14-4586-b9dc-f9389e18eda7" />


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


<img width="687" height="202" alt="image" src="https://github.com/user-attachments/assets/49b89756-3aa0-4853-bae1-abda921f1800" />


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


<img width="727" height="160" alt="image" src="https://github.com/user-attachments/assets/37aaec60-e7f8-4a90-a4dc-268333c62ef3" />


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


<img width="677" height="171" alt="image" src="https://github.com/user-attachments/assets/55211a9a-127c-478b-86f7-429bf17d28f5" />


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


<img width="565" height="171" alt="image" src="https://github.com/user-attachments/assets/80af67ba-2117-4e26-a74e-496b744128b7" />

 
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
 


<img width="708" height="376" alt="image" src="https://github.com/user-attachments/assets/78e1a237-1bb2-4921-92a3-713a36abec53" />

 
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
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```

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


<img width="507" height="226" alt="image" src="https://github.com/user-attachments/assets/e3f99a35-c7ef-4b17-b321-ce6401c57220" />


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


<img width="572" height="182" alt="image" src="https://github.com/user-attachments/assets/e7003737-1cbc-4b1b-b1d3-f6565004d9f4" />


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


<img width="479" height="182" alt="image" src="https://github.com/user-attachments/assets/bd67bfce-0ca7-4b9e-ba50-3128e94630df" />


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


<img width="505" height="272" alt="image" src="https://github.com/user-attachments/assets/d452f9cc-8765-49ea-ac3a-87dd56fa90e7" />

 
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


<img width="466" height="131" alt="image" src="https://github.com/user-attachments/assets/85a4daef-703b-4c39-9af2-1ef0e7feefc9" />


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


<img width="528" height="152" alt="image" src="https://github.com/user-attachments/assets/32389a62-c375-4863-ad2b-6bcd734cbe49" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="469" height="114" alt="image" src="https://github.com/user-attachments/assets/b45c71ca-6c49-4a4e-b04f-30b668a0a709" />


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


<img width="453" height="145" alt="image" src="https://github.com/user-attachments/assets/2f296419-9182-4065-acff-10ce7204cede" />

 
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


<img width="452" height="177" alt="image" src="https://github.com/user-attachments/assets/23fe69a0-7c6f-4e5a-a790-ff9d56ee73e7" />


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


<img width="522" height="127" alt="image" src="https://github.com/user-attachments/assets/8cd6d7d4-3d66-47f3-a4de-b290f5e406b1" />


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

<img width="835" height="105" alt="image" src="https://github.com/user-attachments/assets/e452454b-8199-4b80-8c32-d161fa874e18" />

 
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


<img width="727" height="480" alt="image" src="https://github.com/user-attachments/assets/dddb4003-5f42-4d78-99c1-5e2257aba66f" />


# RESULT:
The Commands are executed successfully.
