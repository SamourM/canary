# canary

Links:

start here: https://github.com/ContainerSolutions/k8s-deployment-strategies


https://github.com/ContainerSolutions/k8s-deployment-strategies/tree/master/canary/native
https://github.com/ContainerSolutions/k8s-deployment-strategies/tree/master/ab-testing
https://github.com/runyontr/k8s-canary
https://github.com/GoogleCloudPlatform/istio-samples/tree/master/istio-canary-gke#setup     istio 


Installation Notes:

sudo helm init --upgrade 

 helm install     --namespace=monitoring     --name=prometheus     --version=7.0.0     stable/prometheus
 
sudo helm install    --namespace=monitoring   --name=grafana    --version=1.12.0   --set=adminUser=admin   --set=adminPassword=admin    --set=service.type=NodePort 	    stable/grafana

kubectl get secret --namespace monitoring grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo
