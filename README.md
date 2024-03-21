# Connect to Private EC2 Instance Guide

This guide provides step-by-step instructions for connecting to a private EC2 instance on AWS.

## Overview

This repository contains detailed instructions for connecting to a private EC2 instance on AWS. By following these steps, you'll be able to establish a connection from a public instance to a private instance, set up internet access for the private subnet, and configure security groups for enhanced security.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Setup Instructions](#setup-instructions)
3. [Usage](#usage)
4. [Additional Documentation](#additional-documentation)
5. [Contributing](#contributing)
6. [License](#license)

## Prerequisites

Before you begin, ensure you have:

- An AWS account with sufficient permissions to create and manage EC2 instances, route tables, NAT gateways, and security groups.
- Access to the AWS Management Console.

## Setup Instructions

1. **Create EC2 Instances**:
   - Ensure you have two instances, one public and one private. If not, create them in your AWS account.

2. **Connect to Public Instance**:
   - Connect to the public instance using its public IP address.
   - Check if it has internet access by pinging google.com.

3. **Check Files in Public Subnet**:
   - Verify the files inside the public subnet.

4. **Create Sample File**:
   - Create a sample.txt file with the content: "This is a public subnet file".
   - Verify that the file has been created and saved properly.

5. **Connect to Private Instance from Public Subnet**:
   - As the private instance doesn't have a public IP, connect to it from the public subnet.
   - Generate a key.pem file and copy its content to the private instance.

6. **Set Up SSH Connection**:
   - Connect to the private instance using SSH and the key.pem file.

7. **Ensure Proper Permissions**:
   - Set the correct permissions for the key.pem file.

8. **Copy Files to Private Instance**:
   - Copy the sample.txt file from the public instance to the private instance.

9. **Verify File Transfer**:
   - Check if the copied file is reflecting correctly on the private instance.

10. **Configure Internet Access for Private Subnet**:
    - Create a NAT gateway and attach it to the private route table.
    - Allocate an elastic IP address for the NAT gateway.

11. **Update Route Table**:
    - Attach the NAT gateway to the private route table to provide internet access to the private subnet.

12. **Configure Security Groups**:
    - Create a dedicated security group for the private subnet.
    - Edit the inbound rules to allow connections from the private instance to the internet via the public instance.

## Usage

Follow the provided instructions to connect to a private EC2 instance on AWS and configure internet access and security settings as required.

## Additional Documentation

For more detailed instructions and additional resources, please refer to the [documentation folder](Documentation/) in this repository. The documentation includes PDF files with detailed guides, best practices, and exercises for practicing.

## Contributing

Contributions to this repository are welcome! If you find issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
