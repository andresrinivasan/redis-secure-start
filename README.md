# Start Redis with a Password

I want to start a Redis container using a password created by another container. Given that Redis 5 supports a single password for all authentication, wrapping the Redis image in another image seems like overkill just to obtain the password from somewhere. 

A shared volume seems like an easy mechanism for one container to create the password and then share it to the Redis container with a custom command. 