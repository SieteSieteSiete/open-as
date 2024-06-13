# Database

I'd like to use Redis as my database system for catagorizing the media library

### Commands

To run redis stack, use command:

`docker run -d --name redis-stack -p 6379:6379 -p 8001:8001 redis/redis-stack:latest`

To run redis stack with persistence, use:

`docker run -v /local-data/:/data redis/redis-stack:latest`

Combining these commands yields:

`docker run -d --name TVDatabase -p 6379:6379 -p 8001:8001 -v TVEmulatorRedisData:/data redis/redis-stack:latest`

To access cli from docker container, use:

`docker exec -it TVDatabase redis-cli`

# Weird Stuff

On Mac, activating a venv needs . (same as `source`), as in:

`. TVEmulatorPython/bin/activate`