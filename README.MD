# Deploy a High-Availability Web App using CloudFormation
This project is for the Udacity Devops Nanodegree course.

Objective was to deploy an Infrastructure using code on CloudFormation to run a HA webapp.


## About the project

In this project, I've deployed web servers for a highly available web app using CloudFormation. I have written the code that creates and deploys the infrastructure and application for an Instagram-like app from the ground up. I have begun with deploying the networking components, followed by servers, security roles and software. The procedure I have followed here will become part of my portfolio of cloud projects. 


### Prerequisites:

I have created an AWS user <b>rahul-superuser</b> with Administrator policy. 

I have configured aws-cli for this user.

I have created a S3 bucket - udacity-pal-devops and uploaded udacity-starter-website.zip in that. 


### Steps:

Execute the following commands:
1) Create infra stack:
```
./create.sh udacity-pal-devops-2-inf-stack infra.yml infra-params.json
```

```
Output:
{
    "StackId": "arn:aws:cloudformation:us-west-2:516964037190:stack/udacity-pal-devops-2-inf-stack/92cb0b50-9c6d-11ea-806e-02ca0801967a"
}
```

2) Create server stack:
```
./create.sh udacity-pal-devops-2-serv-stack servers.yml servers-params.json
```

```
Output:
{
    "StackId": "arn:aws:cloudformation:us-west-2:516964037190:stack/udacity-pal-devops-2-serv-stack/233fc9a0-9c6e-11ea-8dbd-0284c9f60df0"
}
```
<br>

![Alt text](/screenshots/stack.PNG "stack created")

<br>

To update a stack use: 
```
modify.sh
```

To delete a stack use: 
```
delete.sh
```


### Access WebApp

Webapp is deployed at:

[Webapp link](http://udaci-webap-ca1kyukqelg6-586824.us-west-2.elb.amazonaws.com/)

