# module-ixload-app/aws

## Description
Terraform module for IxLoad application deployment on Amazon Web Services

## Deployment
This module creates a single instance having a single network interface.

## Usage
```tf
module "App" {
	source  = "git::https://github.com/Keysight/terraform-aws-module-ixload-app.git"
	Eth0SecurityGroupId = aws_security_group.PublicSecurityGroup.id
	Eth0SubnetId = aws_subnet.PublicSubnet.id
	SshKeyName = aws_key_pair.SshKey.key_name
}
```
