# docker-webdav
A webdav docker deployment

The image is based on https://github.com/BytemarkHosting/docker-webdav with Elbosso's patch https://github.com/BytemarkHosting/docker-webdav/pull/15 .

This docker-compose file will start the service for you, with self-signed SSL certificate and digest settings.

Create mulitple logins with
```
touch user.passwd
htdigest user.passwd WebDAV alice
htdigest user.passwd WebDAV bob
```
and then run the docker service
```
docker-compose -d up
```

