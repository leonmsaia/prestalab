# prestalab
PrestaShop Docker Implementation for Learning Purposes

Step 1: Clone the Repository
Clone the repository from GitHub:
git clone https://github.com/leonmsaia/prestalab.git

Step 2: Configure the .env File
Complete the .env file with the desired data as needed.
(It can be left as default)

Step 3: Build and Run Docker Containers
docker-compose up --build
This will build the necessary Docker containers, namely:
PrestaShop (8.1.0)
MySQL
phpMyAdmin

Step 4: Import the Database Dump
After the containers are up and running, import the database dump by executing the following command in another terminal:
docker-compose exec mysql sh -c 'exec mysql -uroot -p"$MYSQL_ROOT_PASSWORD" $MYSQL_DATABASE' < sql/prestashop.sql

Step 5: Access PrestaShop and phpMyAdmin
Once the previous steps are completed, PrestaShop should be available at http://localhost:8080 and phpMyAdmin at http://localhost:8081.
You can access phpMyAdmin using the credentials defined in the .env file.

That's it! Now you have a lab environment to study, modify, create, break, and recreate a complete PrestaShop store.

PrestaShop Documentation: https://devdocs.prestashop-project.org/8/

Author
Leon. M. Saia
leonmsaia@gmail.com
+54 9 11 2374 7372
https://www.linkedin.com/in/leonmsaia/
https://github.com/leonmsaia/prestalab