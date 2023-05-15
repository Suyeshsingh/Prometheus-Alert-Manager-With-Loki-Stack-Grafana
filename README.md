# Prometheus-Alert-Manager-With-Loki-Stack-Grafana


kubectl create ns monitoring

git clone https://github.com/Suyeshsingh/Prometheus-Alert-Manager-With-Loki-Stack-Grafana.git

cd Prometheus-Alert-Manager-With-Loki-Stack-Grafana/

kubectl apply -f Prometheus-Alert-Manager\ /

helm repo add grafana https://grafana.github.io/helm-charts

helm repo update

helm install loki-stack grafana/loki-stack --set grafana.rbac.pspEnabled=false --values values.yaml -n monitoring

Note: Please edit values.yaml file for loki stack accordingly.
