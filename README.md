# VPC Module

AWS VPC module to create a basic VPCs with 1 public subnet per AZ in AWS.

## How To Use

### Variables

  * `name_prefix`: String (optional, default: `tf-`)
  * `cidr_block`: String (optional, default: `172.31.0.0/16`)

### Outputs

  * `vpc_id`: String 
  * `default_security_group`: String
  * `subnets`: Map[List]: List of subnet ids per tier (_public_)
  * `cidr_blocks`: Map[List]: List of CIDR blocks per tier (_vpc_, _public_)

### Example
```hcl
module "vpc" {
  source = "github.com/gbergere/tf-vpc-module"
}
```

## Used by

  * [tf-consul-module](https://github.com/gbergere/tf-consul-module)
