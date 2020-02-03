# Project: Reusable Terraform Infrastructure

Projects created as infrastructure building blocks

## Static Website

Terraform module for running a static website hosted on S3 and Cloudfront. Used as a building block in other projects

* Hosts a static site (e.g. a [React](https://reactjs.org/) App) on AWS services to allow effortless and inexpensive scaling
* Includes an [AWS CodePipeline](https://aws.amazon.com/codepipeline/) for CI/CD, automatically building and deploying a specified branch of a GitHub repository when changes are pushed to it

### Repository

* [Terraform Module](https://github.com/Lsquared13/terraform-aws-static-website)

## Lambda CD Pipeline

Terraform module for a CI/CD [AWS CodePipeline](https://aws.amazon.com/codepipeline/) which builds and deploys Lambda functions. Used as a building block in other projects

* Builds a specified source branch and repository and deploys the resulting code to any number of Lambda functions
* Build process is configurable, but uses sane defaults for a [NodeJS](https://nodejs.org/en/) project

### Repositories

* [Terraform Module](https://github.com/Lsquared13/terraform-aws-lambda-cd-pipeline)
* [Lambda Deployment Function](https://github.com/Lsquared13/lambda-deploy-lambda)
* [Default Lambda](https://github.com/Lsquared13/default-lambda)

## OpenVPN Server

Terraform configuration for running an OpenVPN server. Used as part of security infrastructure for main network (all mainn network operators needed to be on the VPN)

* Manages a [OpenVPN Access Server](https://aws.amazon.com/marketplace/pp/OpenVPN-Inc-OpenVPN-Access-Server/B00MI40CAE) from the AWS Marketplace and all associated networking infrastructure
* Contains all relevant configuration in terraform variables, allowing a VPN to be spun up with just a `terraform apply`

### Repository

* [Terraform Configuration](https://github.com/Lsquared13/terraform-aws-openvpn-server)

## Multi Cert Tool

Terraform configuration for creating multiple internal certificates signed by a single private CA

* Modified from a HashiCorp module that creates a single internal certificate
* Allows clients to trust a single private CA to cover multiple internal certificates

### Repository

* [Terraform Module](https://github.com/Lsquared13/terraform-multi-cert-tool)