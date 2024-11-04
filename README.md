# bank-account-manager-terraform
Terraform script for creatining AWS infrastructure


## Initial Setup - Localstack

Configure AWS profile
> aws configure --profile local

Create S3 bucket for Terraform State
> aws s3api create-bucket --profile local --endpoint http://localhost:4566 --bucket terraform-state --region us-east-1

## Prepare Terraform

Obs.: On LocalStack you don´t need to pass access key and secret key. Leave it blank

Init
> terraform -chdir=src init

Plan
> terraform -chdir=src plan

Apply
> terraform -chdir=src apply