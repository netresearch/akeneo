# Akeneo

This is an image running [Akeneo PIM](https://www.akeneo.com/) on an [php-apache](https://hub.docker.com/_/php/) base image, ready to run with MongoDB.

## What is Akeneo?

> A Product Information Management system (also known as PIM, PCM or Products MDM) is a tool that helps companies to centralize and harmonize all the technical and marketing information of their catalogs and products.

*(Quoted from [Akeneo Website](https://www.akeneo.com/))*

## How to use this image

### Run

This image doesn't contain but requires a MySQL/MariaDB database in order to run - thus, it's best to run it using docker-compose. See [here](https://github.com/netresearch/docker-akeneo/blob/master/docker-compose.yml) for an example.

### Enironment variables

All of the following environment variables are optional and overwrite the according lowercase keys in [default configuration](https://github.com/akeneo/pim-community-dev/blob/master/app/config/parameters.yml.dist)

- DATABASE_DRIVER
- DATABASE_HOST
- DATABASE_PORT
- DATABASE_NAME
- DATABASE_USER
- DATABASE_PASSWORD
- LOCALE
- SECRET
- PIM_CATALOG_PRODUCT_STORAGE_DRIVER

  If you want to use MongoDB you need this variable with this value: doctrine/mongodb-odm

- MONGODB_SERVER
    
  If this variable is set, the DoctrineMongoDBBundle will automatically activated.
     
- MONGODB_DATABASE

  If you use MongoDb you must provide a database name, which will be used for the product collections



## GitHub

If you have any problems, questions, feature requests or simply stars to give please visit the [GitHub repository](https://github.com/netresearch/docker-akeneo).
