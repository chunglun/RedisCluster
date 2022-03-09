# RedisCluster


# Steps
1. Use 127.0.0.1 to replace $(ipconfig getifaddr en0)
> ip=$(ipconfig getifaddr en0) docker-compose up -d

> ip=127.0.0.1 docker-compose up -d

2. Check
> redis-cli -p 7000 cluster info #確認 cluster_state:ok

> docker exec -it rediscluster_redis-node1_1 redis-cli -p 7000 cluster info

> docker exec -it rediscluster_redis-node1_1 redis-cli -p 7000 cluster nodes

> docker exec -it rediscluster_redis-node1_1 redis-cli -p 7000 -c

[reference](https://blog.bimap.com.tw/2021/06/10/dockerize-redis-cluster-tutorial)