# docker-mongo-replica
docker mongo replica


## clone 

````
git clone https://github.com/wachira90/docker-mongo-replica.git
````

## create data folder

````
cd docker-mongo-replica
mkdir data
sudo chmod -R 0777 data/
````

## start 
````
docker-compose up -d && docker-compose logs -f
````

## command create user 
````
use admin

db.createUser({
    user: "root",
    pwd: "example",
    roles: [{
        role: "userAdminAnyDatabase",
        db: "admin"
    }, "readWriteAnyDatabase"]
})

````
