# Docker Swarm ELK Stack
 Deploy ELK Stack in Docker Swarm

![logo](elk-stack.png)

By default, the stack exposes the following ports:
* **5000** : Logstash TCP input
* **9200** : Elasticsearch HTTP
* **9300** : Elasticsearch TCP transport
* **5601** : Kibana

### Bringing up the stack

```shell
docker stack deploy -c docker-stack.yml elk
```

If all components get deployed without any error, the following command will show 3 running services :

```shell
docker stack services elk
```

### Elastic License

You need license after terial time. You can use oss version of images for free version :

* Change images :

```yaml
docker.elastic.co/elasticsearch/elasticsearch-oss:7.6.1
docker.elastic.co/logstash/logstash-oss:7.6.1
docker.elastic.co/kibana/kibana-oss:7.6.1
```

* Remove XPack options from config files
