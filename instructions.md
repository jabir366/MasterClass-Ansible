# Instructions 

   These instructions are for those who are using Ubuntu system 

## Install Ansible  on Ubuntu

https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible
   - If pip is not installed use this command to install pip
       `sudo apt-get install python3-pip`   
   - To install ansible from pip 
       `pip install ansible`
   - To install from apt
      ``` $ sudo apt update
          $ sudo apt install software-properties-common
          $ sudo apt-add-repository --yes --update ppa:ansible/ansible
          $ sudo apt install ansible
      ```
 Setting up environment
   - create 2 Virtualbox VMs with brige networking interfaces (note the usernames and passwords) usernames labuser1 and labuser2 
   - Ensure that openssh-server is installed and running in VMs. use command `sudo service sshd status`
   - Install openssh-server if not already installed .   `sudo apt update; sudo apt get install openssh-server`
   - If the ansible host doesn't have ssh-key pair generated , do it using `ssh-keygen` 
   - To copy public-key of ansible machine to other hosts ,use `ssh-copy-id`
   - In each VM , you need to allow the user to not prompt password while issuing command with sudo, for that type command `visudo` in terminal and edit the line containing 
      ```%sudo   ALL(ALL:ALL) ALL``` 
      to
      ```%sudo   ALL(ALL) NOPASSWD:ALL```
   
* configuring ansible 
  - If ansible is installed from pip use this command to dowload the default ansble.cfg
   `sudo wget -O /etc/ansible https://raw.githubusercontent.com/ansible/ansible/devel/examples/ansible.cfg`  .
   If installed using apt, it will be there already
   
   
  
  
