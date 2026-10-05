# Task 3 - Infrastructure as Code with Terraform

## Objective

Provision and manage a local Docker Nginx container using Terraform.

## Tools Used

* Terraform
* Docker Desktop
* Git & GitHub
* Nginx Docker Image

## Project Structure

```text
terraform-docker-task/
├── main.tf
├── README.md
└── .gitignore
```

## Terraform Configuration

The Terraform configuration uses the Docker provider to:

1. Pull the `nginx:latest` Docker image.
2. Create an Nginx container named `terraform-nginx`.
3. Map Docker port `80` to local port `8081`.

## Commands Executed

Initialize Terraform:

```bash
terraform init
```

Check the execution plan:

```bash
terraform plan
```

Create the infrastructure:

```bash
terraform apply
```

Verify Terraform state:

```bash
terraform state list
terraform state show docker_container.nginx
```

Verify the Docker container:

```bash
docker ps
```

The application was accessible locally at:

```text
http://localhost:8081
```

Destroy the infrastructure:

```bash
terraform destroy
```

## Result

The Nginx Docker container was successfully provisioned and managed using Terraform.

Terraform state was verified using `terraform state` commands, and the infrastructure was successfully destroyed using `terraform destroy
