<<<<<<< HEAD
# cluster
=======
# kubernetes-cluster-files
these are the terraform files to create a kubernetes cluster with one master node i.e, management node and 2 worker nodes 
clone the repo and apply using below commands in the terminal
  terraform init
  terraform validate
  terraform plan
  terraform apply -auto-approve

after it is sucessfully applied and create a infra in your aws cloud 
get the ip address of the management node and ssh into the instance 
inside the instance configure your aws account where the cluster is created using access key and secret key using below commands
  aws configure

after configuring the aws account the .kube/config must be updated with the cluster context, for that use the below command

aws eks update-kubeconfig --region <cluster_region> --name <cluster-name>  # use sudo if permission denied 
by this steps the cluster will be accessible
>>>>>>> c63d6cb (creating to the cluster)
