# redis-commander-docker
Redis Commander in a tiny Docker image powered by Alpine Linux

# How to use this image

Run Redis server if you don't have it:

```bash
docker run -d --name=redis -p 6379:6379 redis:3.0
```
Run Redis Commander:

```bash
docker run -d --name=redis_commander \
  -p 8081:8081 \
  --link=redis:redis \
  diyan/redis-commander \
  --redis-host redis
```
Access to Web UI using your browser:

```bash
firefox http://localhost:8081
```
