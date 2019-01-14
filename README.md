
Init Swarm :

I3 Wifi LocalManap :
docker swarm init \
    --listen-addr 192.168.1.5 \
    --advertise-addr 192.168.1.5


i7 Latitude :
docker swarm join \
    --token=SWMTKN-1-0as2atbl3c3usu7dbh50d6i4ra683561w9orvufuyv8ok9q6z6-0bzwgcoq8xo9hej593n2381b1 \
    --listen-addr 192.168.1.18 \
    --advertise-addr 192.168.1.18 \
    192.168.1.5


Sur le manager :
git pull https://github.com/Nasjoe/DockerSwarmGeoClusterSql.git
docker network create --driver=overlay traefik-net

docker stack deploy -c composes/https-traefik-docker-compose.yml mystack