Deploy a high-availability new application using AWS CloudFormation infrastructure.

## Architecture Diagram

![Diagram](udagram-infrastructure-diagram.png)
 
### File Structure

1. `create.sh` 
    * use ssh key to deploy server into Public Subnets,  helps with troubleshooting.

2. `network-infrastructure.yml` `network-parameters.json`
    * contains network resources to be deployed
    * includes VPC, two pairs of public and private subnets, Internet Gateway, NAT Gateways and Routing Tables for public and private subnets with associations

3. `server-infrastructure.yml` `server-parameters.json`
    * contains app resources to be deployed
    * includes Application services. In particular, Load Balancer, web servers and corresponding autoscaling, target and security groups.

4. `update.sh`
    * ssh updates

- Bastion hosts _(Optional)_. EC2 instances for troubleshooting of application web servers.

## Instructions




### Output
LoadBalances DNS Url **[Udagram](http://serve-WebAp-161GK7Q8AC2BX-657455822.us-east-1.elb.amazonaws.com)**.

