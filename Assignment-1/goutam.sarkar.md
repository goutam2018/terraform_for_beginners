terraform {
  required_providers {
    aws = {
      source = "hashicorp/aws"
      version = "5.42.0"
    }
  }
}

provider "aws" {
  region     = "ap-south-1"
  access_key = "*********"
  secret_key = "**************"
}

resource "aws_instance" "ec2-1" {
  ami           = "ami-007020fd9c84e18c7"
  instance_type = "t2.micro"

  tags = {
    Name = "ec2_instance"
  }

