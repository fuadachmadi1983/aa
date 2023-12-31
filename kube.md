NAME                                         READY   STATUS      RESTARTS   AGE
pod/coredns-77ccd57875-px2zz                 1/1     Running     0          13m
pod/local-path-provisioner-957fdf8bc-ltb55   1/1     Running     0          13m
pod/helm-install-traefik-crd-qbkdm           0/1     Completed   0          13m
pod/helm-install-traefik-kv5qv               0/1     Completed   1          13m
pod/svclb-traefik-739534bd-6c27g             2/2     Running     0          13m
pod/traefik-64f55bb67d-vnzc5                 1/1     Running     0          13m
pod/metrics-server-648b5df564-z7nm4          1/1     Running     0          13m

NAME                     TYPE           CLUSTER-IP     EXTERNAL-IP   PORT(S)                      AGE
service/kube-dns         ClusterIP      10.43.0.10     <none>        53/UDP,53/TCP,9153/TCP       13m
service/metrics-server   ClusterIP      10.43.40.192   <none>        443/TCP                      13m
service/traefik          LoadBalancer   10.43.34.100   172.23.0.3    80:31072/TCP,443:31204/TCP   13m

NAME                                    DESIRED   CURRENT   READY   UP-TO-DATE   AVAILABLE   NODE SELECTOR   AGE
daemonset.apps/svclb-traefik-739534bd   1         1         1       1            1           <none>          13m

NAME                                     READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/coredns                  1/1     1            1           13m
deployment.apps/local-path-provisioner   1/1     1            1           13m
deployment.apps/traefik                  1/1     1            1           13m
deployment.apps/metrics-server           1/1     1            1           13m

NAME                                               DESIRED   CURRENT   READY   AGE
replicaset.apps/coredns-77ccd57875                 1         1         1       13m
replicaset.apps/local-path-provisioner-957fdf8bc   1         1         1       13m
replicaset.apps/traefik-64f55bb67d                 1         1         1       13m
replicaset.apps/metrics-server-648b5df564          1         1         1       13m

NAME                                 COMPLETIONS   DURATION   AGE
job.batch/helm-install-traefik-crd   1/1           20s        13m
job.batch/helm-install-traefik       1/1           23s        13m
