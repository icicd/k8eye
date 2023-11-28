# k8eye

## config file

```
Name: k8eye.job
ListenOn:
Mode: dev

Log:
  ServiceName: k8eye.job
  Level: debug
  Mode: "console"

DB:
  Type: mysql
  ShowSQL: true
  DataSource: test:test@tcp(127.0.0.1:3306)/test?charset=utf8mb4&parseTime=true&loc=Asia%2FShanghai

RedisDb:
  Host: 127.0.0.1:6379
  Type: node
  Pass: test
  DB: 0
  PoolSize: 500
  BlockTimeout: 60s

#AccountRpc:
#  Conf:
#    NonBlock: true
#    #    Target: k8s://dex-dev/rpc-svc:80
#    Target: 127.0.0.1:3060
#    Timeout: 1000
#  Token: test

Tg:
  Token: 66666:xxxxxx
  ChatId: "-123456"
  TurnOn: true

Job:
  LivenessSleep: 10s

K8s:
  Config: "/Users/root/.kube/config"

LivenessProbe:
  LoopSleep: 10s
  Platform: "xx"
  Namespace: "dex-dev"
  NormalStatus:
    running: true
    completed: true
    succeeded: true

  Ignore:
    - alert
    - csi
    - uk8s
    - kube
    - cloud
    - cni
    - core
    - metrics



```
