# Docker Lucee Command Box and Mysql

A simple project using Lucee Command Box and MySQL Docker

### MySQL

* Version 5.7 linux/x86_64
* Root password is `mysqlpass`. To change it, change the `MYSQL_ROOT_PASSWORD`
  in the `docker-compose.yml` file.
* Default database name is `mydb`. To change it, change the `MYSQL_DATABASE`
  in the `docker-compose.yml` file.
* Create a directory called `volume` inside `./mysql` to maintain database persistence

### Lucee

* Version 5.3.8.206 linux/arm64 (for MacOS)
* Change the `config.json` in the `lucee/boxconfig` folder with your settings
* The same is valid for the `server.json` file 

### APP sources

* Copy your sources to the `lucee/app` directory, or change in the `docker-compose` application path

### Run

You will need to have [Docker Compose][docker-compose] installed. Once it is installed, just run:

```
docker-compose up
```

Or macOS compatibility with arm64:

```
docker-compose --compatibility up --build
```

If this is your first time running this, docker will download the Lucee and MySQL images. 
Then both Lucee server and MySQL server will startup in separate containers.

### Test

http://127.0.0.1:8080/

### Lucee Web Admin

http://127.0.0.1:8080/lucee/admin/web.cfm

[docker-compose]: https://docs.docker.com/compose/