# kubernetes-spring-cloud-order-service

### Run
```bash
./gradlew bootRun
```

### build, tag and push
```bash
./gradlew clean build
```

```bash
docker build . -t kubernetes-spring-cloud-order-service
```

```bash
docker run -p 8080:8080 kubernetes-spring-cloud-order-service
```

```bash
export DOCKER_ID_USER="benweizhu" ## put your docker-hub username
```


```bash
docker tag kubernetes-spring-cloud-order-service $DOCKER_ID_USER/kubernetes-spring-cloud-order-service
```

```bash
docker push $DOCKER_ID_USER/kubernetes-spring-cloud-order-service
```

```bash
docker pull $DOCKER_ID_USER/kubernetes-spring-cloud-order-service
```

### kubernetes

```bash
kubectl apply -f ./kubenetes/deployment.yml
```

```bash
kubectl apply -f ./kubenetes/service.yml
```

### reference
https://github.com/benweizhu/kubernetes-spring-cloud-example