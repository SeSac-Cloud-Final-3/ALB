# ALB
ALB 전용 세팅 yaml 파일   

mkdir settings   
cd settings   

curl -L -O https://github.com/SeSac-Cloud-Final-3/ALB/raw/main/alb-controller.yaml   
curl -L -O https://github.com/SeSac-Cloud-Final-3/ALB/raw/main/cert-manager.yaml   

kubectl create -f cert-manager.yaml   
kubectl get pods -n cert-manager   

kubectl create -f alb-controller.yaml   
kubectl get pods -n kube-system   

kubectl get deploy -n kube-system aws-load-balancer-controller   
