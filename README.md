```
docker run --rm -it --net=host  xwzhou/socat TCP-LISTEN:2376,reuseaddr,fork TCP:127.
0.0.1:2375
```


```
docker run --restart=always -v /var/run/docker.sock:/var/run/docker.sock -p 2376:2376 \
    xwzhou/socat TCP-LISTEN:2376,reuseaddr,fork UNIX-CONNECT:/var/run/docker.sock
```
