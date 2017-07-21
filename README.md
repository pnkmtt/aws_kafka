# aws-kafka
TerraForm Scripts for AWS and Kafka

To use this:

You must set these environmental variables to use this
$ export AWS_ACCESS_KEY_ID="anaccesskey"
$ export AWS_SECRET_ACCESS_KEY="asecretkey"
$ export AWS_DEFAULT_REGION="us-east-1"

You will be asked for an existing key in each region: set or know before you run apply


Variables are driven from within the production environment: aws_kafka/produciton/services/kafka-cluster/vars.tf or from commandline

key_name = ssh key that has already been uploaded to the AWS region that this is targeting
cluster_name - unique name for the cluster - default = "kafka-01"
broker_instance_type - broker instance type - default = "t2.micro"
zookeeper_instance_type - zookeeper instance type-  default = "t2.micro"
number_of_zookeepers - number of zookeeper nodes to build default = 3
number_of_brokers - number of brokers to build default = 6

TODO:

- Add ansible for Kafka build
- put in ELB in front of Kafka nodes
- put in autoscaling for broker nodes
