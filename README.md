#Before you begin be sure have all the proper software installed to get started:
 - virtualbox
#Create your vm using vm manager
#When you have your vm up and running open a Terminal window.
#You will need to install several packages and run a few commands
#First run sudo apt-get update 
 - This will update all the packages for the software
#Run sudo apt install git
 - This will assist with the github repository that will be downloaded
#Now run git clone https://github.com/gustanik/CNA350
#Now change directories using by typing cd CNA350/maxscale
#Type sudo apt install docker-compose
#Type docker-compose up -d
- pulls up the databases
#Run sudo docker-compose -f"docker-compose.yml" up -d --build > help.txt
- creates master's and slaves
#In maxscale folder run mysql -u maxuser -pmaxpwd -h 127.0.0.1 -P 3306 -e "SELECT * FROM zipcodes_one.zipcodes_one LIMIT 7;
- Also run run mysql -u maxuser -pmaxpwd -h 127.0.0.1 -P 3306 -e "SELECT * FROM zipcodes_two.zipcodes_two LIMIT 7;
- Selects the limit of 12 zipcodes with information. The output will be zipcode, zipcode type, city, state, location type, coord_lat, coord_long, location, decommisioned, taxreturn fields, estimated population, and total wages for both queries.
#Run sudo apt install  mysql-client-core-5.7
- install mysql client
#You will also need sudo apt install mariadb-client-core-10.1
output
+-------+
| State |
+-------+
| PR    |
| PR    |
| PR    |
| PR    |
| PR    |
| PR    |
| PR    |
+-------+
#Run sudo apt install make. enter pw for vm
#Next type sudo docker pull mariadb/maxscale:latest
- grabs the latest mariadb update
#Run sudo docker run -d --name mxs mariadb/maxscale:latest
#Next run sudo docker run -d -p 8989:8989 --name mxs mariadb/maxscale:latest
#Run sudo apt install curl
- outputs in a tree formation for shards, commands, errors


