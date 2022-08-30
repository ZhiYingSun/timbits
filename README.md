# timbits
code snippets that could be useful -- and should be scripts 

## AWS EC2 Snippets

ssh - can also find it in connect to instance under ssh

```
 ssh -i "key.pem" ec2-user@[Public DNS]
```

keep EC2 instance running after SSH is terminated

```
echo -e "to keep the mistr running in background"
screen -d -m go run main.go

echo -e "to list the available screens"
screen -ls

echo -e "to quit the session"
screen -X -S [session you want to kill] quit
```

copy files from local to remote aws ec2 instance
- you should probably just pull with git

 ```
 scp -i mistr.pem main.go ec2-user@[Public DNS]:
 
 scp -i mistr.pem -r  ~/Documents/GitHub/mistr ec2-user@[Public DNS]:
 ```
