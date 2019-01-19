# Environment Setup
Install the Postgresql and MySQL by running
```
$sudo apt-get update
$sudo apt-get install postgresql postgresql-contrib
$sudo apt-get update
$sudo apt-get install mysql-server
```

# Configure User Role & Database
Set up user role and password for specific user and change the corresponding field in demo_init.py. Enter the interative shell/client of postgres and mysql and create corresponding database
```
CREATE DATABASE argo;
CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'localhost';
```

# Timing Experiment Query 
All experiment queries contains in the argo/experiment folder. Run the query by moving them out. The script will generate all time results in corresponding text file. Same for argomysql.
```
cd ~/argo/experiment
mv * ../
./run-test.sh
```
# Run other query
Simply run 
```
python demoshell.py
```
It will enter the shell and write SQL-like sentence from argo.
