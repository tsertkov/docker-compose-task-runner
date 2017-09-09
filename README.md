# Docker-compose task runner

> Approach for executing scripts in `docker-compose` managed environment.

## Overview

Regular services are defined in `docker-compose.yml` file and task runner services in `docker-compose.tasks.yml`.

Tasks

```
$ docker-compose up -d
$ ./run-task
$ ./run-task bash
$ ./run-task bash -c 'top'
$ ./run-task db-init
$ ./run-task db-restore
$ ./run-task db-migrate
$ ./run-task db-backup
$ docker-compose down --volumes
```

## Dot-env file configuration

Configuration variables are passed via environment variables to `docker-compose` and are defined in `.env` file.

## Included task scripts

- `db-init` create database
- `db-restore` restore database from backup
- `db-migrate` wordpress db example migration script
- `db-backup` backup database
