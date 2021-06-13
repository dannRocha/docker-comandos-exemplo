# DOCKER comandos de execução


## Postgres

* OBTER: 
```
docker pull postgres:alpine
```

* RODAR: 
```sh
docker run --name postgres-0 -e POSTGRES_PASSWORD=password -d -p 5432:5432 postgres:alpine

# ou
docker run -d \
           --name postgres-container \
           -e POSTGRES_PASSWORD=password \
           -e PGDATA=/var/lib/postgresql/data/ \
           -v /home/daniel/Workspace/docker/data:/var/lib/postgresql/data \
           -p 5432:5432 \
            postgres:alpine

```
OBS: ***password*** vai ser a senha para acessar o banco de dados


## MariaDB
* OBTER: 
```
docker pull mariadb:latest
```

* RODAR: 
```sh
docker run -d \
			--name mariadb-container \
			-e MARIADB_ALLOW_EMPTY_ROOT_PASSWORD=yes \
			-v /home/daniel/Workspace/docker/data-mariadb:/var/lib/mysql \
			-p 3306:3306 \
			mariadb:latest

```
