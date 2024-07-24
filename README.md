# url-shorter-challenge

docker build -t url-shorter:latest ./url-shorter
docker build -t process-queue:latest ./process-queue

docker swarm init

docker network create --driver overlay my-network-overlay

docker stack deploy -c docker-compose.yml my_stack
