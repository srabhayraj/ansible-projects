## Welcome to Ansible project

![Image](https://github.com/Chandrashekhars816/ansible-projects/blob/master/icons/ansible.png)

## 1. what this project does?
```markdown
~  This project does configure the following tasks:

       a) install jenkins servers.

       b) Rhel 8 iso yum configuration.

       c) pull the docker images that you want from the dockerhub ( only those that don't require you to login ).

       d) some additional tasks such as screen resolution inside virtualbox vm of rhel 8.
 
       e) It will also install jupyter and some python libraries used for machine learning projects.

       f) all you need to configure the roles according to your requirements.

       g) It will give you very simple commands to push and commit ( fast commit ) all you need is to configure some things for these commands to work easily.

          Such as: 

          1. ssh-key public key must be given of the user which will be used for pushing and pulling as well as commiting as 'fast commit'
             
           **known bugs:
                    - push will fail when there's unrelated history files on the remote repo.

                    - It will only push at master remote branch.**
```
## 2. What are prequsites?
```markdown
       a) Ansible must be installed.
      
       b) All the controlled nodes must have given ssh key access for login and don't require the passwords.

       c) Controller node must have entry in thier host files with the alias for the remote nodes as the file is at /etc/hosts and entry should be like:
       `127.0.0.1   localhost localhost.localdomain localhost4 localhost4.localdomain4
        ::1         localhost localhost.localdomain localhost6 localhost6.localdomain6
        192.168.43.128 server1
        192.168.81.43  server2
        192.168.97.84  server3`
      
     **d) It will only work in RHEL 8 version.**
```
## 3. How to use?
```markdown
       1. Go to the inventory file ( hosts ) in your current directory:         
       To install jenkins: 
       a) Change your inventory file from such that:
     **`[jenkinsservers]
        localhost`**

                   To

     **`[jenkinsserver]
        server1
        server2
        server3

        [machine]
        server1
        server2
        
        [resolution]
        server1
        server2
       
        [registry]
        server1
        server2`**


       2. run the command `ansible-playbook setup.yml`
```
## 4. How to browse your wordpress site on the container

```markdown
       1. Go to the terminal.
       2. type command "ip addr"
       3. notice your ip and the wordpress server is running on 8082 port.
       4. Open your windows browser and type in url http://[the above step i.p.]:8082 
       5. Well here goes your wordpress server deployed on the container
```

### Contact

**Having trouble with using the project? Connect me on LinkedIn [Chandra Shekhar Sharma](https://www.linkedin.com/in/chandra-shekhar-s-a76b37158/) will help you sort it out. CIAO)/**
