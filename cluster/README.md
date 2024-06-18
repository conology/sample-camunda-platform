## Getting started
### Prerequisites
The following cli tools are required
- docker
- kubectl
- k3d
- helm

Also, you want a dns proxy configuration to point *.test to local host

### Setup
If not already available, create k3d default registry on port 5000
```shell
k3d registry create --port 5000
```

Create the cluster
```shell
k3d cluster create --config ./k3d.yaml
```

Declare namespaces
```shell
kubectl apply -f namespaces.yaml
```

#### setup camunda self managed
See [camunda setup](./camunda-platform/setup.md)