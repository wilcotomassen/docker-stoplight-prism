A minimal container for running Stoplight.io Prism, which can mock an API from a Swagger/OpenAPI Specification file

# Show version
```sh
docker run wilcotomassen/prism:v0.1 run version
```

# Create a mocking server from a Swagger/OpenAPI Specification file
```sh
docker run -d \
    --name=my-mock-server \
    -p 4010:4010 \
    -v $(pwd)/api-specification.yaml:/app/api-specification.yaml \
    wilcotomassen/prism:v0.1 run --mock --list --spec /app/api-specification.yaml
```

# Show all log lines
```sh
docker logs my-mock-server
```

# Show last 10 lines
```sh
docker logs --tail=10 my-mock-server
```
