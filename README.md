## Popcorn

### About the project

This project contains the dafault project of Laravel framework and the docker files to run the Laravel project immediately,
without installing anything except docker in the operating system.

The docker configuration contains the nginx and the mysql database that communicate with each other inside the containers.

### Configure database in .env file

```
DB_CONNECTION=mysql
DB_HOST=database
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=elison
DB_PASSWORD=password

``` 

The host is the same with the service name in the docker-compose.yml configuration file.

### Commands

docker-compose build laravel-app -> build the containers

docker-compose up -d -> run the containers in background

#### Run commands inside container

sudo docker-compose exec laravel-app sh -> enter with shell inside container and run necessary commands for laravel project

#### Run commands without shell

sudo docker-compose exec laravel-app composer i -> run command to install composer packages  

sudo docker-compose exec laravel-app php artisan migrate


### Access the project

Visit http://localhost:8000 in your browser


#### References

`1. https://docs.docker.com/compose/`

`2. https://www.digitalocean.com/community/tutorials/how-to-install-and-set-up-laravel-with-docker-compose-on-ubuntu-22-04`