# learningDockerCompose

## MONGO
```bash
    docker run -d \
    -p 27017:27017 \
    -e MONGO_INITDB_ROOT_USERNAME=admin \
    -e MONGO_INITDB_ROOT_PASSWORD=supersecret \
    --network mongo-network \
    --name mongodb \
    mongo
```
## MONGO EXPRESS
```bash
    docker run -d \
    -p 8081:8081 \
    -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin \
    -e ME_CONFIG_MONGODB_ADMINPASSWORD=supersecret \
    -e ME_CONFIG_MONGODB_SERVER=mongodb \
    --network mongo-network \
    --name mongo-express \
    mongo-express
```


### credenciales Mongo Express

```bash

docker logs <id contenedor mongo-express>
```