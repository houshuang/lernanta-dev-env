
====================
P2PU Development Environment
====================

Easy setup:
-----------
1. Download and install VirtualBox https://www.virtualbox.org/wiki/Downloads
2. Download and install Vagrant http://downloads.vagrantup.com/tags/v1.0.3
   - or alternatively run 'gem install vagrant' if you have a working ruby environment
3. git clone http://github.com/p2pu/lernanta-dev-env.git
4. cd to the project directory and type "vagrant up"

Terminology:
-----------
 * Host machine: Your computer that you are using now
 * VM / Guest Machine: The 'virtual machine' that is running inside vagrant. This is where the webserver lives.
 * Project Directory: The directory that you clone this project into.

How to Use:
------
 * vagrant resume to start the lernanta environment
 * vagrant suspend to shutdown the lernanta environment
 * You can access the server from localhost:8001 from your host machine
 * You can ssh to the server by typing 'vagrant ssh' from the project directory
 * The lernanta directory is shared between the vm and the host. Use your favorite editor to edit the code in this directory and it will be reflected inside the vm (Django will reload files automatically). 
 * The lernanta directory is pulled from http://github.com/p2pu/lernanta. To update to the latest code, use git pull origin master.
 * More info here http://vagrantup.com/v1/docs/getting-started/index.html

Tips:
-------
 * vagrant ssh
 * tail -f /opt/lernanta/lernanta/webserver.log
 
Troubleshooting:
----------------
 * If there is a problem:
 * cd into the project directory
 * vagrant destroy
 * vagrant up
 * Local modifications to your code will stay in the lernanta folder. 
