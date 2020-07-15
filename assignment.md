### Assignment1: 
Modify the following flask application to use mysql db instead of postgres data base
 
 [Hackfest App](https://github.com/rathneesh/hackfest)
 
### Assignment2:

Create a docker-compose yaml for the following Multi-contianer app(drupal postgres)

contianer1(front-end)


front-end image - drupal:8-apache

container port - 80

volumes - /var/www/html/modules

        - /var/www/html/profiles
        
        - /var/www/html/themes
        
        - /var/www/html/sites

contianer2(database)

back-end image - postgre:10

environment variable -  POSTGRES_PASSWORD: example


Note: Bring up both the containers on same user defined bridge network

### Assignment3:

wordpress - mysql app

contianer1(mysql)

   image: mysql:5.7
   
   volumes:/var/lib/mysql
   
   environment variables
   
       MYSQL_ROOT_PASSWORD: somewordpress
       
       MYSQL_DATABASE: wordpress
       
       MYSQL_USER: wordpress
       
       MYSQL_PASSWORD: wordpress


container2(wordpress)

     image: wordpress:latest
     
     port:80
     
     environment variables
     
       WORDPRESS_DB_HOST: db:3306
       
       WORDPRESS_DB_USER: wordpress
       
       WORDPRESS_DB_PASSWORD: wordpress
       WORDPRESS_DB_NAME: wordpress

Note: Bring up the application on an user defined bridge network

Create a docker-compose file to bring up the application

### Assignment4:
text here

