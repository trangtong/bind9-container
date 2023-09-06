# bind9-container

sudo docker network create --subnet=172.20.0.0/16 bind9-net

sudo docker build -t bind9 .

sudo docker run -d --rm --name=dns-server --net=bind9-net --ip=172.20.0.2 bind9

sudo docker exec -d dns-server /etc/init.d/bind9 start
