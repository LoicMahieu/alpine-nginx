# Alpine Nginx

Tiny web server using [`nginx`](http://nginx.org/) built from source on Alpine Linux.

Currently only available on Quay.io:
```sh
$ docker pull quay.io/loicmahieu/alpine-nginx
```

# Tags
Currently `loicmahieu/alpine-nginx` is only published on Quay.io as automated build. Docker tags are reflect of git tag.
- https://quay.io/repository/loicmahieu/alpine-nginx?tab=tags
- https://github.com/LoicMahieu/alpine-nginx/releases

### Available tags:
- [v1.9.4](https://github.com/LoicMahieu/alpine-nginx/releases/tag/v1.9.4)
- [v1.8.0](https://github.com/LoicMahieu/alpine-nginx/releases/tag/v1.8.0)
- [v1.7.12](https://github.com/LoicMahieu/alpine-nginx/releases/tag/v1.7.12)

# Examples
```
$ docker run quay.io/loicmahieu/alpine-nginx nginx -v
nginx version: nginx/1.9.4
```

- [Simple](./examples/simple/Dockerfile)
```Dockerfile
FROM quay.io/loicmahieu/alpine-nginx
COPY www /etc/nginx/html
```
Overwrite default HTML pages of nginx.

- [Configurable](./examples/full/Dockerfile)
```Dockerfile
FROM quay.io/loicmahieu/alpine-nginx
COPY conf/nginx.conf /etc/nginx/conf/nginx.conf
COPY www /www
```
Overwrite whole nginx configuration.
