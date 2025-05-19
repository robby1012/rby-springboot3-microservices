# rby-springboot3-microservices

Multiple microservices communications implementation using spring boot 3.


## Requirement
- Java: https://adoptium.net/installation
- curl: https://curl.haxx.se/download.html
- jq: https://stedolan.github.io/jq/download/
- The Spring Boot CLI: https://docs.spring.io/spring-boot/docs/3.0.4/reference/html/
getting-started.html#getting-started.installing.cli
- Siege: https://github.com/JoeDog/siege#where-is-it
- Helm: https://helm.sh/docs/intro/install/
- kubectl: https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/
- Minikube: https://minikube.sigs.k8s.io/docs/start/
- Istioctl: https://istio.io/latest/docs/setup/getting-started/#download

## Tools instalation
` curl -LO "https://dl.k8s.io/release/v1.26.1/bin/darwin/amd64/kubectl"
sudo install kubectl /usr/local/bin/kubectl
rm kubectl `

` curl -LO https://storage.googleapis.com/minikube/releases/v1.29.0/minikubedarwin-amd64
sudo install minikube-darwin-amd64 /usr/local/bin/minikube
rm minikube-darwin-amd64
`

` curl -L https://istio.io/downloadIstio | ISTIO_VERSION=1.17.0 TARGET_
ARCH=x86_64 sh -
sudo install istio-1.17.0/bin/istioctl /usr/local/bin/istioctl
rm -r istio-1.17.0
`

## Verify Installation

git version && \

docker version -f json | jq -r .Client.Version && \

java -version 2>&1 | grep "openjdk version" && \

curl --version | grep "curl" | sed 's/(.*//' && \

jq --version && \

spring --version && \

siege --version 2>&1 | grep SIEGE && \

helm version --short && \

kubectl version --client -o json | jq -r .clientVersion.gitVersion && \

minikube version | grep "minikube" && \

istioctl version --remote=false


### RUN
- ` docker compose up `
- ` docker compose build `


## Tech Stack
- Spring Boot 3
- Apache Kafka
- RabbitMQ
- Spring Cloud
- OpenAPI
- MongoDB
- MySQL
- Docker
- Kubernetes
- Minikube
- Grafana


### Additional
- Comprehensive unit testing
- AOT (Ahead of Time Compilation)
