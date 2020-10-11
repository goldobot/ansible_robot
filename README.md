# ansible_robot

Prepare the ansible master

Prepare the raspberry pi:
Flash the sd card with a fresh image of raspbian 10
Enable ssh access by writing an empty file named ssh on the sd card root partition
Create a user named ansible, with "raspberry" as the password and add it to the sudo group
Add the ansible master ssh public key to the raspberry pi ansible user's .ssh/authorized_keys file
Now the ansible master can ssh into the raspberry without password prompt.



Install ros
execute the following command on the ansible master:
ansible-playbook -i hosts ros.yml
ros compilation mmight take up to one hour