# kubewatch.io pod deployment with k8s

## setup

You can use stacksensor-setup-exec.yaml to setup your RBAC and service account for stacksensor pod.
This template will enable exec for the stacksensor pod. If you don't want to allow exec (testing for shell and user rights inside containers), you can use the stacksensor-setup.yaml file.

```
kubectl apply -f stacksensor-setup-exec.yaml
```

## Deploy pod

You have to fill the token field with the token value you've created on the platform for this specific cluster.
As soon as the pod start, it will contact the platform with this token and register.
You will see the connected pod in the cluster list.

```
kubectl apply -f stacksensor.yaml
```

