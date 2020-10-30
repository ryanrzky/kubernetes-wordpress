### Create PV and PVC

### Create Secret
```
cat <<EOF >./kustomization.yaml
secretGenerator:
- name: mysql-pass
  literals:
  - password=qwe123       
EOF

```

`kubectl apply -k .`

`minikube service wordpress --url`