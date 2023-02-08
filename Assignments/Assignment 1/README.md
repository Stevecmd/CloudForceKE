**<em> Assignment: :point_right: Creating a cloud formation template. :smirk: </em>**

This AWS CloudFormation template creates and configures the following resources in Amazon Web Services (AWS):

---

> 1. A virtual private cloud (VPC) network with a CIDR block of 10.0.0.0/16, with enabled DNS support and hostnames.
<br/>

> 2. Two subnets within the VPC, one public (10.0.2.0/24) and one private (10.0.1.0/24), with public IPs only assigned to instances in the public subnet.
<br/> 

> 3. Two security groups, one for web servers and another for instances, both within the VPC network. The web server security group allows HTTP and SSH access from any IP, while the instance security group only allows SSH access.
<br/>

> 4. An Amazon EC2 auto-scaling launch configuration, with t2.micro instances and a custom user data script that installs and starts Apache Web Server on the instances.
<br/>

> 5. An auto-scaling group of 10 instances, all in the private subnet.
<br/>

> 6. An Amazon Elastic Load Balancer, in the public subnet, with the web server security group attached.
<br/>

> 7. A load balancer listener for incoming HTTP traffic on port 80.
<br/>

> 8. A target group for the instances in the auto-scaling group, with a protocol of HTTP and a port of 80.
<br/>

> 9. An attachment of the target group to the load balancer.
<br/>

>> Upon deployment, this CloudFormation template creates a fully functioning infrastructure, with a load-balanced, auto-scaling group of web servers.

<br/>