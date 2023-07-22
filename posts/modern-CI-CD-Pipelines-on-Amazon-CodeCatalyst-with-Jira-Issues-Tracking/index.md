---
title: "Modern CI/CD Pipelines on Amazon CodeCatalyst with Jira Issues Tracking"
description: "How To Build a modern CI/CD Pipeline in a few clicks on Amazon CodeCatalyst and ignite its power of extensibility by leveraging Atlassian's Jira Issues Tracking"
tags:
  - CI-CD
  - codecatalyst
  - jira
  - pipelines
authorGithubAlias: kevshakes
authorName: Kevin Tuei
date: 2023-07-21
---
In the current day and age, teamwork and collaboration is becoming increasingly important as technical teams become highly specialized. This is further evidenced by the unprecedented growth and embrace of agile teams, project management and program management. Dev(Sec)Ops has become the order of the day for development and operation teams to easily work together and break down silos.  
However, building applications in an effective and efficient way requires native CI/CD tools that support these methodologies and are able to extend their functionality to specialized third-party tools that handle issue management. 

This article takes you on an exiciting journey on how to leverage Amazon CodeCatalyst from AWS and Jira from Atlassian to build a Modern CI/CD pipeline with Issue Tracking. 

## Getting started

By the end, we will have:

* Installed and configured a Jira Software Extension on an Amazon CodeCatalyst Project
* Update an Issue on a CodeCatalyst project and view the status in Jira Issues 

Although this is not covered in this article, once you have Amazon CodeCatalyst set up with Jira Issues you will also be able to: 
* Update Jira issues with CodeCatalyst pull requests
* View status and workflow runs of linked CodeCatalyst pull requests in Jira issues

## Prerequisites
As a prerequisite, we will need:

* Basic knowledge of navigating between AWS Services
* Active AWS Account
* Free AWS Builder ID
* Free Amazon CodeCatalyst Account
* Active Jira Site (Note: CodeCatalyst is only compatible with Jira Software Cloud.)

Let’s get rolling!

## Modern CI/CD Architecture on Amazon CodeCatalyst

The following architecture provides an overview of all the AWS resources and services that are used in creating a turnkey morern CI/CD pipeline on Amazon CodeCatalyst

![Overview of the Amzon CodeCatalyst CI/CD Architecture](images/architecture.jpg)


### Step 1: Log in to Amazon CodeCatalyst using your AWS Builder ID

You create your AWS Builder ID when you sign up for one of the AWS tools and services that use it. Amazon CodeCatalyst is one of those tools.

`Do remember that having an AWS Account does not necessarilty mean that you already have an AWS Builder ID.` 

Navigate to the Amazon CodeCatalyst Log in Page [Amazon CodeCatalyst Log In Page ](https://codecatalyst.aws/login) 

Amazon CodeCatalyst will automatically Navigate you to the AWS BuilderID Sign Up Page as shown :
![AWS Builder ID Sign Up Page](images/aws_builderid_signup.png)

You will provide your email, click next and a new page will appear where you will be required to provide your name (This is the name that will appear to other users).

After providing your name, you will go through an email verification and password set up process and you will hav your AWS Builder ID created. 

`The AWS Builder ID you just created is what you will use to log in to Amazon CodeCatalyst.`

### Step 2: Create and Configure a CodeCatalyst Space and Project from a Blueprint

* Quick Primer on Spaces, Projects and Blueprints

Consider a CodeCatalyst Space as a logical grouping on CodeCatalyst that can be used to represent a Company if it is small. Several Spaces can represent departments or groups in a large organization.


 `From experience mine my space initialized without a tier and had to contact AWS Support to assist me to resolve this. Same case happened to a fellow builder. So make sure you check your current tier after you link it with your AWS Account and verify your space on the AWS Management Console` 

A CodeCatalyst Project as a collaborative effort in CodeCatalyst that supports development teams and tasks with shared continuous integration/continuous delivery (CI/CD) workflows and repositories.

You can initialize projects using your own code from a CodeCommit, GitHub or Bitbucket Repository. The AWS team continuously develop and update CodeCatalyst Blueprints that synthesize projects and generate projects for you using the base configuration specified by the blueprint.

 `For this particular tutorial you will use a CodeCatalyst Blueprint to create a React Web Application Project which you can customize further.` 

Phew, that was quite a primer. Now that you understand what a Space, Project and a Blueprint is on CodeCatalyst let's proceed and create them. 

After you have successfully logged in to Amazon Codetalyst from Step 1, CodeCatalyst will take you on an Onboarding journey consisting of the following:

* Create your CodeCatalyst Alias which will be part of your profile on all of CodeCatalyst and used to mention you when collaborating on projects for example on a Kanban Board. 

`Your CodeCatalyst alias needs to be unique, does not allow spaces and CANNOT be changed after creating them.`

CodeCatalyst Onboarding - Create your Alias Page :
![Create your CodeCatalyst Alias Page](images/CodeCatalyst_Onboarding1.png)

* After creating your alias, you need to create the space where your projects will live in. 

`Spaces can be used to store and manage projects and are free to use on AWS. However it is important to note that Spaces are initialized on the Free Tier`

CodeCatalyst Onboarding - Create your Space Page :
![Create your CodeCatalyst Space Page](images/CodeCatalyst_Onboarding2.png)


* Once your Space is ready, you need to link an AWS Account to handle billing and deployments. 

`You need to only enter an AWS Account ID you can access and has the appropriate permissions to access CodeCatalyst otherwise you will be unable to verify on the AWS Console.`

In case you don't have an AWS Account you can create an [Free Tier AWS Account here:](https://aws.amazon.com/free/) 

CodeCatalyst Onboarding - Link your AWS Account to CodeCatalyst Page :
![Link your AWS Account with CodeCatalyst Page](images/CodeCatalyst_Onboarding3.png)

### Step 3: Set up and test your CodeCatalyst CI/CD Pipeline


### Step 4: Connect your Jira sites to your CodeCatalyst space 

The next step to connect your Jira Sites is to install Jira Software extension to your CodeCatalyst space.


### Step 5: Link your Jira issue to a CodeCatalyst Pull Request

Check this AWS Codumentation Article for more information on [working with pull requests in Amazon CodeCatalyst](https://docs.aws.amazon.com/codecatalyst/latest/userguide/source-pull-requests.html)

### Step 6: Link your Jira project to your CodeCatalyst project

### Step 7: Confirm the CodeCatalyst Workflow Events in your Jira Issue

## Clean Up the Resources

Now that you’ve finished building a modern CI/CD pipeline on Amazon CodeCatalyst, you can delete all resources from Amazon CodeCatalyst and your AWS Account.


## Conclusion

Congratulations! You have built a Modern CI/CD Pipeline Complete with Jira Issue Tracking on Amazon CodeCatalyst. You can explore further on how you can integrate your own code from CodeCommit or other source Providers such as GitHub and BitBucket.

If you want to learn more about Amazon CodeCatalyst, you can check out the following blog posts:

* [AWS re:Invent 2022 - Introducing Amazon CodeCatalyst](https://www.youtube.com/watch?v=mKdGehrUYFI)
* [AWS Developer Innovation Day | AWS On Air ft. Team up without the friction with Amazon CodeCatalyst ](https://www.youtube.com/watch?v=fTK_7l8md1M)
* [Amazon CodeCatalyst User Guide - AWS Documentation ](https://docs.aws.amazon.com/codecatalyst/latest/userguide/welcome.html)
* [Amazon CodeCatalyst Workshop](https://catalog.us-east-1.prod.workshops.aws/workshops/23fa5676-2943-415b-98b9-125f5e86912d/en-US)


If you found this guide helpful, we appreciate your feedback and in case you end up facing any challenges, we are here for you, please send it our way