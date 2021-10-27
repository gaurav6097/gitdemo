    1  kubectl get pods -n uat
    2  kubectl logs -n uat redis-master-56d4ffcddf-565qj
    3  kubectl get pods -n uat
    4  kubectl logs -n uat redis-slave-55cd7d77c9-bpzzw 
    5  kubectl exec -it redis-slave -- redis-cli
    6  kubectl exec -it redis-slave -- redis-cli -n uat
    7  kubectl get pods -n uat
    8  kubectl exec -it redis-slave-55cd7d77c9-bpzzw -- redis-cli -n uat
    9  kubectl exec -it redis-master -- redis-cli -n uat
   10  kubectl exec -it -n uat redis-master -- redis-cli
   11  kubectl get pods -n uat
   12  kubectl exec -it -n uat redis-master-56d4ffcddf-565qj -- redis-cli
   13  kubectl exec -it -n uat redis-slave-55cd7d77c9-bpzzw -- redis-cli
   14  gcloud container clusters get-credentials autopilot-cluster-1 --region us-central1 --project business-transformers
   15  cd testredis/
   16  cp ../icici.org/smartcity_prod/redisslave.yaml .
   17  ls
   18  cat redis-pod.yaml |less
   19  gcloud container clusters get-credentials autopilot-cluster-1 --region us-central1 --project business-transformers
   20  cd testredis/
   21  ls
   22  vi redisslave.yaml 
   23  rm .redisslave.yaml.swp
   24  cd testredis/
   25  ls
   26  cat redisslave.yaml 
   27  vi redisslave.yaml 
   28  gcloud container clusters get-credentials autopilot-cluster-1 --region us-central1 --project business-transformers
   29  cd testredis/
   30  ls
   31  cat redisslave.yaml |less
   32  kubectl apply -f redisslave.yaml 
   33  cat redisslave.yaml |less
   34  cat redis-pod.yaml |less
   35  cat redisslave.yaml |less
   36  vi redisslave.yaml 
   37  rm .redisslave.yaml.swp
   38  vi redisslave.yaml 
   39  kubectl apply -f redisslave.yaml 
   40  kubectl get pods
   41  kubectl describe configmap/example-redis-config
   42  kubectl exec -it -n uat redis-slave-674bf6595b-h8mx2 -- redis-cli
   43  kubectl exec -it redis-slave-674bf6595b-h8mx2 -- redis-cli
   44  kubectl get pods
   45  kubectl exec -it redis-master -- redis-cli
   46  kubectl describe configmap/example-redis-config
   47  vi example-redis-config.yaml 
   48  kubectl apply -f example-redis-config.yaml 
   49  kubectl describe configmap/example-redis-config
   50  history
   51  cat redis-pod.yaml |less
   52  cat redisslave.yaml |less
   53  kubectl  apply -f redisslave.yaml 
   54  vi redis-pod.yaml 
   55  kubectl  apply -f redis-pod.yaml 
   56  vi redis-pod.yaml 
   57  kubectl  apply -f redis-pod.yaml 
   58  kubectl get pods
   59  kubectl exec -it redis-slave-674bf6595b-mdt9t -- redis-cli
   60  ls
   61  cp build_upgrade_21.6.0_20210628.sh build_upgrade_21.6.0_20210715.sh
   62  vi build_upgrade_21.6.0_20210715.sh
   63  gsutil cp build_upgrade_21.6.0_20210715.sh gs://prod_backups1/build_upgrade/
   64  gcloud container clusters get-credentials autopilot-cluster-1 --region us-central1 --project business-transformers
   65  cd testredis/
   66  cp ../icici.org/smartcity_prod/redismaster.yaml .
   67  ls
   68  cat redisslave.yaml |less
   69  cat redis-pod.yaml |less
   70  vi redismaster.yaml 
   71  cat redis-pod.yaml |less
   72  vi redismaster.yaml 
   73  vi redisslave.yaml 
   74  cat redisslave.yaml |less
   75  vi example-redis-config.yaml 
   76  mv example-redis-config.yaml common-redis-config.yaml
   77  ls
   78  kubectl apply -f common-redis-config.yaml 
   79  kubectl apply -f redismaster.yaml 
   80  kubectl apply -f redisslave.yaml 
   81  kubectl get pods
   82  kubectl exec -it redis-master-ff9b9b5d-jzkkb -- redis-cli
   83  kubectl exec -it redis-slave-7b87676849-p24ns -- redis-cli
   84  vi redisslave.yaml 
   85  vi redismaster.yaml 
   86  vi redisslave.yaml 
   87  gcloud container clusters get-credentials icici-common-services-uat-cluster --region asia-south1 --project common-services-uat-279216
   88  kubectl apply -f common-redis-config.yaml -n uat
   89  kubectl apply -f redismaster.yaml -n uat
   90  kubectl apply -f redisslave.yaml -n uat
   91  kubectl get pods -n uat
   92  kubectl logs redis-master-75ff4bc988-mz9kr -n uat
   93  kubectl get pods -n uat
   94  kubectl logs redis-slave-fbbdb964f-5ptts -n uat
   95  kubectl logs redis-master-75ff4bc988-mz9kr -n uat
   96  kubectl logs redis-slave-fbbdb964f-5ptts -n uat
   97  kubectl logs redis-master-75ff4bc988-mz9kr -n uat
   98  gcloud container clusters get-credentials icici-common-services-uat-cluster --region asia-south1 --project common-services-uat-279216
   99  kubectl get pods -n uat
  100  kubectl logs redis-master-75ff4bc988-mz9kr -n uat
  101  kubectl logs redis-slave-fbbdb964f-5ptts -n uat
  102  gcloud container clusters get-credentials autopilot-cluster-1 --region us-central1 --project business-transformers
  103  gcloud container clusters get-credentials common-services-dev-cluster --region asia-south1 --project common-services-dev
  104  gcloud config set project common-services-dev
  105  gcloud container clusters get-credentials common-services-dev-cluster --region asia-south1 --project common-services-dev
  106  cd testredis/
  107  ls
  108  kubectl apply -f common-redis-config.yaml -n dev
  109  kubectl apply -f redismaster.yaml 
  110  kubectl apply -f redismaster.yaml -n dev
  111  kubectl apply -f redisslave.yaml -n dev
  112  kubectl get pods
  113  kubectl get pods -n dev
  114  kubectl exec -it -n dev redis-master-75ff4bc988-8gszp -- redis-cli
  115  cat common-redis-config.yaml |less
  116  gcloud container clusters get-credentials tsg1-ifee-prod-cluster --region asia-south1 --project tsg1-ifee-prod-279216
  117  cat common-redis-config.yaml |less
  118  kubectl apply -f common-redis-config.yaml -n prod
  119  cat common-redis-config.yaml |less
  120  cat redisslave.yaml |less
  121  kubectl apply -f redismaster.yaml -n prod
  122  kubectl apply -f redisslave.yaml -n prod
  123  kubectl get pods -n prod
  124  kubectl exec -it -n prod redis-master-75ff4bc988-mx6sw -- /bin/bash
  125  kubectl exec -it -n prod redis-master-75ff4bc988-mx6sw -- redis-cli
  126  kubectl exec -it -n prod redis-slave-fbbdb964f-gr8fn -- redis-cli
  127  gcloud config set project tsg1-ifee-dev
  128  gcloud container clusters get-credentials tsg1-ifee-dev-cluster --region asia-south1 --project tsg1-ifee-dev
  129  kubectl apply -f common-redis-config.yaml -n dev
  130  cd testredis/
  131  kubectl apply -f common-redis-config.yaml -n dev
  132  kubectl apply -f redismaster.yaml -n dev
  133  kubectl apply -f redisslave.yaml -n dev
  134  gcloud container clusters get-credentials tsg1-ifee-uat-cluster --region asia-south1 --project tsg1-ifee-uat-279216
  135  kubectl apply -f common-redis-config.yaml -n uat
  136  kubectl apply -f redismaster.yaml -n uat
  137  kubectl apply -f redisslave.yaml -n uat
  138  gcloud container clusters get-credentials tsg1-smartcity-prod-cluster --region asia-south1 --project tsg1-smartcity-prod-279216
  139  kubectl apply -f common-redis-config.yaml -n prod
  140  kubectl apply -f redismaster.yaml -n prod
  141  kubectl apply -f redisslave.yaml -n prod
  142  gcloud container clusters get-credentials tsg1-smartcity-dev-cluster --region asia-south1 --project tsg1-smartcity-dev
  143  kubectl apply -f common-redis-config.yaml -n dev
  144  kubectl apply -f redismaster.yaml -n dev
  145  kubectl apply -f redisslave.yaml -n dev
  146  gcloud container clusters get-credentials tsg1-smartcity-uat-cluster --region asia-south1 --project tsg1-smartcity-uat
  147  kubectl apply -f common-redis-config.yaml -n uat
  148  kubectl apply -f redismaster.yaml -n uat
  149  kubectl apply -f redisslave.yaml -n uat
  150  gcloud container clusters get-credentials common-services-prod-cluster --region asia-south1 --project common-services-prod-279216
  151  kubectl apply -f common-redis-config.yaml -n prod
  152  kubectl apply -f redismaster.yaml -n prod
  153  kubectl apply -f redisslave.yaml -n prod
  154  ls
  155  cat common-redis-config.yaml|less
  156  cat redismaster.yaml |less
  157  gcloud container clusters get-credentials common-services-prod-cluster --region asia-south1 --project common-services-prod-279216
  158  kubectl get pods -n prod
  159  kubectl exec -it -n prod redis-master-75ff4bc988-5gv86 -- redis-cli
  160  kubectl exec -it -n prod redis-master-75ff4bc988-5gv86 -- /bin/bash
  161  histroy
  162  history
  163  gcloud beta compute instances create jump-host --project=business-transformers --zone=us-central1-a --machine-type=n2-standard-2 --subnet=ikea-app-subnet --private-network-ip=10.65.61.100 --source-machine-image projects/optimusdev/global/machineImages/jump-host-img-20210321 --service-account 1875750515-compute@developer.gserviceaccount.com
  164  gcloud container clusters get-credentials common-services-dev-cluster --region asia-south1 --project common-services-dev
  165  kubectl get pods -n dev
  166  kubectl logs common-api-7b688b5b8-d895q -n dev
  167  gcloud container clusters get-credentials asia-south1-comm-airflow-3884d1e8-gke --zone asia-south1-a --project comm-307708
  168  kubectl get pods -n composer-1-16-8-airflow-1-10-15-3884d1e8
  169  kubectl logs airflow-scheduler-66df495b59-4xl5m -n composer-1-16-8-airflow-1-10-15-3884d1e8
  170  kubectl logs airflow-scheduler-66df495b59-4xl5m
  171  kubectl logs airflow-scheduler -n composer-1-16-8-airflow-1-10-15-3884d1e8
  172  kubectl describe pod airflow-scheduler-66df495b59-4xl5m -n composer-1-16-8-airflow-1-10-15-3884d1e8
  173  kubectl logs airflow-scheduler-66df495b59-4xl5m -n composer-1-16-8-airflow-1-10-15-3884d1e8
  174  kubectl get pods
  175  kubectl logs airflow-monitoring-69c4fdc67c-9mg7x 
  176  dig +short leveredgestaging.hulcd.com
  177  gcloud config auth project hul-leveredge-ikea
  178  gcloud auth config hul-leveredge-ikea
  179  gcloud config set project hul-leveredge-ikea
  180  ls
  181  cd testdir/
  182  ls
  183  gsutil cp gs://prod_backups1/build_upgrade/build_upgrade_21.7.0_20210723.sh .
  184  ls
  185  vi build_upgrade_21.7.0_20210723.sh 
  186  mv build_upgrade_21.7.0_20210723.sh build_upgrade_21.7.0_20210803.sh
  187  ls
  188  gsutil cp build_upgrade_21.7.0_20210803.sh gs://prod_backups1/build_upgrade/
  189  gcloud container clusters get-credentials asia-south1-comm-airflow-3884d1e8-gke --zone asia-south1-a --project comm-307708
  190  kubectl get pods -n composer-1-16-8-airflow-1-10-15-3884d1e8
  191  kubectl get hpa -n composer-1-16-8-airflow-1-10-15-3884d1e8
  192  kubectl autoscale deployment airflow-scheduler --cpu-percent=50 --min=1 --max=3 -n composer-1-16-8-airflow-1-10-15-3884d1e8
  193  kubectl get hpa -n composer-1-16-8-airflow-1-10-15-3884d1e8
  194  kubectl describe hpa -n airflow-scheduler
  195  kubectl describe hpa -n airflow-scheduler -n composer-1-16-8-airflow-1-10-15-3884d1e8
  196  kubectl get hpa -n composer-1-16-8-airflow-1-10-15-3884d1e8
  197  gcloud auth list
  198  gsutil cp gs://asia-south1-comm-airflow-3884d1e8-bucket/airflow.cfg .
  199  gcloud sql connect comm-db-uat --user=root --quiet
  200  history
  201  gcloud logging read 'resource.type="cloudsql_database" AND resource.labels.database_id="comm-uat:comm-db-uat" AND logName=""projects/comm-uat/logs/cloudsql.googleapis.com%2Fmysql-general.log" OR "projects/comm-uat/logs/cloudsql.googleapis.com%2Fmysql.err"" AND timestamp>="2021-08-10T09:30:19.998313Z" AND timestamp<="2021-08-10T11:31:04.567550Z" --format=json >> logs
  202  gcloud logging read 'resource.type="cloudsql_database" AND resource.labels.database_id="comm-uat:comm-db-uat" AND logName="projects/comm-uat/logs/cloudsql.googleapis.com%2Fmysql.err" AND timestamp>="2021-08-10T09:30:19.998313Z" AND timestamp<="2021-08-10T11:31:04.567550Z" --format=json >> logs
  203  gcloud logging read 'resource.type="cloudsql_database" AND resource.labels.database_id="comm-uat:comm-db-uat" AND logName="projects/comm-uat/logs/cloudsql.googleapis.com%2Fmysql.err" AND timestamp>="2021-08-10T09:30:19.998313Z" AND timestamp<="2021-08-10T11:31:04.567550Z"' --format=json >> logs
  204  cat logs |less
  205  gcloud logging read 'resource.type="cloudsql_database" AND resource.labels.database_id="comm-uat:comm-db-uat" AND logName="projects/comm-uat/logs/cloudsql.googleapis.com%2Fmysql.err" AND timestamp>="2021-08-10T09:30:19.998313Z" AND timestamp<="2021-08-10T11:31:04.567550Z"' --format=json >> logs1
  206  ll|grep logs1
  207  cat logs1
  208  history
  209  cat logs1|less
  210  gcloud container clusters get-credentials asia-south1-comm-uat-airflo-cbd58fc7-gke --zone asia-south1-a --project comm-uat
  211  history
  212  cd icici.org/
  213  ls
  214  cd smartcity_prod/
  215  ls
  216  cd ..
  217  cd ../icici-bank/
  218  ls
  219  cat config |less
  220  kubectl exec --stdin --tty airflow-worker-868c75b5cc-f4g2q -n composer-1-16-5-airflow-1-10-15-cbd58fc7  -- /bin/bash
  221  ls
  222  vi config 
  223  kubectl create configmap ip-masq-agent --from-file config --namespace composer-1-16-5-airflow-1-10-15-cbd58fc7
  224  cat ip-masq-agent.yaml |less
  225  kubectl apply -f ip-masq-agent.yaml 
  226  iptables -t nat -L IP-MASQ
  227  kubectl get configmap -n composer-1-16-5-airflow-1-10-15-cbd58fc7
  228  kubectl exec --stdin --tty airflow-worker-868c75b5cc-f4g2q -n composer-1-16-5-airflow-1-10-15-cbd58fc7  -- /bin/bash
  229  kubectl create configmap ip-masq-agent --from-file config --namespace kube-system
  230  kubectl exec --stdin --tty airflow-worker-868c75b5cc-f4g2q -n composer-1-16-5-airflow-1-10-15-cbd58fc7  -- /bin/bash
  231  kubectl get configmap -n composer-1-16-5-airflow-1-10-15-cbd58fc7
  232  gcloud container clusters get-credentials common-services-dev-cluster --region asia-south1 --project common-services-dev
  233  kubectl get configmap -n dev
  234  kubectl get configmap -n kube-system
  235  gcloud container clusters get-credentials asia-south1-comm-uat-airflo-cbd58fc7-gke --zone asia-south1-a --project comm-uat
  236  iptables -t nat -L IP-MASQ
  237  kubectl get configmap -n composer-1-16-5-airflow-1-10-15-cbd58fc7
  238  kubectl delete configmap ip-masq-agent -n composer-1-16-5-airflow-1-10-15-cbd58fc7
  239  kubectl delete configmap ip-masq-agent -n kube-system
  240  ls
  241  kubectl create configmap ip-masq-agent --from-file config --namespace kube-system
  242  kubectl apply -f ip-masq-agent.yaml 
  243  ls
  244  cat backup_91.sh |less
  245  gsutil cp LeverEdge_R21.8.0_20210825 .
  246  gsutil cp gs://prod_backups1/build_upgrade/build_upgrade_21.8.0_20210825.sh .
  247  vi build_upgrade_21.8.0_20210825.sh 
  248  gsutil cp LeverEdge_R21.8.0_20210825 gs://prod_backups1/build_upgrade/
  249  gsutil cp  build_upgrade_21.8.0_20210825.sh gs://prod_backups1/build_upgrade/
  250  gcloud services enable servicenetworking.googleapis.com --project=common-services-staging
  251  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  252  kubectl get namespaces
  253  kubectl create namespace stage
  254  kubectl get namespaces
  255  docker pull asia.gcr.io/common-services-staging/common-api:v1
  256  docker images
  257  kubectl  run common-api --image=asia.gcr.io/common-services-staging/common-api:v1  -n stage --requests=cpu=300m
  258  kubectl  create deployment common-api --image=asia.gcr.io/common-services-staging/common-api:v1  -n stage --requests=cpu=300m
  259  ls
  260  cd icici.org/
  261  ls
  262  mkdir common_stage
  263  cd common_stage/
  264  mv /home/gaurav_singh/common-services-staging-15b5d7caeabc.json .
  265  ls
  266  ls ../../icici-bank/secrets/
  267  mv common-services-staging-15b5d7caeabc.json common-services-stage.json
  268  ls
  269  history
  270  kubectl create secret svc-accnt --from-flie common-services-stage.json -n stage
  271  kubectl create secret generic svc-accnt --from-flie common-services-stage.json -n stage
  272  kubectl create secret generic svc-accnt --from-env-flie common-services-stage.json -n stage
  273  kubectl create secret generic svc-accnt --from-flie=common-services-stage.json -n stage
  274  kubectl create secret generic --help
  275  kubectl create secret generic svc-accnt --from-flie /home/gaurav_singh/icici.org/common_stage/common-services-stage.json -n stage
  276  kubectl create secret generic svc-accnt --from-flie /home/gaurav_singh/icici.org/common_stage/common-services-stage.json 
  277  kubectl create secret generic my-secret --from-file=/home/gaurav_singh/icici.org/common_stage/common-services-stage.json
  278  kubectl create secret generic svc-accnt --from-file=/home/gaurav_singh/icici.org/common_stage/common-services-stage.json -n stage
  279  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  280  history
  281  cd icici-bank/
  282  ls
  283  cat config |less
  284  vi config 
  285  kubectl create configmap ip-masq-agent --from-file config --namespace kube-system
  286  kubectl apply -f ip-masq-agent.yaml
  287  cd Redis-latest/
  288  ls
  289  cd ../../icici.org/
  290  ls
  291  cd ../testredis/
  292  ls
  293  cat redis-pod.yaml |less
  294  cat redismaster.yaml |less
  295  cat common-redis-config.yaml |less
  296  kubectl apply -f common-redis-config.yaml -n stage;kubectl apply -f redismaster.yaml -n stage ;kubectl apply -f redisslave.yaml -n stage
  297  cd ../icici-bank/
  298  ls
  299  cat smartcity-prod-internal-lb.yaml |less
  300  cd common-service-uat/
  301  ls
  302  cat users-api-uat-internal-lb.yaml |less
  303  ls
  304  cat users-api-uat-internal-lb.yaml |less
  305  kubectl apply -f users-api-uat-internal-lb.yaml  -n stage
  306  cd ..
  307  ls
  308  vi smartcity-prod-internal-lb.yaml 
  309  rm .smartcity-prod-internal-lb.yaml.swp
  310  cp smartcity-prod-internal-lb.yaml transactions-stage-internal-lb.yaml 
  311  vi transactions-stage-internal-lb.yaml 
  312  cat common-service-uat/users-api-uat-internal-lb.yaml |less
  313  cd common-service-uat/
  314  cp users-api-uat-internal-lb.yaml transactions-stage-internal-lb.yaml
  315  vi transactions-stage-internal-lb.yaml 
  316  kubectl apply -f transactions-stage-internal-lb.yaml -n stage
  317  ls
  318  cd ../
  319  ls
  320  cd common-service
  321  cd common-services-prod/
  322  ls
  323  cd ../../icici.org/
  324  ls
  325  cd smartcity_prod/
  326  ls
  327  curl -X GET -H "Authorization: Bearer "$(gcloud auth print-access-token) "https://sqladmin.googleapis.com/sql/v1beta4/projects/comm-uat/instances/comm-db-uat-clone/backupRuns"
  328  mkdir commlive
  329  cd commlive/
  330  vi request.json
  331  ls
  332  cd icici.org/
  333  ls
  334  cd university_prod/
  335  ls
  336  cd ../../icici-bank/
  337  ls
  338  cd common-services-prod/
  339  ls
  340  cd ../icici-common-service-dev/
  341  ls
  342  cat common-services-dev-ingress.yaml |less
  343  cp common-services-dev-ingress.yaml common-services-stage-ingress.yaml 
  344  vi common-services-stage-ingress.yaml 
  345  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  346  kubectl apply -f common-services-stage-ingress.yaml -n stage
  347  Firewall change required by security admin: `gcloud compute firewall-rules create k8s-fw-l7--0e5ae31054c7677c --network icici-stage-vpc --description "GCE L7 firewall rule" --allow tcp:30000-32767 --source-ranges 130.211.0.0/22,35.191.0.0/16 --target-tags gke-icici-common-services-stage-cluster-7b96f811-node --project tsg1-ecosystem-sharedservice`
  348  gcloud compute firewall-rules create k8s-fw-l7--0e5ae31054c7677c --network icici-stage-vpc --description "GCE L7 firewall rule" --allow tcp:30000-32767 --source-ranges 130.211.0.0/22,35.191.0.0/16 --target-tags gke-icici-common-services-stage-cluster-7b96f811-node --project tsg1-ecosystem-sharedservice
  349  dig +short icici-app-staging.mediaagility.com 
  350  gcloud cobfig set project comm-307708
  351  gcloud config set project comm-307708
  352  gsutil cp gs://asia-south1-comm-airflow-3884d1e8-bucket/logs/GODB_LOAD_VIEW_PARTY_EXPLODE_910/populate_view_party_explode_new/2021-08-28T18:10:22.311476+00:00/1.log .
  353  head -l 100 1.log 
  354  head -n 100 1.log 
  355  head -n 50 1.log 
  356  gcloud container clusters get-credentials tsg1-admin-stage-cluster --region asia-south1 --project tsg1-admin-staging
  357  kubectl create namespace stage
  358  cd icici.org/
  359  ls
  360  cd ../icici-bank/
  361  ls
  362  vi config 
  363  history
  364  ls
  365  kubectl create configmap ip-masq-agent --from-file config --namespace kube-system; kubectl apply -f ip-masq-agent.yaml
  366  cd ../testredis/
  367  kubectl apply -f common-redis-config.yaml -n stage;kubectl apply -f redismaster.yaml -n stage ;kubectl apply -f redisslave.yaml -n stage
  368  cd /icici-bank/common-service-uat/
  369  cd ../icici-bank/common-service-uat/
  370  ls
  371  cp transactions-stage-internal-lb.yaml admin-stage-internal-lb.yaml
  372  vi admin-stage-internal-lb.yaml 
  373  kubectl apply -f admin-stage-internal-lb.yaml -n stage
  374  gcloud container clusters get-credentials icici-eco-app-stage-cluster --region asia-south1 --project tsg1-eco-app-stage
  375  cd ../../icici-bank/
  376  vi config 
  377  gcloud container clusters get-credentials tsg1-admin-stage-cluster --region asia-south1 --project tsg1-admin-staging
  378  kubectl create configmap ip-masq-agent --from-file config --namespace kube-system; kubectl apply -f ip-masq-agent.yaml
  379  kubectl get config -n kube-system
  380  kubectl get configmap -n kube-system
  381  kubectl delete configmap ip-masq-agent -n kube-system
  382  kubectl create configmap ip-masq-agent --from-file config --namespace kube-system; kubectl apply -f ip-masq-agent.yaml
  383  gcloud container clusters get-credentials icici-eco-app-stage-cluster --region asia-south1 --project tsg1-eco-app-stage
  384  vi config 
  385  kubectl create configmap ip-masq-agent --from-file config --namespace kube-system; kubectl apply -f ip-masq-agent.yaml
  386  cd ../testredis/
  387  kubectl apply -f common-redis-config.yaml -n stage;kubectl apply -f redismaster.yaml -n stage ;kubectl apply -f redisslave.yaml -n stage
  388  kubectl create namespace stage
  389  kubectl apply -f common-redis-config.yaml -n stage;kubectl apply -f redismaster.yaml -n stage ;kubectl apply -f redisslave.yaml -n stage
  390  cd ..
  391  cd /icici-bank/common-service-uat/
  392  cd icici-bank/common-service-uat/
  393  ls
  394  cp transactions-stage-internal-lb.yaml eco-app-internal-lb.yaml
  395  vi eco-app-internal-lb.yaml 
  396  kubectl apply -f eco-app-internal-lb.yaml -n stage
  397  gcloud container clusters get-credentials tsg1-ifee-stage-cluster --region asia-south1 --project tsg1-ifee-stage
  398  kubectl create namespace stage
  399  cd ../../testredis/
  400  kubectl apply -f common-redis-config.yaml -n stage;kubectl apply -f redismaster.yaml -n stage ;kubectl apply -f redisslave.yaml -n stage
  401  cd ../icici-bank/
  402  vi config 
  403  kubectl create configmap ip-masq-agent --from-file config --namespace kube-system; kubectl apply -f ip-masq-agent.yaml
  404  cd ..
  405  cd icici-bank/common-service-uat/
  406  ls
  407  cp eco-app-internal-lb.yaml ifee-stage-internal-lb.yaml 
  408  vi ifee-stage-internal-lb.yaml 
  409  kubectl apply -f ifee-stage-internal-lb.yaml -n stage
  410  gcloud compute firewall-rules create k8s-7875c2d6dc870528-node-hc --network icici-stage-vpc --description "" --allow tcp:10256 --source-ranges 130.211.0.0/22,209.85.152.0/22,209.85.204.0/22,35.191.0.0/16 --target-tags gke-tsg1-ifee-stage-cluster-fa6a2335-node --project tsg1-ecosystem-sharedservice
  411  gcloud container clusters get-credentials tsg1-smartcity-stage-cluster --region asia-south1 --project tsg1-smartcity-stage
  412  ls
  413  kubectl create namespace stage
  414  cd ../
  415  ls
  416  vi config 
  417  kubectl create configmap ip-masq-agent --from-file config --namespace kube-system; kubectl apply -f ip-masq-agent.yaml
  418  cd ../testredis/
  419  kubectl apply -f common-redis-config.yaml -n stage;kubectl apply -f redismaster.yaml -n stage ;kubectl apply -f redisslave.yaml -n stage
  420  cd ..
  421  cd icici-bank/common-service-uat/
  422  ls
  423  cp eco-app-internal-lb.yaml smartcity-stage-internal-lb.yaml
  424  vi smartcity-stage-internal-lb.yaml 
  425  kubectl apply -f smartcity-stage-internal-lb.yaml -n stage
  426  gcloud compute firewall-rules create k8s-fw-af57cb981266b42c4a7197e08b594057 --network icici-stage-vpc --description "{\"kubernetes.io/service-name\":\"stage/smartcity-api-service\", \"kubernetes.io/service-ip\":\"10.245.0.5\"}" --allow tcp:80 --source-ranges 0.0.0.0/0 --target-tags gke-tsg1-smartcity-stage-cluster-af75fadd-node --project tsg1-ecosystem-sharedservice
  427  gcloud compute firewall-rules create k8s-a121a9bd61d7e06c-node-hc --network icici-stage-vpc --description "" --allow tcp:10256 --source-ranges 130.211.0.0/22,209.85.152.0/22,209.85.204.0/22,35.191.0.0/16 --target-tags gke-tsg1-smartcity-stage-cluster-af75fadd-node --project tsg1-ecosystem-sharedservice
  428  gcloud compute firewall-rules create k8s-fw-ae4a6cbae3986414dbba1c2fd518f602 --network icici-stage-vpc --description "{\"kubernetes.io/service-name\":\"stage/university-services-service\", \"kubernetes.io/service-ip\":\"10.250.0.5\"}" --allow tcp:80 --source-ranges 0.0.0.0/0 --target-tags gke-tsg1-ifee-stage-cluster-fa6a2335-node --project tsg1-ecosystem-sharedservice
  429  gcloud compute firewall-rules create k8s-fw-a7979d0c8aab74c62a787cb31de883ac --network icici-stage-vpc --description "{\"kubernetes.io/service-name\":\"stage/eco-app-internal-service\", \"kubernetes.io/service-ip\":\"10.240.0.7\"}" --allow tcp:80 --source-ranges 0.0.0.0/0 --target-tags gke-icici-eco-app-stage-cluster-5e2c04e1-node --project tsg1-ecosystem-sharedservice
  430  gcloud compute firewall-rules create k8s-98b1a03087096460-node-hc --network icici-stage-vpc --description "" --allow tcp:10256 --source-ranges 130.211.0.0/22,209.85.152.0/22,209.85.204.0/22,35.191.0.0/16 --target-tags gke-icici-eco-app-stage-cluster-5e2c04e1-node --project tsg1-ecosystem-sharedservice
  431  gcloud compute firewall-rules create k8s-98b1a03087096460-node-hc --network icici-stage-vpc --description "" --allow tcp:10256 --source-ranges 130.211.0.0/22,209.85.152.0/22,209.85.204.0/22,35.191.0.0/16 --target-tags gke-tsg1-admin-stage-cluster-c7692e39-node --project tsg1-ecosystem-sharedservice
  432  gcloud compute firewall-rules create k8s-c7692e39-node-hc --network icici-stage-vpc --description "" --allow tcp:10256 --source-ranges 130.211.0.0/22,209.85.152.0/22,209.85.204.0/22,35.191.0.0/16 --target-tags gke-tsg1-admin-stage-cluster-c7692e39-node --project tsg1-ecosystem-sharedservice
  433  gcloud compute firewall-rules create k8s-fw-c7692e39 --network icici-stage-vpc --description "{\"kubernetes.io/service-name\":\"stage/eco-app-internal-service\", \"kubernetes.io/service-ip\":\"10.240.0.7\"}" --allow tcp:80 --source-ranges 0.0.0.0/0 --target-tags gke-tsg1-admin-stage-cluster-c7692e39-node --project tsg1-ecosystem-sharedservice
  434  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  435  kubectl get pods -n stage
  436  kubectl exec -it -n stage common-api-847d4db985-4sbkg  -- /bin/bash
  437  kubectl exec -it -n stage common-api-847d4db985-4sbkg  -- /bin/sh
  438  history
  439  kubectl get pods -n stage
  440  kubectl exec -it -n stage common-api-847d4db985-4sbkg -- /bin/bash
  441  kubectl exec -it -n stage paymentgateway-api-58cfd74f5b-d7gxm -- /bin/bash
  442  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  443  kubectl exec -it -n stage paymentgateway-api-58cfd74f5b-d7gxm -- /bin/bash
  444  kubectl exec -it -n stage common-api-847d4db985-4sbkg -- /bin/bash
  445  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  446  kubectl exec -it -n stage common-api-847d4db985-4sbkg -- /bin/bash
  447  gcloud container clusters get-credentials tsg1-smartcity-stage-cluster --region asia-south1 --project tsg1-smartcity-stage
  448  kubectl get pods -n stage
  449  kubectl exec -it -n stage aycraft-api-7d946799d7-ndjcp -- /bin/bash
  450  kubectl exec -it -n stage paycraft-api-7d946799d7-ndjcp -- /bin/bash
  451  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  452  kubectl get nodes -o wide
  453  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  454  kubectl get pods -n stage
  455  kubectl exec -it -n stage common-api-847d4db985-4d45t -- /bin/bash
  456  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  457  kubectl exec -it -n stage common-api-847d4db985-4d45t -- /bin/bash
  458  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  459  kubectl exec -it -n stage common-api-847d4db985-4d45t -- /bin/bash
  460  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  461  kubectl exec -it -n stage common-api-847d4db985-4d45t -- /bin/bash
  462  history
  463  cd icici-bank/
  464  ls
  465  cd common-service-uat
  466  ls
  467  cat smartcity-stage-internal-lb.yaml |less
  468  cat transactions-stage-internal-lb.yaml |less
  469  cat smartcity-stage-internal-lb.yaml |less
  470  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  471  kubectl exec -it -n stage common-api-847d4db985-4d45t -- /bin/bash
  472  ls
  473  cp transactions-stage-internal-lb.yaml smartcity-stage-internal-lb-1.yaml 
  474  vi smartcity-stage-internal-lb-1.yaml 
  475  kubectl apply -f smartcity-stage-internal-lb -n stage
  476  gcloud container clusters get-credentials tsg1-smartcity-stage-cluster --region asia-south1 --project tsg1-smartcity-stage
  477  ls
  478  kubectl apply -f smartcity-stage-internal-lb-1.yaml -n stage
  479  gcloud compute firewall-rules create k8s-fw-a31b2010c19d940a6afdeff850c5048b --network icici-stage-vpc --description "{\"kubernetes.io/service-name\":\"stage/paycraft-api-services-internal-service\", \"kubernetes.io/service-ip\":\"10.245.0.6\"}" --allow tcp:80 --source-ranges 0.0.0.0/0 --target-tags gke-tsg1-smartcity-stage-cluster-af75fadd-node --project tsg1-ecosystem-sharedservice
  480  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  481  kubectl exec -it -n stage common-api-847d4db985-4d45t -- /bin/bash
  482  gcloud container clusters get-credentials icici-common-services-stage-cluster --region asia-south1 --project common-services-staging
  483  kubectl exec -it -n stage common-api-847d4db985-4d45t -- /bin/bash
  484  ls
  485  rm logs
  486  rm logs1
  487  gcloud logging read 'resource.type="cloudsql_database" AND resource.labels.database_id="comm-307708:comm-db-prod" AND logName=""projects/comm-307708/logs/cloudsql.googleapis.com%2Fmysql-general.log" OR "projects/comm-307708/logs/cloudsql.googleapis.com%2Fmysql.err"" AND timestamp>="2021-09-09T15:30:48.962743Z" AND timestamp<="2021-09-09T16:59:59.853820Z"' --format=json >> logs
  488  gcloud logging read 'resource.type="cloudsql_database" AND resource.labels.database_id="comm-307708:comm-db-prod" AND logName="projects/comm-307708/logs/cloudsql.googleapis.com%2Fmysql-general.log" OR "projects/comm-307708/logs/cloudsql.googleapis.com%2Fmysql.err" AND timestamp>="2021-09-09T15:30:48.962743Z" AND timestamp<="2021-09-09T16:59:59.853820Z"' --format=json >> logs
  489  cat logs|less
  490  history
  491  ls
  492  cd hul_scripts/
  493  ls
  494  cd ../dr_hul/
  495  ls
  496  gcloud config set project hul-leveredge-ikea
  497  gcloud beta compute instances create app-dr --project=hul-ikea --zone=us-central1-a --machine-type=n2-highmem-4 --subnet=app-server-subnet --private-network-ip=10.0.1.91 --source-machine-image projects/hul-leveredge-ikea/global/machineImages/app-golden-image --service-account 823706900550-compute@developer.gserviceaccount.com
  498  gcloud beta compute instances create dbserver-dr --project=hul-ikea --zone=us-central1-a --machine-type=n2-custom-10-81920 --subnet=db-server-subnet --private-network-ip=10.0.2.91 --source-machine-image projects/hul-leveredge-ikea/global/machineImages/dbserver-golden-img --service-account 823706900550-compute@developer.gserviceaccount.com
  499  gcloud beta compute instances create dbserver91 --project=hul-ikea --zone=us-central1-a --machine-type=n2-custom-10-81920 --subnet=db-server-subnet --private-network-ip=10.0.2.91 --source-machine-image projects/hul-leveredge-ikea/global/machineImages/dbserver91-img-20210915 --service-account 823706900550-compute@developer.gserviceaccount.com
  500  history
  501  ls
  502  gcloud config set project business-transformers
  503  mkdir gitdemo
  504  cd gitdemo/
  505  history >> readme.md
