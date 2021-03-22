# gitea-docker-compose
The docker-compose file for deploying gitea

### Start
`bash start.sh`

### Stop
`bash stop.sh`

### Check
```
docker-compose ps
```

# Add system service
1. Open `docker-gitea.service file` and Adjust WorkingDirectory in service file if needed
2. Create symbolic link: `ln -s docker-gitea.service /etc/systemd/system/docker-gitea.service`
3. Start service: `systemctl start docker-gitea`
4. (optional) Enable autostart at boot: `systemctl enable docker-gitea`

## Reference
1. https://docs.gitea.io/en-us/install-with-docker/