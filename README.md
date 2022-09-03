![](redis-logo.svg)
# Redis

## Remote Dictionary Server

![](redis.png)

## Open Source In Memory Data Store

https://redis.io/

![](web.png)

# Developer: Salvatore Sanfilippo

https://github.com/antirez

![](developer.png)

## Redis CLI

![](INCR.png)

All commands: https://redis.io/docs/manual/cli/

```
sudo apt-get install redis
sudo apt-get install php-redis
```

# PHP Redis

```
$redis = new Redis(); 
$redis->connect('127.0.0.1', 6379); 
echo "Connected to the Redis server<br>"; 

$redis->lpush("dbs", "Redis"); 
$redis->lpush("dbs", "Mongodb"); 
$redis->lpush("dbs", "Mysql");  

$arList = $redis->lrange("dbs", 0 ,3); 

echo "Stored in Redis <br>"; 
print_r($arList); 
```
![](php-redis.png)


# Redis Persistance

https://redis.io/docs/manual/persistence/

## Snapshotting

By default Redis saves snapshots of the dataset on disk, in a binary file called dump.rdb. You can configure Redis to have it save the dataset every N seconds if there are at least M changes in the dataset, or you can manually call the SAVE or BGSAVE commands.
