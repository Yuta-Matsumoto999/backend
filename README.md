# Backend
## Introduction

Build a laravel environment with docker-compose. You can run unit tests using the github actions workflow.
Also, you can automatically deploy to the ECS on Fargate environment prepared on AWS.
See the wiki for a detailed explanation of Workflows. 

## Usage

### Laravel setup

1. Git clone & change directory
2. Execute the following command

```bash
$ make setup
```

http://localhost

## Tips

- Read this [Makefile](https://github.com/Yuta-Matsumoto999/backend/blob/main/Makefile).

## Container structures

```bash
├── app
├── web
└── db
```

### app container

- Base image
  - [php](https://hub.docker.com/_/php):8.1-fpm-bullseye
  - [composer](https://hub.docker.com/_/composer):2.2

### web container

- Base image
  - [nginx](https://hub.docker.com/_/nginx):1.22

### db container

- Base image
  - [mysql/mysql-server](https://hub.docker.com/r/mysql/mysql-server):8.0

### mailhog container

- Base image
  - [mailhog/mailhog](https://hub.docker.com/r/mailhog/mailhog)
