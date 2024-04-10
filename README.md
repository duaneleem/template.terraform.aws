# template.terraform.aws
Terraform AWS template.

Each example are inside the `environments` folder.  Each folder contains example spinning up the required infrastructure.  Before deploying any example, start with `environments/example-vpc` to start with a foundational VPC that contains a private/public subnet.

## Initialization

```sh
terraform init

```

## Troubleshoot Infrastructure

```sh
# Set environment
export TERRAFORM_EXAMPLE_ENV=dev

terraform plan -var-file=".env.${TERRAFORM_EXAMPLE_ENV}.tfvars"

terraform apply -var-file=".env.${TERRAFORM_EXAMPLE_ENV}.tfvars"

terraform show -var-file=".env.${TERRAFORM_EXAMPLE_ENV}.tfvars"

```
