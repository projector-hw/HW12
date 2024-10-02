# HW12

docker run -d --name redis-stack -v `pwd`/redis_7.4/local-redis-stack.conf:/redis-stack.conf -v `pwd`/redis_7.4/data:/data -v `pwd`/redis_7.4/log:/var/log/redis -p 6379:6379 -p 8001:8001 redis/redis-stack:latest

redis-benchmark -q -n 100000 -c 50 -P 10
redis-benchmark -q -n 100000 -c 50 -P 1
