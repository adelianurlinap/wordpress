# wordpress

## Create namespace

### From Rancher
```
From Rancher UI -> Go to Cluster -> Cluster -> Project/Namespace -> Not In Project “Create Namespace” 

Name : wordpress
```

### From kubectl
```
kubectl create ns wordpress
```

## Create Secret

### From Rancher
```
From Rancher UI -> Go to Cluster -> Storage -> Secrets -> Create -> Opaque

Namespace : wordpress
Name : mysql-pass
Key : password
Value : Gladiators88@
```

### From kubectl
```
kubectl create -n wordpress secret generic mysql-pass --from-literal=password=Gladiators88@
```
