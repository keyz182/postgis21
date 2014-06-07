postgis21
=========

Postgres 9.3 + Postgis 2.1 Dockerfile

Based on the example at http://docs.docker.io/examples/postgresql_service/.

Tweaked to work with Ubuntu Trusty

Database name: docker
Username     : docker
Password     : docker

Example Usage:

```bash

$ sudo docker build -t postgis21 .

$ sudo docker run --rm -P --name pg_test postgis21

$ sudo docker run --rm -t -i --link pg_test:pg postgis21 bash

postgres@7ef98b1b7243:/$ psql -h $PG_PORT_5432_TCP_ADDR -p $PG_PORT_5432_TCP_PORT -d docker -U docker --password

```
