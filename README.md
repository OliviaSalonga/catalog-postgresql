The IP address and SSH port so your server can be accessed by the reviewer.
-----------------------------------------------------------------------------
ip address: 52.89.88.40
port: 2200

The complete URL to your hosted web application.
-----------------------------------------------------------------------------
http://ec2-52-89-88-40.us-west-2.compute.amazonaws.com

A summary of software you installed and configuration changes made.
-----------------------------------------------------------------------------
* General configuration changes
  - Change local timezone to UTC
  - Change Uncomplicated Firewall configrations
  - Change SSH port in /etc/ssh/sshd_config
  - Configured /etc/hosts and /etc/hostname to contain the correct host & ip address
  - Changed /etc/ssh/sshd_config to have the folloing configurations: (1) 'PasswordAuthentication yes' to enable user to ssh to server using a password, (2) 'PermitRootLogin no' to disable root ssh login, and (3) 'AllowUsers grader' to only allow grader user to log in to the server 
    
* Finger

* Apache2
  - Run 'sudo a2enmod cgi' to give Apache permission to run scripts
  - Configured /etc/apache2/sites-enabled/catalog-postgresql.conf file 
  - Configured /etc/apache2/apache2.conf to set global ServerName 
  - executed 'sudo service apache2 restart' after file change above

* Mod_wsgi
  - Configured /var/www/catalog-postgresql/catalog-postgresql.wsgi
  
* Python setuptools
  -  Note:  Python is already installed.

* libapache2-mod-wsgi
  - Configured /etc/apache2/sites-enabled/catalog-postgresql.conf file 
  - executed 'sudo apache2ctl restart' after file change above.

* Python-psycopg2

* Django
  - set DATABASE in settings.py

* Python-dev

* Python-pip

* Python-flask-sqlalchemy

* Flask
  - set database in __inti_py

* Virtualenv

* PostgreSQL
  - Do not allow remote connections is the default of the installation.  No additional configuration is needed.

* Git
  - Create .htaccess file in root directory to avoid web access of .git file.  The file contains "RedirectMatch 404 /\.git".

* Git clone <project git hub url> from /var/www directory.  (This creates /var/www/catalog directory and clone all files of the project.) 
  - Executed 'chmod 711 *.py' to make the script executable 

* net-tools
  -  To run netstat and see network connections linked to the machine  


A list of any third-party resources you made use of to complete this project.
-----------------------------------------------------------------------------
* Change timezone to UTC 
  - https://help.ubuntu.com/community/UbuntuTime#Using_the_Command_Line_.28terminal.29
* Add new user and give sudo permissions 
  - http://askubuntu.com/questions/7477/how-can-i-add-a-new-user-as-sudoer-using-the-command-line
  - https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-12-04
* Change root ssh log in permission
  - https://mediatemple.net/community/products/dv/204643810/how-do-i-disable-ssh-login-for-the-root-user
* Enable server users to SSH to server using a password
  - https://help.ubuntu.com/community/SSH/OpenSSH/Configuring
* Update & Upgrade software  
  - https://wiki.ubuntu.com/Security/Upgrades
* Configure Uncomplicated Firewall 
  - https://www.digitalocean.com/community/tutorials/how-to-setup-a-firewall-with-ufw-on-an-ubuntu-and-debian-cloud-server
* Install Apache, Python, mod_wsgi, PostgreSQL 
  - http://blog.udacity.com/2015/03/step-by-step-guide-install-lamp-linux-apache-mysql-python-ubuntu.html 
* Configure Apache 
  - http://drumcoder.co.uk/blog/2010/nov/12/apache-environment-variables-and-mod_wsgi/
  - https://help.ubuntu.com/lts/serverguide/httpd.html
  - https://www.digitalocean.com/community/tutorials/how-to-configure-the-apache-web-server-on-an-ubuntu-or-debian-vps
* Configure PostgreSQL
  - https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-14-04
* Create PostgreAQL user
  - https://www.postgresql.org/docs/9.1/static/app-createuser.html
* Manage PostgreSQL tables
  - https://www.digitalocean.com/community/tutorials/how-to-create-remove-manage-tables-in-postgresql-on-a-cloud-serve
  - https://www.youtube.com/watch?v=PJK950Gp780 
* Convert SQlite to PostgreSQL
  - https://discussions.udacity.com/t/how-to-move-a-flask-app-from-using-a-sqlite3-db-to-postgresql/7004/5
  - https://www.digitalocean.com/community/tutorials/
* Grant data base roles  
  - how-to-use-roles-and-manage-grant-permissions-in-postgresql-on-a-vps--2
* Configure mod_wsgi   
  - http://flask.pocoo.org/docs/0.11/deploying/mod_wsgi/
* Setting the global ServerName
  - http://unix.stackexchange.com/questions/155150/where-in-apache2-do-you-set-the-servername-directive-globally
* Django installation and configuration
  - http://postgresapp.com/documentation/configuration-python.html 
  - https://www.digitalocean.com/community/tutorials/how-to-use-postgresql-with-your-django-application-on-ubuntu-14-04 
