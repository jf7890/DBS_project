Run command:
chmod +x permission.sh

./permission.sh

docker-compose up -d --build

Now, exec to MySQL container and test some basic command such as: 
show databases;
use mysql;
show tables;
...
or try to create user and grant permission
and then get back to host to check /logs/mysql.log to see if logs have been written.
if not, exec back to mysql container and run command:
SET GLOBAL general_log = 'ON';

