# Terratest Implementation README

## Introduction

This repository demonstrates the usage of Terratest for testing Terraform configurations, specifically for Azure resources. Terratest is a Go library that makes it easier to write automated tests for your infrastructure code.

## Repository Structure

The repository has the following structure:

- **main.tf**: This file in the root folder contains the Terraform configuration for creating Azure resources.

- **/test/main_test.go**: This folder contains the Terratest Go test file that will test the infrastructure defined in `main.tf`.

## Prerequisites

Before running Terratest, ensure you have the following prerequisites installed and configured:

1. **Terraform**: Install Terraform by following the instructions on the [official Terraform website](https://www.terraform.io/downloads.html).

2. **Go**: Install Go by following the instructions on the [official Go website](https://golang.org/doc/install).

3. **Azure CLI**: Install the Azure CLI by following the instructions on the [official Azure CLI website](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli).


## Azure Login

Before running the Terratest, ensure you are logged in to Azure using the service principal created earlier. Use the following steps:

```bash
# Log in to Azure using the service principal credentials or any other method
az login --service-principal --username <app-id> --password <password> --tenant <tenant-id>
```

## Running Terratest
To run the Terratest, follow these steps:

1. Clone the repository:
```bash
git clone https://github.com/SaiAnilKumarDeyyala/Terratest-Demo.git
cd Terratest-Demo/test
```
2. Navigate to the test folder:
```bash
cd test
```
3. Initialize Go modules and tidy:
```bash
go mod init test
go mod tidy
```

### Run Tests
4. To run the tests, execute the following commands from the test folder:
```bash
cd test
go test -v -timeout 30m
```

Refer to the Terratest documentation for more information on writing and running tests.