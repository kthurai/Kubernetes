
<h3><a href="https://kubernetes.io/docs/home/">Kubernetes Documentation</h3>

<pre>
k config view --raw

$ kubectl get pods -o wide
NAME            READY   STATUS    RESTARTS   AGE   IP           NODE                   NOMINATED NODE   READINESS GATES
httpd-ethukok   1/1     Running   0          22h   10.42.0.10   lima-rancher-desktop   <none>           <none>
nginx-ethukok   1/1     Running   0          22h   10.42.0.9    lima-rancher-desktop   <none>           <none>
nginx-yaml      1/1     Running   0          17h   10.42.0.13   lima-rancher-desktop   <none>           <none>

$ kubectl get namespaces
NAME              STATUS   AGE
default           Active   24h
kube-node-lease   Active   24h
kube-public       Active   24h
kube-system       Active   24h

$ kubectl rollout history deployment ngnix-deploy 
deployment.apps/ngnix-deploy 
REVISION  CHANGE-CAUSE
1         <none>
2         <none>

ethukok@ethukok-Rampage-Extreme:~/GitHub/Kubernetes/YAML/Deployments$ k config get-clusters 
NAME
rancher-desktop

ethukok@ethukok-Rampage-Extreme:~/GitHub/Kubernetes/YAML/Deployments$ k config get-contexts 
CURRENT   NAME              CLUSTER           AUTHINFO          NAMESPACE
*         rancher-desktop   rancher-desktop   rancher-desktop   


ethukok@ethukok-Rampage-Extreme:~/GitHub/Kubernetes/YAML/Deployments$ k config set-context rancher-desktop 
Context "rancher-desktop" modified.

ethukok@ethukok-Rampage-Extreme:~/GitHub/Kubernetes/YAML/Deployments$ kubectl config view --minify | grep namespace:
    namespace: mealie

ethukok@ethukok-Rampage-Extreme:~/GitHub/Kubernetes/YAML/Deployments$ kubectl config set-context --current --namespace=mealie
Context "rancher-desktop" modified.

ethukok@ethukok-Rampage-Extreme:~/GitHub/Kubernetes/YAML/Deployments$ k expose deployment frontend --port 8080
Error from server (AlreadyExists): services "frontend" already exists



</pre>

