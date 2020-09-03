# README

## To run the kubernetes objects based

```
kubectl create -f db/permissions.yml
kubectl create -f db/statefulset.yml
kubectl create -f db/service.yml

kubectl create -f app/deployment.yml
kubectl create -f app/service.yml

minikube service service-application --url
```

Last command is going to tell the service IP address and port to be used

## Access the application

```
GET http://<SERVICE_IP_ADDRESS:PORT>/tasks
```

-> Refer to https://github.com/wkurosawa/tasker/blob/master/docs/endpoints.md for documentation on how to use the endpoints

## To remove kubernete objects

In case of an error, or to cleanup the environment

```
kubectl delete -f db/permissions.yml
kubectl delete -f db/statefulset.yml
kubectl delete -f db/service.yml

kubectl delete -f app/deployment.yml
kubectl delete -f app/service.yml
```
