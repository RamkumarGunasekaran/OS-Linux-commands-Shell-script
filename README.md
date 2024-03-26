## NAME: RAMKUMAR G
## REG NO:212223220084

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
![1](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/10649990-14fe-4fa1-99c3-5923d2b4041f)


cat < file2
## OUTPUT
![314976091-5efa87e6-0d63-4d21-9c17-8ea4c9f869ac](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/8444188a-6b95-4959-9b4b-3bd26434948f)



# Comparing Files
cmp file1 file2
## OUTPUT
![314979500-2369bf72-0c7e-4a4a-8d9c-f2817448649e](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/0461b10e-d409-4182-8c50-35ce14860123)

 
comm file1 file2
 ## OUTPUT

 ![314980658-34b7d485-8cd4-4686-ba34-2c670fcaafb5](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/f898a817-39f3-4a70-a79a-0853b5e7478b)

diff file1 file2
## OUTPUT

![314981548-af7bc968-5664-4eea-aecb-510f6fd2806c](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/9a640589-96e9-462d-be4f-35650b67847c)

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

![314982781-c924d3c5-77d0-4d43-ab9a-9df9b570c884](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/6d6fed07-f4d0-4dfa-b733-c8a5b3e553ec)



cut -d "|" -f 1 file22
## OUTPUT

![315045147-a1ade342-d6f7-40e0-bc3d-a2114ba4393b](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/4d809497-5176-48ac-9653-4d4c69aca4ac)


cut -d "|" -f 2 file22
## OUTPUT

![314984927-a785b063-a475-49fe-86ab-87934f42de4f](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/48143bc7-7004-4d19-865c-0e15fdb3c0ca)

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
![315045367-918fd2d1-a5c2-44b3-8857-af3a62a3dd90](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/98d7f3da-33f3-46f9-9608-b774f0f6d3c7)



grep hello newfile 
## OUTPUT
![315045509-98b182a7-0843-4e15-9c9b-64bc6c808b4d](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/73bf8e93-37bc-40f9-b783-e87865f1e7d1)




grep -v hello newfile 
## OUTPUT

![315045682-73054690-36c2-4d1a-b158-b68a7b6b3507](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/23b14ee4-329f-48fd-8cb8-28e6d05995c5)


cat newfile | grep -i "hello"
## OUTPUT
![315045958-969653d1-89f7-4706-82dc-1f4780c78fdd](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/6b9fe234-8e54-4e5a-990b-542a712d8e05)




cat newfile | grep -i -c "hello"
## OUTPUT

![315046072-844132bd-b8b5-4215-ba32-ba489c0d6014](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/184856ed-d3db-4004-9c3a-e33ce17469b3)



grep -R ubuntu /etc
## OUTPUT


![315049198-c7ce112d-af5e-4d92-a968-c92781ded17e](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/6347f4a7-1cbd-4fad-ace4-afc3c51648f1)

grep -w -n world newfile   
## OUTPUT
![315049293-efc11869-fbbb-4274-a95e-b9fc5d38d7b8](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/3226e7d9-5098-42ae-ab55-782e4ebd53d6)


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


![315049431-f340880e-10a0-4153-a6e8-24f5803eb3d0](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/84a3944b-d701-4389-8c5d-bebae9e51d84)

egrep -w '(H|h)ello' newfile 
## OUTPUT

![315049510-bc13760c-523b-4bc9-a248-86612f8457aa](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/8a2ebc66-d401-451d-b542-e0a770079890)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![315049638-d52fc186-1711-4f61-b721-46c43149f75b](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/213d27f6-37ef-4996-825f-975a34cea02a)


egrep '(^hello)' newfile 
## OUTPUT

![315049697-dafcaa24-98f8-461c-834a-90a0f9f22042](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/5748022c-efed-48cb-a798-9f51c9d1b6c3)


egrep '(world$)' newfile 
## OUTPUT
![315049807-e5b7a566-53ac-4c40-81d8-e92251d84705](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/18b005d7-d019-460f-8899-601177a9394e)



egrep '(World$)' newfile 
## OUTPUT
![315049949-db9b134b-2f67-4831-88f1-dd376546a9b1](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/56ecd425-2602-471e-b124-bb95ba605501)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![315050030-07b2b361-19d2-4325-a80f-90ee10da31a1](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/892cecf5-b807-49ad-9b4b-4299a4fe3907)



egrep '[1-9]' newfile 
## OUTPUT
![315050100-e65b1028-bdfc-4c9d-80a5-690869d58baa](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/5fb304bf-b189-4aa0-a750-b9b3867e37af)



egrep 'Linux.*world' newfile 
## OUTPUT

![315050187-717e504e-9ee0-45dd-8a43-20c54ce25e1a](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/13e990e1-4c83-4261-8fc4-8f564f2157fa)

egrep 'Linux.*World' newfile 
## OUTPUT
![315050289-dba5e101-51b6-43cc-8fd4-24fda134e0e5](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/8c0d5f90-18d0-4795-8b58-65d470e2cf40)


egrep l{2} newfile
## OUTPUT

![315050364-77c4514f-f813-4c19-9398-e84c99e4ecf9](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/c2c5dcaf-ba7f-44f5-9ddf-e3130dcd3410)


egrep 's{1,2}' newfile
## OUTPUT 

![315050423-061d3ce2-4e67-4c87-88a4-18bf33137c2f](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/04cc0cfc-a004-4bce-bc5a-4c32951de81c)

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

![315050538-935675a0-9795-429f-b332-dac1a0df4585](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/442fd4dd-ffdf-4fa4-9b6c-4dfdc9b49419)


sed -n -e '$p' file23
## OUTPUT

![315050604-2c858b0e-ab68-440a-8444-7d752e2bb87f](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/7d58c6e3-e0c4-4d61-b82a-a1c53f9539e1)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![315050689-171431fb-405a-46a2-a389-9bff3f7d5fd9](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/e9b40e04-e9ee-484e-a5b9-88979eac4a3b)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![315050770-3f7eb83f-3849-4559-8f9b-fd44dde88d9c](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/02b19fb6-56f9-40a4-8593-6ebb23eeaddd)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![315050832-3d05d047-9edd-414c-bd64-180a50cb67bd](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/74f40683-f6fa-4530-8f31-2dde4e8d3e9a)



sed -n -e '1,5p' file23
## OUTPUT

![315050939-3c3c8c82-64bf-4a61-b74d-0e4894fd0cce](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/354bbd4d-3adf-495e-8296-611c0921b0af)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![315051095-4a9ec8d2-4043-430b-bd3c-37e9ba77753b](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/eb615e73-04d8-49ae-8777-b609a6266734)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![315051183-f10b3ec1-8b19-481e-8dc0-c5aecdc79256](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/7d9d96a0-8b82-48b3-b704-ecc6adbd3f54)


seq 10 
## OUTPUT
![315051279-4d45e5ad-1b87-4e1b-ae3d-80a3c2499b88](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/3e8a5134-dc9e-4159-a82c-2ffd311a6e94)



seq 10 | sed -n '4,6p'
## OUTPUT

![315051338-c599a819-c954-40cc-97b4-e0ba9840f76a](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/efad87a3-0200-4183-946b-6dd1c8cefa25)


seq 10 | sed -n '2,~4p'
## OUTPUT

![315051433-31847249-709d-4f4c-8a36-933006e8c918](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/ed4ec424-3c45-4f22-b5a6-561e6e3d6c61)


seq 3 | sed '2a hello'
## OUTPUT

![315051499-4e1e44e1-0275-4115-9eeb-17dca6edb024](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/c81f4af2-f99a-4333-9468-1241436c99d4)


seq 2 | sed '2i hello'
## OUTPUT
![315051661-d4f040d9-b131-4c9f-b4bc-a232b3925822](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/fa1ffcd7-aacd-4c7c-b39f-2eaae19d31ad)



seq 10 | sed '2,9c hello'
## OUTPUT
![315051782-66d090d9-1141-4440-90d6-b6904930420e](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/2fc660b1-d176-4bae-9aec-69d71ce998e2)



sed -n '2,4{s/$/*/;p}' file23


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
![315052060-f22c53a2-d867-44ff-b973-51aabcfea661](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/15c00164-45e2-47c4-a92d-c1ff8f774f56)


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

![315052122-54b9d1b8-9935-40d1-8d31-24579af43011](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/d4a9cbc6-a685-49f6-a18d-86d76c838dbd)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![315052200-ec3da3c1-d6e9-4626-8e83-f5ebac077abd](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/60c8508d-fe88-4e05-8c52-673f261bb667)

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
![315052283-f0764e0d-496d-4b50-bed3-12af4f1247ee](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/caabbe3b-8957-4ad3-b871-3b4387d13be0)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![315052353-510df307-db0f-45da-aa4e-53b487854204](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/8a41f4ee-819e-4b80-b69d-f626d57594a0)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![315052467-eeb22489-13ad-4c16-8b3c-80b265c56342](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/ef013e11-29f4-41b4-94b6-edd79b89514c)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![315052555-03050655-c052-4079-bdd0-0c1c456396e5](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/0d724c29-286c-4075-b691-3e9d7ec74293)


tar -xvf backup.tar
## OUTPUT
![315052687-a8ba39c2-8596-4d5f-a90d-591c27ecd8f9](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/06d2c20e-9f7b-47ca-8021-da20d110ef6a)

gzip backup.tar

ls .gz
## OUTPUT
 ![315052909-0fcbfd6d-d13c-48bc-a517-f6ff9f64cdb6](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/44f69784-886d-4ff5-9fee-8e9d4a1cdb83)

gunzip backup.tar.gz
## OUTPUT
![315053010-9a516b72-0dbb-426b-80cd-a0c35dbe56b9](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/26bc5c65-491a-4266-b927-2d737b58dbd5)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![315053091-944a6318-0993-41f0-83a3-4e0d31c7747b](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/16fa152c-cd29-4ce0-af5b-d6742696b4fb)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![315053142-a67ef2a8-efa1-4d30-b46f-c4d8d9aff6f6](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/2c47f141-d832-48d1-b9d6-7bbf82cbf5e1)


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

 ![315053210-3bf7acf6-ced2-49b4-8c26-3aee860d283d](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/04d38b11-d833-4cda-a2fe-0d64456b10a2)

ls file1
## OUTPUT
![315053259-062e9d43-b487-4175-9d66-638f4eae8124](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/ed8ca02f-baae-46d1-9b0c-e2b4785637ff)

echo $?
## OUTPUT 
![315053330-b3dc11e7-1fb9-42eb-9fc0-5dee991a740a](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/19e4213d-081b-4bd2-aaf0-f829149eb5ea)

./onebash: ./one: Permission denied
 
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
## OUTPUT
![315053463-d3c586d5-7711-4037-bef5-a5471159e95d](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/32ea02fc-5cb7-4622-9ae0-bbbcb9592f3b)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![315053534-802c33b4-9293-4c1e-a42e-03b3001bd464](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/e72cdb9b-88cd-4bc5-bc8c-020f73fee2ef)


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
![315053714-0767a906-2530-4dc9-b718-f9df8f324d56](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/423451dd-bf52-411d-830b-5966244f49d4)

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


![315053769-2af720ff-fe3f-4448-b7de-6bbc53f400e0](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/abe520b6-76c0-4ede-a039-66f0475c6780)

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
![315053877-dd76eefb-8f02-47ed-b214-bcedadd6fac3](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/d40c1359-7f73-4d0e-9f3b-9c3d1befb1e6)

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
![315053935-0d818d8b-f359-4a2d-bcc9-33c4d8eb2e2a](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/f9a0f615-ea6d-4c52-b4e6-1fff8e290f14)


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
![315053978-60f3ced8-cf0f-4712-a8b1-799d7e7597b5](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/39a7cd91-2374-496f-a6d6-76c8300dc450)


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
![315054040-8ec298bf-4359-4da2-9872-c2c13b620661](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/d2605f86-9733-4f78-839f-b7b84b43b72e)

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

 ![315054306-2e1927ad-e4fb-429e-8220-dcb542af2b1b](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/bbf23f34-d989-48b8-b84e-270ff33845fd)

cat > whiletest.sh
```
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
 ![315054465-b43d560e-1485-41e9-a36c-c529930a5bd2](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/ddf2836a-aff7-4635-8df4-5d8a3bff4d83)

 
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
 ![315054536-690a4c5c-abde-49ba-845e-9d3aed194677](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/522c8a03-845d-4d21-92be-c6f304360d30)

 
 
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
 ![315054777-a4c8db23-b308-4106-93b7-20c4c0e30fbf](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/44517c2d-0864-4977-bf8a-4278a9ae9039)

 
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
cat forin2.sh
```
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
 
$ ./forin2.sh 
 ## OUTPUT
 ![315055032-0541fbbd-8226-43ed-a89e-746691689be3](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/1c3ffaad-56ee-4e40-be32-a112f8e47756)

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
## OUTPUT
![315055405-d91349d5-3f02-4fe8-8c30-56eae0bd5908](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/842bfff0-c002-48e9-907e-e524230684d7)

$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![315055193-5a2a72e8-7829-4a2a-aa50-d45b84acae28](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/f321bcb6-633b-4ce5-b569-fb902dff0463)


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
![315055298-ee0760bc-1152-48ec-8c28-bfb9699bf539](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/27c92b6b-ee06-4840-b5fa-b05475e3f7ce)

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
![315055544-d2b9b477-6a26-4eff-8ad9-1ef84070fd13](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/664cd778-ade8-4bf2-9b04-de9619038aa7)

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
 ![315055599-7a6b46e9-a024-46d4-9770-51057f95ae6c](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/b1cd3217-98ee-4a13-bf18-4726d3dd0327)


 
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
 ![315055840-86ddc8e8-f42d-4e7d-bb4b-e1cc69bb8625](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/0765d54a-32b7-4dab-aee7-73ba559f2404)

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

![315055880-32c1adce-cb5d-44c2-8050-b35d2fa6c778](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/199c23aa-0ad2-43c1-be6f-633842b9fac4)

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
![315055954-bc56e21d-c2ed-44c4-a627-a651370559fd](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/7ee0fda7-4aee-48b9-b66c-db62420186d5)

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
[315056163-654bba20-181a-4810-8919-6f5d5e990f32](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/d0fd2ccc-8439-46b4-b072-8a78cd3503db)

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
 ![315056365-5724f3a3-fc08-4383-b0f1-1314f98e019e](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/fbf0ccbc-30fd-4ba9-8017-efa27261d721)

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
 ![315056280-e954b54f-ca35-4f34-bf46-9d87602e221e](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/b564ab36-5649-4d4f-b1e4-a269609ab7d7)

 
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
 ![315056163-654bba20-181a-4810-8919-6f5d5e990f32](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/d0fd2ccc-8439-46b4-b072-8a78cd3503db)
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
![315056117-4c86ecae-a50d-4a9d-8146-78ad4d1d4a20](https://github.com/RamkumarGunasekaran/OS-Linux-commands-Shell-script/assets/144870820/1daf5b3a-3394-47b0-ac6f-32a86e8c83f0)


# RESULT:
The Commands are executed successfully.
