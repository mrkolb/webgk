# python-flask-docker
Basic Python Flask app in Docker which prints the hostname and IP of the container used for JenkinsX CI/CD integration tests. App prints hostname and IP.

# Test

Now visit http://awsdomain:8080
```
 Ex.
 The hostname of the container is 6095273a4e9b and its IP is 172.17.0.2.
```

### Verify the running container
Verify by checking the container ip and hostname (ID):
```
$ docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' my-container
172.17.0.2
$ docker inspect -f '{{ .Config.Hostname }}' my-container
6095273a4e9b
```

### Cudos and thanks to Lorenz Vanthill for the build
