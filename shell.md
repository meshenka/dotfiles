# Usefull shell commands

## Rerun as sudo

```sh
apt update
sudo !!
```

## Start editor

```sh
//start the default editor
ctrl-x+ctrl-e
```

## Mount a ramdisk

```sh
mkdir -p /mnt/ram
mount -t tmpfs tmpfs /mnt/ram -o -size=256M
```

## Avoid writing command to history

With a leading space

```sh
 ps aux
```

## Fix long command 

fc allow last command edition in default editor
(notice the missing - on Accept: applicaiton/json header)

```sh
curl -XPUT https://test.org:8080 -d "{id:77,name:test}" H "Accept: application/json" -H "Content-Type: application/json" 
fc
```

## Ssh tunnels

local port 3337 to remote host's 127.0.0.1 on port 6379

```sh
ssh -L 3337:127.0.0.1:6379 root@remote.org -N
```

## Create folder structures

Create a bunch of folders with one command

```sh
mkdir -p ~/folder/{sub1,sub2}/{1..100}
```



