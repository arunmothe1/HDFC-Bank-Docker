sudo yum install docker -y

sudo systemctl start docker
sudo systemctl enable docker
sudo systemctl status docker

sudo mkdir -p /usr/local/lib/docker/cli-plugins

sudo curl -fSL \
https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.linux-amd64 \
-o /usr/local/lib/docker/cli-plugins/docker-buildx

sudo chmod +x /usr/local/lib/docker/cli-plugins

sudo curl -SL \
https://github.com/docker/compose/releases/latest/download/docker-compose-linux-x86_64 \
-o /usr/local/lib/docker/cli-plugins/docker-compose

sudo chmod +x /usr/local/lib/docker/cli-plugins/docker-compose

docker compose version

sudo yum install git -y

git clone https://github.com/Nitishkrsahu/HDFC-Bank-Docker

cd HDFC-Bank-Docker

docker compose up -d --build
