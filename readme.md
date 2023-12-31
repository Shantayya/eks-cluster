#EKS-CLUSTER
```
1. install eksctl on machine and set the eksctl binary path
https://eksctl.io/installation/

2. Step 1: Create your Amazon EKS cluster and nodes
command: eksctl create cluster --name my-cluster --region region-code

you can enable cloudwatch logging with 'eksctl utils update-cluster-logging --enable-types={SPECIFY-YOUR-LOG-TYPES-HERE (e.g. all)} --region=ap-south-1 --cluster=my-cluster'

eksctl created a kubectl config file in ~/.kube or added the new cluster's configuration within an existing config file in ~/.kube on your computer.

After cluster creation is complete, view the AWS CloudFormation stack named eksctl-my-cluster-cluster in the AWS CloudFormation console at https://console.aws.amazon.com/cloudformation to see all of the resources that were created.

2. Step 2: View Kubernetes resources
command: kubectl get nodes -o wide
         kubectl get pods -A -o wide

3. Step 3: Delete your cluster and nodes
eksctl delete cluster --name my-cluster --region region-code

```