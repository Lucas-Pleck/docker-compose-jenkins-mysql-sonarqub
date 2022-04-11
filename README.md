Docker-compose: GitLab, Jenkins, and SonarQube.

# Start the instance

```bash
docker-compose up -d
```
URLs for various services:
* GitLab - http://localhost:8000
* Jenkins - http://localhost:8080
* SonarQube - http://localhost:9000

Jenkins installation requires a secret key which sent to the logs => use `docker logs` to get the key:
```bash
docker logs gitlab_jenkins_1 | less
```

# Stop instance
```bash
docker-compose down
```

Data is persisted through various volumes. 
Remove all the volumes:
```bash
docker-compose down -v
```
