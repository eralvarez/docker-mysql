# docker-mysql

Table of contents
- [Introduction](#introduction)
- [Version](#version)
- [Commands](#commands)

## Introduction

Example of how to run mysql in docker.

_Note: This is just for development purposes._

## Version

`MySQL v5.6`

## Commands

Create volume to persist data

```bash
docker volume create mysql_vol
```

Pull and create mysql container, map it to `3306` port.

```bash
docker run --name mysql_container --env-file .env --mount type=volume,src=mysql_vol,dst=/var/lib/mysql -p 3306:3306 -d mysql:5.6
```