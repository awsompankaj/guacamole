# Guacamole with mysql authentication
Apache Guacamole is an HTML5 application useful for accessing a remote desktop through RDP, VNC, and other protocols. You can create a virtual cloud desktop where applications can be accessed through a web browser. This guide will cover the installation of Apache Guacamole through Docker,

## Installation

Make sure you have docker installed on your system.

clone git repo

```bash
git clone https://github.com/awsompankaj/guacamole.git
```

## Usage

```bash
docker-compose up
```

## This Docker-compose file consist of 4 images

guacamole/guacamole

guacamole/guacd

mysql/mysql-server

nginx/nginx



## Access

[https://localhost](https://localhost)

Username: guacadmin

Password: guacadmin

## To use your own mysql password

  remove files from data directory before running docker compose
  
  ```sh
  #rm -rf ./data/*
  ```
  ```sh
  #docker-compose up -d
  #docker cp initdb.sql mysql:/
  #docker exec -it mysql bash
  bash$ mysql -u root -p
  password:
  mysql> use guacamole_db;
  mysql>source /initdb.sql
  ```
  
  Now mysql container will run with updated mysql password:
