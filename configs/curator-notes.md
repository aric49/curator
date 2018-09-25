###Build Docker File:

```
docker build -t curator:1 .
```

###Run Curator Job to Delete Indices:

```
docker run -v $PWD/configs:/jobs -e ELASTIC_HOST=elasticsearch.kubernetes.internal.domain.com -e ELASTIC_PORT=80 --rm curator:1 /jobs/delete-indices.yml --config /jobs/curator.yml
```
