# Example flux repo

Start minikube

```shell
export KUBECONFIG=~/.kube/minikube.config
minikube start
minikube update-context
```

Bootstrap Flux

```shell
flux bootstrap git \
  --url=ssh://git@github.com/jvengustnchain/myapp-flux.git \
  --branch=master \
  --path=clusters/mycluster \
  --components-extra=image-reflector-controller,image-automation-controller \
  --private-key-file=$HOME/.ssh/github_nchain
```
