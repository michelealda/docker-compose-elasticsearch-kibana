# docker-compose-elasticsearch-kibana-apm

## In a nutshell
Setup your development environment with

- [x] Elasticsearch version 7.2.0
- [x] Kibana version 7.2.0
- [x] APM Server version 7.2.0

Please [check the full original repo](https://github.com/maxyermayank/docker-compose-elasticsearch-kibana) if you want a full ELK stack.

I have the need to simply run a local APM server for development purpose, so I simplified the repo.

## Important note
Based on your local docker setup, you might need to increase the [vm.max_map_count](https://www.elastic.co/guide/en/elasticsearch/reference/7.2/docker.html#docker-cli-run-prod-mode)

Working on Windows I set the docker engine available memory to 4Gb and didn't have any issue running this stack consistently.

## Requirements
- [x] Docker 18.05
- [x] Docker-compose 1.21

### Start Stack in Daemon Mode
```
docker-compose up -d
```

### Check status of docker-compose cluster
```
docker-compose ps -a
```

### Stop Compose Stack
```
docker-compose down
```

### Access Kibana
```
http://localhost:5601
```

### Access Elasticsearch
```
http://localhost:9200
```

# Resources
* [Hands on Elasticsearch](https://medium.com/@maxy_ermayank/hands-on-elasticsearch-8fa59d8aebfc)
* [Elasticsearch Resources](https://medium.com/@maxy_ermayank/elasticsearch-resources-27d24f01c1dc)
* [Open Distro Elasticsearch](https://medium.com/@maxy_ermayank/tl-dr-aws-open-distro-elasticsearch-fc642f0e592a)
