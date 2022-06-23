# docker

### Installing Docker
```bash
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
apt-cache policy docker-ce
sudo apt install docker-ce
sudo systemctl status docker
```

### Executing the Docker Command Without Sudo
```bash
sudo usermod -aG docker ${USER}
su - ${USER}
groups
sudo usermod -aG docker username
```

### Docker Command
```bash
docker [option] [command] [arguments]
docker info
```

### Working with Docker Images
```bash
docker run hello-world
docker search ubuntu
docker pull ubuntu
docker images
```

### Running a Docker Container
```bash
docker run -it ubuntu
```

### Uninstall Docker
```bash
dpkg -l | grep -i docker
sudo apt-get purge -y docker-engine docker docker.io docker-ce docker-ce-cli
sudo apt-get autoremove -y --purge docker-engine docker docker.io docker-ce  
sudo rm -rf /var/lib/docker /etc/docker
sudo rm /etc/apparmor.d/docker
sudo groupdel docker
sudo rm -rf /var/run/docker.sock
```
