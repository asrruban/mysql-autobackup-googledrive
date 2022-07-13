# mysql-autobackup-googledrive

The final command will be like the following, Type it in the terminal then click enter
./backup.sh mysqlbackup test_db root pass123 drive BackupFolder
After executing the command type “ls” in Terminal you will find mysqlbackup folder which you passed as a parameter.
Now go to mysqlbackup folder by typing “cd mysqlbackup” then type “ls”you will find a dumped Database file
Now go to Google drive Check your folder you will find a Backedup Database
Now we are going to automate our script using crontab

nano /etc/crontab
Add the below line in your crontab file
0 11 * * * root /backup.sh mysqlbackup test_db root pass123 drive BackupFolder
