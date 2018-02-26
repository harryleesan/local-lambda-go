## Introduction
This project is a demonstration on how to use **AWS SAM local** to simulate a
local **AWS API Gateway** pointing to a local **lambda function** (using **Go** as runtime)
for local development.

## Usage

1. Compile the `main.go` into a binary

  ```bash
  GOOS=linux go build -o main
  ```

2. Start the **SAM Local** server

  ```bash
  sam local start-api
  ```

3. Access the API (`curl` needs to be installed)

  ```bash
  curl -X POST -d world http://localhost:3000/products/test
  ```

  You should see `Hello world%` being returned.
