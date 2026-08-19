# Deploy
    kubectl apply -f https://raw.githubusercontent.com/ashish404403/argocd-app-config/refs/heads/main/application.yaml
    
# Delete
    kubectl delete -f https://raw.githubusercontent.com/ashish404403/argocd-app-config/refs/heads/main/application.yaml

#
    kubectl get pods -A
#
    kubectl get application -A
#
    kubectl get svc -n myapp

# Argo CD web ui

    kubectl port-forward --address 0.0.0.0 svc/argocd-server -n argocd 8080:443

# Access myapp-service

    kubectl port-forward --address 0.0.0.0 -n myapp svc/myapp-service 8088:80


# test auto sync by deleting namespace myapp

    kubectl delete namespace myapp

