# loki-project
Setup of loki, prometheous and grafana on minikube

loki - statefulset
prometheous - Daemonset
grafana - deployment


+----------------+       +-------------------------+       +-----------------------+
|                |       |                         |       |                       |
|  Application   +------>+      Prometheus         +------>+      Grafana          |
|    Logging     |       |   (Metrics Collector)   |       |    (Visualization)    |
|                |       |                         |       |                       |
+----------------+       +-------------------------+       +-----------------------+
        ^                           |                            |
        |                           |                            |
        |                           |                            |
        |                           |                            |
        |                           v                            |
        |                  +-------------------------------+     |
        |                  |                               |     |
        +----------------->+         Loki                  +<----+
                           |   (Log Aggregation System)   |
                           |                               |
                           +-------------------------------+

**1. installation of docker**
https://docs.docker.com/engine/install/ubuntu/

**2. installtion of minikube**
https://minikube.sigs.k8s.io/docs/start/

**3. setup of nginx ingress controller**
minikube addons enable ingress

**4.installtion of Helm binary**
https://helm.sh/docs/intro/install/

**5. install of loki with helm charts**
https://artifacthub.io/packages/helm/grafana/loki (loki + minlo)
  1.deploy minlo in minikube as it is pre-requesite
  
  2.install loki

  3. install promtail and grafana
