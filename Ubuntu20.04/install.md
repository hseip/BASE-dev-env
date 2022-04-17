## Install DEV on Ubuntu 20.04
### Install Git
Open the terminal.
git --version

if git does not exist on the local machine then install it. Find instructions here: https://www.atlassian.com/git/tutorials/install-git


sudo apt install git
git config --global user.name "FIRST_NAME LAST_NAME"
git config --global user.email "MY_NAME@example.com"

### Github
Create a Github account at github.com
Enable 2FA. Use Authenticator App
Create a personal access token:
Settings -> Developer Settings

Create a personal access token to push code to Github by clicking "Generate new token"
Select boxes for:
repo
write packages

Click the "Generate Token" button. Save the generated token in a safe location. The token is shown only once.


### Install VSCode:
sudo snap install --classic code



### Install MySQL
Instructions: https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04


sudo apt update
sudo apt install mysql-server
sudo systemctl start mysql.service

sudo mysql_secure_installation

VALIDATE PASSWORD COMPONENT can be used to test passwords
and improve security. It checks the strength of password
and allows the users to set only those passwords which are
secure enough. Would you like to setup VALIDATE PASSWORD component?

Press y|Y for Yes, any other key for No: N


Please set the password for root here.



By default, a MySQL installation has an anonymous user,
allowing anyone to log into MySQL without having to have
a user account created for them. This is intended only for
testing, and to make the installation go a bit smoother.
You should remove them before moving into a production
environment.

Remove anonymous users? (Press y|Y for Yes, any other key for No) : Y


Normally, root should only be allowed to connect from
'localhost'. This ensures that someone cannot guess at
the root password from the network.

Disallow root login remotely? (Press y|Y for Yes, any other key for No) : Y


By default, MySQL comes with a database named 'test' that
anyone can access. This is also intended only for testing,
and should be removed before moving into a production
environment.

Remove test database and access to it? (Press y|Y for Yes, any other key for No) : N

Reloading the privilege tables will ensure that all changes
made so far will take effect immediately.

Reload privilege tables now? (Press y|Y for Yes, any other key for No) : Y

All done! 



sudo mysql


mysql> CREATE USER 'hseip'@'localhost' IDENTIFIED BY 'blablabla';

mysql> create database BASE;

mysql> grant all privileges on BASE.* to 'hseip'@'localhost';

mysql> FLUSH PRIVILEGES;

mysql> exit;


### Install MySQL Workbench
Download from https://dev.mysql.com/downloads/workbench/

Then doubleclick on .deb file in Filemanager

 
### Install Node.js

sudo apt update

sudo apt install nodejs

node -v

sudo apt install npm


### install curl
sudo apt install curl


### install Node version manager
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
source ~/.bashrc

nvm install v16.14.2


### install yarn

echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

sudo apt install yarn

npm install --global yarn

### install Quasar/Vue3
npm i -g @quasar/cli



