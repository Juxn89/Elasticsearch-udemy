# Elasticsearch-udemy
Complete guide to Elasticsearch

## Run Elasticsearch - Docker
Before start make sure you have [Docker Desktop](https://www.docker.com/products/docker-desktop/)
1. Run ```docker-compose up```.
2. Open new terminal.
3. Run ```docker exec -it elasticsearch /bin/bash```
4. Add new user for Kibana, run next command: ```elasticsearch-users useradd kibana_system -p mykibanapass -r kibana_system```
5. Re-start services: ```docker-compose down && docker-compose up -d```
6. Open Elasticsearch with ```http://localhost:9200/``` and Kibana with ```http://localhost:5601/```

## Hosting options
- [Bonsai free plan - OpenSearch](https://bonsai.io/partner/bo-andersen-udemy)
- [Elastic Cloud trial - Elasticsearch](https://www.elastic.co/cloud/cloud-trial-overview?utm_source=udemy&utm_medium=referral&utm_campaign=udemy-guide-to-es-gc)
- [Aiven trial - OpenSearch](https://aiven.io/opensearch)
- [Digital Ocean - OpenSearch](https://www.digitalocean.com/products/managed-databases-opensearch)
- [Amazon OpenSearch Service - OpenSearch](https://aws.amazon.com/opensearch-service/)
- [Elasticsearch download](https://www.elastic.co/downloads/elasticsearch)
- [Kibana download](https://www.elastic.co/downloads/kibana)
- [OpenSearch download](https://opensearch.org/downloads.html)

## Kibana
### Commands
#### Nodes and Cat API
|HTTP Verb|URL|Summary|
|---------|---|-------|
|**GET**|```/_cluster/health```|Retrive clusters state|
|**GET**|```/_cat/nodes?v```|Show information readable|
|**GET**|```/_cat/indexes?v&expand_wildcards=all```|Check indexes in our cluster|

- [Nodes info API](https://www.elastic.co/guide/en/elasticsearch/reference/current/cluster-nodes-info.html)
- [cat nodes API](https://www.elastic.co/guide/en/elasticsearch/reference/current/cat-nodes.html)

#### Indexes
|HTTP Verb|URL|Summary|
|---------|---|-------|
|**GET**|```/cat/indices?v```|Get list of indexes|
|**PUT**|```/cat/INDEX_NAME```|Create a index. ex: ```/cat/pages```|
|**GET**|```/_cat/shards?v```|Get list of sharps|
