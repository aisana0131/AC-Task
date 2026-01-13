## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | ~> 1.14.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | ~> 6.28.0 |
| <a name="requirement_okta"></a> [okta](#requirement\_okta) | ~> 4.10.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | ~> 6.28.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_final_ec2"></a> [final\_ec2](#module\_final\_ec2) | ./modules/ec2 | n/a |
| <a name="module_okta_users"></a> [okta\_users](#module\_okta\_users) | ./modules/okta-users | n/a |

## Resources

| Name | Type |
|------|------|
| [aws_secretsmanager_secret_version.okta_private_key](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/secretsmanager_secret_version) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_ami_id"></a> [ami\_id](#input\_ami\_id) | n/a | `string` | n/a | yes |
| <a name="input_default_groups"></a> [default\_groups](#input\_default\_groups) | n/a | `list(string)` | `[]` | no |
| <a name="input_environment"></a> [environment](#input\_environment) | n/a | `string` | n/a | yes |
| <a name="input_instance_type"></a> [instance\_type](#input\_instance\_type) | n/a | `string` | `"t2.micro"` | no |
| <a name="input_name"></a> [name](#input\_name) | n/a | `string` | n/a | yes |
| <a name="input_okta_base_url"></a> [okta\_base\_url](#input\_okta\_base\_url) | n/a | `string` | n/a | yes |
| <a name="input_okta_client_id"></a> [okta\_client\_id](#input\_okta\_client\_id) | n/a | `string` | n/a | yes |
| <a name="input_okta_org_name"></a> [okta\_org\_name](#input\_okta\_org\_name) | n/a | `string` | n/a | yes |
| <a name="input_okta_private_key_id"></a> [okta\_private\_key\_id](#input\_okta\_private\_key\_id) | n/a | `string` | n/a | yes |
| <a name="input_okta_scopes"></a> [okta\_scopes](#input\_okta\_scopes) | n/a | `list(string)` | n/a | yes |
| <a name="input_okta_users"></a> [okta\_users](#input\_okta\_users) | n/a | <pre>map(object({<br/>    first_name = string<br/>    last_name  = string<br/>    email      = string<br/>    groups     = list(string)<br/>  }))</pre> | n/a | yes |
| <a name="input_region"></a> [region](#input\_region) | n/a | `string` | n/a | yes |

## Outputs

No outputs.

## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_instance.final_ec2](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/instance) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_ami_id"></a> [ami\_id](#input\_ami\_id) | n/a | `string` | n/a | yes |
| <a name="input_environment"></a> [environment](#input\_environment) | n/a | `string` | n/a | yes |
| <a name="input_instance_type"></a> [instance\_type](#input\_instance\_type) | n/a | `string` | `"t2.micro"` | no |
| <a name="input_name"></a> [name](#input\_name) | n/a | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_instance_id"></a> [instance\_id](#output\_instance\_id) | n/a |
| <a name="output_public_ip"></a> [public\_ip](#output\_public\_ip) | n/a |


## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_okta"></a> [okta](#requirement\_okta) | ~> 4.10.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_okta"></a> [okta](#provider\_okta) | ~> 4.10.0 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [okta_user.users](https://registry.terraform.io/providers/okta/okta/latest/docs/resources/user) | resource |
| [okta_user_group_memberships.memberships](https://registry.terraform.io/providers/okta/okta/latest/docs/resources/user_group_memberships) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_okta_users"></a> [okta\_users](#input\_okta\_users) | n/a | <pre>map(object({<br/>    first_name = string<br/>    last_name  = string<br/>    email      = string<br/>    groups     = list(string)<br/>  }))</pre> | n/a | yes |

## Outputs

No outputs.


