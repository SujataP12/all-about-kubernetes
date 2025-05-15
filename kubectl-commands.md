### 📦 Cluster Management

1. `kubectl cluster-info`
   Display endpoint information about the master and services in the cluster

2. `kubectl version`
   Display the Kubernetes version running on the client and server

3. `kubectl config view`
   Get the configuration of the cluster

4. `kubectl api-resources`
   List the API resources that are available

5. `kubectl api-versions`
   List the API versions that are available

6. `kubectl get all --all-namespaces`
   List everything

---

### 🔄 Daemonsets (`ds`)

7. `kubectl get daemonset`
   List one or more daemonsets

8. `kubectl edit daemonset <daemonset_name>`
   Edit and update a daemonset

9. `kubectl delete daemonset <daemonset_name>`
   Delete a daemonset

10. `kubectl create daemonset <daemonset_name>`
    Create a new daemonset

11. `kubectl rollout daemonset`
    Manage the rollout of a daemonset

12. `kubectl describe ds <daemonset_name> -n <namespace_name>`
    Display detailed state of daemonsets in a namespace

---

### 🚀 Deployments (`deploy`)

13. `kubectl get deployment`
    List deployments

14. `kubectl describe deployment <deployment_name>`
    Show deployment state

15. `kubectl edit deployment <deployment_name>`
    Edit deployment

16. `kubectl create deployment <deployment_name>`
    Create deployment

17. `kubectl delete deployment <deployment_name>`
    Delete deployment

18. `kubectl rollout status deployment <deployment_name>`
    Show rollout status

---

### 🗓️ Events (`ev`)

19. `kubectl get events`
    List recent events

20. `kubectl get events --field-selector type=Warning`
    Show only Warnings

21. `kubectl get events --field-selector involvedObject.kind!=Pod`
    Exclude Pod events

22. `kubectl get events --field-selector involvedObject.kind=Node,involvedObject.name=<node_name>`
    Events for a node

23. `kubectl get events --field-selector type!=Normal`
    Filter out Normal events

---

### 📜 Logs

24. `kubectl logs <pod_name>`
    Print logs

25. `kubectl logs --since=1h <pod_name>`
    Logs from last hour

26. `kubectl logs --tail=20 <pod_name>`
    Last 20 lines

27. `kubectl logs -f <service_name> [-c <container>]`
    Logs from service/container

28. `kubectl logs -f <pod_name>`
    Follow logs

29. `kubectl logs -c <container_name> <pod_name>`
    Logs from specific container

30. `kubectl logs <pod_name> pod.log`
    Save logs to file

31. `kubectl logs --previous <pod_name>`
    View logs from failed pod

32. `kubetail <pod_prefix>`
    Logs for all pods with prefix (via Kubetail)

33. `kubetail <pod_prefix> -s 5m`
    Include recent 5 minutes

---

### 📄 Manifest Files

34. `kubectl apply -f manifest_file.yaml`
    Apply configuration

35. `kubectl create -f manifest_file.yaml`
    Create object

36. `kubectl create -f ./dir`
    Create from directory

37. `kubectl create -f 'url'`
    Create from URL

38. `kubectl delete -f manifest_file.yaml`
    Delete object

---

### 🧱 Namespaces (`ns`)

39. `kubectl create namespace <namespace_name>`
    Create namespace

40. `kubectl get namespace <namespace_name>`
    List namespace

41. `kubectl describe namespace <namespace_name>`
    Describe namespace

42. `kubectl delete namespace <namespace_name>`
    Delete namespace

43. `kubectl edit namespace <namespace_name>`
    Edit namespace

44. `kubectl top namespace <namespace_name>`
    Resource usage

---

### 🖥️ Nodes (`no`)

45. `kubectl taint node <node_name>`
    Update taints

46. `kubectl get node`
    List nodes

47. `kubectl delete node <node_name>`
    Delete node

48. `kubectl top node`
    Node resource usage

49. `kubectl describe nodes | grep Allocated -A 5`
    Allocation per node

50. `kubectl get pods -o wide | grep <node_name>`
    Pods on node

51. `kubectl annotate node <node_name>`
    Annotate node

52. `kubectl cordon node <node_name>`
    Unschedulable

53. `kubectl uncordon node <node_name>`
    Schedulable

54. `kubectl drain node <node_name>`
    Drain node

55. `kubectl label node`
    Label node

---

### 📦 Pods (`po`)

56. `kubectl get pod`
    List pods

57. `kubectl delete pod <pod_name>`
    Delete pod

58. `kubectl describe pod <pod_name>`
    Describe pod

59. `kubectl create pod <pod_name>`
    Create pod

60. `kubectl exec <pod_name> -c <container_name> <command>`
    Execute command

61. `kubectl exec -it <pod_name> /bin/sh`
    Interactive shell

62. `kubectl top pod`
    Resource usage

63. `kubectl annotate pod <pod_name> <annotation>`
    Annotate pod

64. `kubectl label pod <pod_name>`
    Label pod

---

### 🔁 Replication Controllers (`rc`)

65. `kubectl get rc`
    List replication controllers

66. `kubectl get rc --namespace="<namespace_name>"`
    By namespace

---

### 🔂 ReplicaSets (`rs`)

67. `kubectl get replicasets`
    List ReplicaSets

68. `kubectl describe replicasets <replicaset_name>`
    Describe ReplicaSet

69. `kubectl scale --replicas=[x]`
    Scale ReplicaSet

---

### 🔐 Secrets

70. `kubectl create secret`
    Create secret

71. `kubectl get secrets`
    List secrets

72. `kubectl describe secrets`
    Describe secrets

73. `kubectl delete secret <secret_name>`
    Delete secret

---

### 🌐 Services (`svc`)

74. `kubectl get services`
    List services

75. `kubectl describe services`
    Describe service

76. `kubectl expose deployment [deployment_name]`
    Expose deployment

77. `kubectl edit services`
    Edit service

---

### 👤 Service Accounts (`sa`)

78. `kubectl get serviceaccounts`
    List service accounts

79. `kubectl describe serviceaccounts`
    Describe service accounts

80. `kubectl replace serviceaccount`
    Replace service account

81. `kubectl delete serviceaccount <service_account_name>`
    Delete service account

---

### 🗂️ StatefulSet (`sts`)

82. `kubectl get statefulset`
    List StatefulSets

83. `kubectl delete statefulset/[stateful_set_name] --cascade=false`
    Delete only StatefulSet

---

### ⚙️ Common Options

84. `-o wide`
    Output format

85. `-n [namespace_name]`
    Specify namespace

86. `-f <filename>`
    Use file to create resource

87. `-l`
    Label selector

88. `-h`
    Help for kubectl
