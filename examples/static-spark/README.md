<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

No requirements.

## Providers

No provider.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| bucket\_name\_for\_logs | S3 bucket name for cluster logs. | `string` | n/a | yes |
| bucket\_name\_for\_root\_directory | S3 bucket name for storing root directory. | `string` | n/a | yes |
| cluster\_name | Name for the EMR cluster to be created | `string` | n/a | yes |
| key\_pair\_name | Name of the Key Pair that will be attached to the EC2 instances | `string` | n/a | yes |
| subnet\_id | ID of the subnet where the EMR cluster will be created | `string` | n/a | yes |
| vpc\_id | VPC ID of the network | `string` | n/a | yes |
| additional\_tags | Additional tags to be attached to the resources created | `map(string)` | `{}` | no |
| core\_instance\_group\_name | Name for the core instance group | `string` | `"tamr-test-spark-core-instance-group"` | no |
| emr\_additional\_core\_sg\_name | Name for the EMR additional core security group | `string` | `"tamr-test-spark-sg-core-additional"` | no |
| emr\_additional\_master\_sg\_name | Name for the EMR additional master security group | `string` | `"tamr-test-spark-sg-master-additional"` | no |
| emr\_config\_file\_path | Path to the EMR JSON configuration file. Please include the file name as well. | `string` | `"../../modules/aws-emr-emrfs/config.json"` | no |
| emr\_ec2\_iam\_policy\_name | Name for the IAM policy attached to the EMR service role | `string` | `"tamr-test-spark-policy-ec2"` | no |
| emr\_ec2\_instance\_profile\_name | Name for the new instance profile for the EMR EC2 instances | `string` | `"tamr-test-spark-instance-profile"` | no |
| emr\_ec2\_role\_name | Name for the new iam role for the EMR EC2 instances | `string` | `"tamr-test-spark-ec2-role"` | no |
| emr\_managed\_core\_sg\_name | Name for the EMR managed core security group | `string` | `"tamr-test-spark-sg-core"` | no |
| emr\_managed\_master\_sg\_name | Name for the EMR managed master security group | `string` | `"tamr-test-spark-sg-master"` | no |
| emr\_service\_access\_sg\_name | Name for the EMR service access security group | `string` | `"tamr-test-spark-sg-service-access"` | no |
| emr\_service\_iam\_policy\_name | Name for the IAM policy attached to the EMR Service role | `string` | `"tamr-test-spark-policy-service"` | no |
| emr\_service\_role\_name | Name for the new iam service role for the EMR cluster | `string` | `"tamr-test-spark-service-role"` | no |
| emrfs\_metadata\_table\_name | Name of the Dynamodb table (already created or to be used for EMR consistent view) | `string` | `"tamr-test-spark-emrfs-metadata"` | no |
| master\_instance\_group\_name | Name for the master instance group | `string` | `"tamr-test-spark-master-instance-group"` | no |
| release\_label | The release label for the Amazon EMR release. | `string` | `"emr-5.29.0"` | no |
| tamr\_cidrs | List of CIDRs for Tamr | `list(string)` | `[]` | no |
| tamr\_sgs | Security Group for the Tamr Instance | `list(string)` | `[]` | no |

## Outputs

No output.

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->