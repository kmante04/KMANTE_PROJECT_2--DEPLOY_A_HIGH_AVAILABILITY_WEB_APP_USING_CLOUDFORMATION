# KMante--project-2--(Deploy-a-high availability web app using"CloudFormation")
This project about Deploy a high-availability web app using CloudFormation
http://udagr-webap-cwzhg10i7541-1042794624.us-east-1.elb.amazonaws.com/ this is the link for website 
Project Overview

Project Files

    /cloudformation-stacks:
        network-params.json: Parameters file for network cloudformation stack.
        network.yml: CloudFormation template for creating networking resources for this project.
        servers-params.json: Parameters file for servers cloud formation stack.
        servers.yml: CloudFormation template for creating servers for this project.
    s3-bucket: It contain the main html file of the application and upload status screenshot.
    /scripts: This folder contains script to create, delete and update CloudFormation stack
    /workflow-screenshots: This folder contain screenshots of whole workflow status
    udagram-infrastructure-diagram.png: This shows visual aid to understand the CloudFormation script.

    #Project Setup

    To create networking resources using cloudformation template, run the below command. After exceuting it these are the resources created:

    VPC
    Subnets
    Route Tables
    Routes
    Internet Gateway
    NAT Gateways

$ scripts/create.sh Udagramnetwork-stack network.yml network-parameters.json

   To create servers resources using cloudformation template which pulls source code from S3 bucket automatically while starting, run the below command. After exceuting it these are the resources created:

    Security Groups
    IAM Role, Policy, Instance Profile
    Launch configuration
    Auto Scaling Group
    Load Balancer
    Target Group

$ scripts/create.sh Udagramserver-stack server.yml server-parameter.json

Once the above steps are complete, you can find the URL of application in the outputs section of Udagramserver-stack CloudFormarion stack. Here is what it looks like.