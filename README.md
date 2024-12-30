## Assignment 2.13: Serverless Architecture Part 1

Make a comparison between Serverless Framework and Terraform as tools for IaC by answering:

**Q1. What type of infrastructure and application deployments are each tool best suited for?**
<br>The Serverless Framework is designed specifically for building and deploying serverless applications such as AWS Lambda, Azure Functions and Google Cloud Functions while Terraform, on the other hand, is a general-purpose infrastructure as code (IaC) tool that supports a wide range of cloud services.

**Q2. How do their primary objectives differ?**
<br>The Serverless Framework is designed specifically for building and deploying serverless applications such as AWS Lambda, Azure Functions and Google Cloud Functions while Terraform, on the other hand, is a general-purpose infrastructure as code (IaC) tool that supports a wide range of cloud services.

**Q3. How do they differ in terms of learning curve and ease of use for developers or DevOps teams?**
<br>Serverless Framework uses a straightforward configuration file (serverless.yml) that makes defining functions, events, and resources simple and intuitive. This YAML-based configuration is more readable and easier to manage for serverless architectures, reducing the learning curve for new developers.
In contrast, Terraform configurations, written in HashiCorp Configuration Language (HCL), can become complex, especially when dealing with intricate dependencies and large-scale infrastructure. While HCL is powerful, it requires a deeper understanding and can be less accessible to developers who are primarily focused on serverless applications.

**Q4. What are the differences in how each tool handles state tracking and deployment changes?**
<br>Terraform uses a state management system(tf state file) that allows you to keep track of the current state of your infrastructure. This makes it easier to manage changes and rollbacks, as Terraform can detect and apply only the necessary changes to your infrastructure.
Serverless Framework Compose uses AWS S3 to store the state of services and AWS SSM (Systems Manager) to track the location of the state storage.

**Q5. In what scenarios would you recommend using Serverless Framework over Terraform, and vice versa?**
<br>Use Terraform to handle infrastructure provisioning across multiple cloud and SaaS providers and manage the entire lifecycle of your infrastructure. It offers a wide range of integrations and we can use it to manage any type of infrastructure, not just serverless.
On the other hand, If solely focused on serverless application development, the Serverless Framework provides an excellent set of tools to manage the deployment and management of the serverless applications. It offers a streamlined workflow and a great developer experience, with support for multiple serverless providers.

**Q6. Are there scenarios where using both together might be beneficial?**
<br>Create all the infrastructure related things(Queues, Topics, Databases, Tables, VPCs, IAM Roles etc.) with Terraform.
Create functions and hook up events (like API Gateway, s3, DynamoDB Streams, SQS, SNS etc) using the Serverless Framework.
