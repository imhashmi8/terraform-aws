### Terraform Settings Scetion

terraform {
    required_providers {
      aws = {
        source = "hashicorp/aws"
      }
    }
  
}

### Provider Section

provider "aws" {
    profile = "default"
    region = "eu-west-1"
  
}

### Resource Section

resource "aws_instance" "ec2-hashmi" {
    ami = "ami-024e06bf5b7eab87b"
    instance_type = "t2.micro"
  
}