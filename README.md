# Logging Docker Container with Elasticsearch

## Required Files
1. Docker compose file
2. fluent bit configuration

## Logging Services
1. Fluent Bit: Lightweight log collector and forwarder 
2. Elasticsearch: Search engine based on the Lucene library to store, search, and analyze large amounts of structured and unstructured data

## Configuring Elasticsearch
Add the elasticsearch hostname to `fluent-bit.conf` file. Add hostname, port, user, password accordingly to same file.

## Running App and Start Logging
```bash
$ docker-compose up -d
```

## Elasticsearch Index Naming
The index to which logs are sent can be changed by altering the variable `Index ${HOSTNAME}` on `fluent-bit.conf` file. Currently, the variable is set from Docker by making static hostname of the fluent bit container
