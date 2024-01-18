# Golang-and-Kubernetes-Based-web-app
A demo application based on 
Golang + 
Postgres + 
Kubernetes + 
gRPC



##
As for database migration
https://github.com/golang-migrate/migrate


## data migration

- Docker for createing database
create a new database
```
docker exec -it postgres12 /bin/bash createdb --username=root --owner=root simple_bank
```

- Use makefile to migrate database
```
make postgres
```

```
make createdb
```

```
migrate -path db/migration -database "postgresql://root:123456@localhost:5432/simple_bank?sslmode=disable" -verbose up
```



## Use SQLC for CRUD operations
