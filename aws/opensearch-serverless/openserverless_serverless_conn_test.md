# Golang AWS OpenSearch Index Management

This Golang code provides an example of how to connect to AWS OpenSearch (formerly known as Amazon Elasticsearch) using IAM-based role authentication. It demonstrates how to create and delete an index with non-default settings.

## Prerequisites

Before running the code, ensure you have the following:

1. An AWS account with appropriate IAM roles and permissions to access AWS OpenSearch.
2. Golang installed on your system.

## Setup

1. Install required dependencies:

   ```bash
   go get github.com/aws/aws-sdk-go-v2/config
   go get github.com/opensearch-project/opensearch-go/v2
   ```

2. Set environment variables:

   Make sure to set the following environment variables before running the code:

   - `AWS_OPENSEARCH_ENDPOINT`: The endpoint URL of your AWS OpenSearch cluster.
   - `AWS_REGION`: The AWS region where your AWS OpenSearch cluster is located.

## Code Description

The code demonstrates the following steps:

1. Initialize AWS configuration and create a request signer using the IAM role.
2. Create an AWS OpenSearch client with the request signer.
3. Define the index mapping with non-default settings.
4. Create an index in AWS OpenSearch with the specified mapping.
5. Delete the previously created index.

## Usage

1. Make sure the environment variables ('AWS_OPENSEARCH_ENDPOINT` and `AWS_REGION`) are set correctly.
2. Run the Golang code using:

   ```bash
   go run main.go
   ```
Please note that this code is for demonstration purposes only. In a production environment, you should handle errors more gracefully and ensure appropriate error logging and handling. Also, make sure to handle the AWS credentials securely and avoid hardcoding them in the code.

For more information about AWS OpenSearch and IAM-based authentication, refer to the official AWS OpenSearch documentation and AWS SDK for Go documentation.

**Important**: Before running the code, ensure you understand the implications of creating and deleting indexes in your AWS OpenSearch cluster. These operations can have a significant impact on your data and should be executed with caution.
