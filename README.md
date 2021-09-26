# 10-monitoring-03-grafana  

![image](https://user-images.githubusercontent.com/67621467/134773008-621ceb18-429b-4851-9e4a-afb850f913c0.png)


![image](https://user-images.githubusercontent.com/67621467/134796840-6f90ff85-c283-4ee9-a01b-69b6ae96fb10.png)

avg(node_load1{instance="$node",job="$job"}) /  count(count(node_cpu_seconds_total{instance="$node",job="$job"}) by (cpu)) * 100
avg(node_load5{instance="$node",job="$job"}) /  count(count(node_cpu_seconds_total{instance="$node",job="$job"}) by (cpu)) * 100
avg(node_load15{instance="$node",job="$job"}) /  count(count(node_cpu_seconds_total{instance="$node",job="$job"}) by (cpu)) * 100

avg by (instance) (rate(node_cpu_seconds_total{job="$job",mode="idle"}[1m])) * 100

node_memory_MemFree_bytes{instance="$node",job="$job"}

(node_filesystem_avail_bytes{instance="$node",job="$job",mountpoint="/",fstype!="rootfs"} * 100)
да, количество места на файловой системе у меня 0
