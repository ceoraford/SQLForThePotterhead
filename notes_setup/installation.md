I used homebrew, and followed the instructions [here](https://wiki.postgresql.org/wiki/Homebrew)
```sh 
#install postgres via homebrew 
brew install postgresql 

#start the postgresql service
`brew services start postgresql`

#connect via psql TODO: explain what is psql
`psql postgres`

# List all the databases 

postgres=# \l
                             List of databases
   Name    |  Owner   | Encoding | Collate | Ctype |   Access privileges
-----------+----------+----------+---------+-------+-----------------------
 postgres  | <YOUR_USERNAME> | UTF8     | C       | C     |
 template0 | <YOUR_USERNAME> | UTF8     | C       | C     | =c/<YOUR_USERNAME>          +
           |          |          |         |       | <YOUR_USERNAME>=CTc/<YOUR_USERNAME>
 template1 | <YOUR_USERNAME> | UTF8     | C       | C     | =c/<YOUR_USERNAME>          +
           |          |          |         |       | <YOUR_USERNAME>=CTc/<YOUR_USERNAME>
(3 rows)

#create a new database 
CREATE DATABASE potter;

#connect to it 
\c potter
```