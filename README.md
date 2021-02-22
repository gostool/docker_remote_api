# docker_remote_api


## run
* network

```
docker network create my_network
docker-compose up -d
```


## test

```
curl -v http://localhost:2375/version
```


```
(venv) ➜  docker_remote_api git:(main) ✗ curl -v http://localhost:2375/version
*   Trying ::1...
* TCP_NODELAY set
* Connected to localhost (::1) port 2375 (#0)
> GET /version HTTP/1.1
> Host: localhost:2375
> User-Agent: curl/7.54.0
> Accept: */*
>
< HTTP/1.1 200 OK
< Api-Version: 1.40
< Content-Type: application/json
< Date: Mon, 22 Feb 2021 08:10:42 GMT
< Docker-Experimental: false
< Ostype: linux
< Server: Docker/19.03.13 (linux)
< Transfer-Encoding: chunked
<
{"Platform":{"Name":"Docker Engine - Community"},"Components":[{"Name":"Engine","Version":"19.03.13","Details":{"ApiVersion":"1.40","Arch":"amd64","BuildTime":"2020-09-16T17:07:04.000000000+00:00","Experimental":"false","GitCommit":"4484c46d9d","GoVersion":"go1.13.15","KernelVersion":"4.19.76-linuxkit","MinAPIVersion":"1.12","Os":"linux"}},{"Name":"containerd","Version":"v1.3.7","Details":{"GitCommit":"8fba4e9a7d01810a393d5d25a3621dc101981175"}},{"Name":"runc","Version":"1.0.0-rc10","Details":{"GitCommit":"dc9208a3303feef5b3839f4323d9beb36df0a9dd"}},{"Name":"docker-init","Version":"0.18.0","Details":{"GitCommit":"fec3683"}}],"Version":"19.03.13","ApiVersion":"1.40","MinAPIVersion":"1.12","GitCommit":"4484c46d9d","GoVersion":"go1.13.15","Os":"linux","Arch":"amd64","KernelVersion":"4.19.76-linuxkit","BuildTime":"2020-09-16T17:07:04.000000000+00:00"}
* Connection #0 to host localhost left intact
```
