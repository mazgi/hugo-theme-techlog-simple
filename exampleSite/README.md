# hugo-theme-techlog-simple/exampleSite

You should create a ".env" file as follows.

```shellsession
rm -f .env
test $(uname -s) = 'Linux' && echo "UID=$(id -u)\nGID=$(id -g)" >> .env
cat<<EOE >> .env
BIND_IP_ADDR=192.168.0.1
EOE
```

And start the container.

```shellsession
docker-compose up
```

Now you can access to the example site via follows URL.  
`http:${BIND_IP_ADDR}:1313`
