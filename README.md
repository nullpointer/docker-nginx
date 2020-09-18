# docker-nginx

```
docker-nginx
├── docker-compose.yml
├── etc
│   ├── nginx
│   │   ├── default.conf
│   │   └── default.template.conf
│   └── ssl
│       ├── cacert.pem
│       ├── server.crt
│       └── server.key
└── web
    └── public  
        ├── css
        ├── img
        ├── js
        └── index.html
```

## Install docker compose

```bash
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.27.3/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
```

> Just use [docker-compose-Linux-x86_64](docker-compose-Linux-x86_64) if you are on Linux-x86_64.

## Set web root

Put static web content to the directory `docker-niginx/web/public`

## Set SSL for HTTPS

Replace server.crt, server.key and cacert.pem in directory `docker-nginx/etc/ssl`

## Start

```bash
$ docker-compose up
```

## Stop

```bash
$ docker-compose down
```
