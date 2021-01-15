**Summary**
A docker-compose set that support:
- Redis cluster
- RabbitMQ
- MongoDB (Replica set - 3 nodes)
- Kafka


**Building step**

```
cd docker
docker-compose up -d
```

**Init replica set**
```
cd docker
docker-compose exec mongo1 bash
mongo
rs.initiate()
rs.add("mongo2")
rs.add("mongo3")
rs.conf()
rs.status()
```
