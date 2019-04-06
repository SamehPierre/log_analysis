
# Log Analysis Tool

## Project purpose
Its a reporting tool that will use information from the database to discover what kind of articles the site's readers like in a newspaper website.

## It has three functions:
1. popular_three_articles().
Results are the most popular three articles of all time.

2. popular_authors().
Results are the most popular article authors of all time.

3. more_than_one_percent().
Results days in which more than 1% of requests lead to errors


## The project code requires the following software:
Python 3.7
psql (PostgreSQL) 9.5.16
vagrant 2.2.4


For this you will need Vagrant and VirtualBox software installed on your system.
You can find:

Vagrant from [here](https://www.vagrantup.com/downloads.html)
VirtualBox from [here](https://www.virtualbox.org/wiki/Downloads)

## Project contents
### This project consists of the following files:

newsdatadb.py - The Python program that connects to the PostgreSQL database, executes the SQL queries and displays the results.
output.txt - A plain text file that is a copy of program's output. 
README.md - This read me file.


## How to Run it:
After installing VirtualBox and Vagrant you will need to use GitBash or command prompt for windows, terminal screen in Linux, browse to the  project directory.

## Start the virtual machine:
From your terminal, run the command <h6> vagrant up</h6>. It should take awhile for the first time in order to download the vm image.
Then you can log into the VM by using this following command ###### vagrant ssh.

## Download the DataBase:
#### You can download the database from [here](https://d17h27t6h515a5.cloudfront.net/topher/2016/August/57b5f748_newsdata/newsdata.zip)
You will need to unzip this file after downloading it. The file inside is called newsdata.sql. Put this file into the vagrant directory, which is shared with your virtual machine.

cd into the vagrant directory and use the command 
###### psql -d news -f newsdata.sql.

This command will connect to the database server and exeute query which will create the tables for the database and populate them with data.

## Now Everything is Setting up:

You can run the reporting tool using this command 
###### python3 newsdata.py

## Logging Out from the VM:
 press Ctrl-D, then shut down use this command "vagrant halt" 
