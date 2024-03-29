# Status Checker

1 Create Docker machine

```
$ docker-machine create status-checker
$ docker-machine env status-checker
$ eval $(docker-machine env status-checker)
```

2 Adjust the .env file
```
$ cp .env.dist .env
$ vi .env
```

3 Run the install script
```
$ chmod +ux bin/* && ./bin/install
```
4 Run the database migrations and seeders
```
$ docker-compose exec site bash
$ ./artisan migrate
$ ./artisan db:seed  --class=SiteTableSeeder
```

5 Open browser
```
$ docker-machine ip status-checker
$ open <DOCKER_MACHINE_IP>
``` 

# Uninstall
```
$ docker-machine rm status-checker
``` 
