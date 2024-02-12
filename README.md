# AWS Continuous Integration Demo

## Set Up GitHub Repository

The first step in our CI journey is to set up a GitHub repository to store our Python application's source code. If you already have a repository, feel free to skip this step. Otherwise, let's create a new repository on GitHub by following these steps:

- Go to github.com and sign in to your account.
- Click on the "+" button in the top-right corner and select "New repository."
- Give your repository a name and an optional description.
- Choose the appropriate visibility option based on your needs.
- Initialize the repository with a README file.
- Click on the "Create repository" button to create your new GitHub repository.

Great! Now that we have our repository set up, we can move on to the next step.

## Create an AWS CodePipeline
In this step, we'll create an AWS CodePipeline to automate the continuous integration process for our Python application. AWS CodePipeline will orchestrate the flow of changes from our GitHub repository to the deployment of our application. Let's go ahead and set it up:

- Go to the AWS Management Console and navigate to the AWS CodePipeline service.
- Click on the "Create pipeline" button.
- Provide a name for your pipeline and click on the "Next" button.
- For the source stage, select "GitHub" as the source provider.
- Connect your GitHub account to AWS CodePipeline and select your repository.
- Choose the branch you want to use for your pipeline.
- In the build stage, select "AWS CodeBuild" as the build provider.
- Create a new CodeBuild project by clicking on the "Create project" button.
- Configure the CodeBuild project with the necessary settings for your Python application, such as the build environment,  build commands, and artifacts.
- Save the CodeBuild project and go back to CodePipeline.
- Continue configuring the pipeline stages, such as deploying your application using AWS Elastic Beanstalk or any other suitable deployment option.
- Review the pipeline configuration and click on the "Create pipeline" button to create your AWS CodePipeline.

Awesome job! We now have our pipeline ready to roll. Let's move on to the next step to set up AWS CodeBuild.

## Configure AWS CodeBuild

In this step, we'll configure AWS CodeBuild to build our Python application based on the specifications we define. CodeBuild will take care of building and packaging our application for deployment. Follow these steps:

- In the AWS Management Console, navigate to the AWS CodeBuild service.
- Click on the "Create build project" button.
- Provide a name for your build project.
- For the source provider, choose "AWS CodePipeline."
- Select the pipeline you created in the previous step.
- Configure the build environment, such as the operating system, runtime, and compute resources required for your Python application.
- Specify the build commands, such as installing dependencies and running tests. Customize this based on your application's requirements.
- Set up the artifacts configuration to generate the build output required for deployment.
- Review the build project settings and click on the "Create build project" button to create your AWS CodeBuild project.

Fantastic! With AWS CodeBuild all set up, we're now ready to witness the magic of continuous integration in action.

## Trigger the CI Process

In this final step, we'll trigger the CI process by making a change to our GitHub repository. Let's see how it works:

- Go to your GitHub repository and make a change to your Python application's source code. It could be a bug fix, a new feature, or any other change you want to introduce.
- Commit and push your changes to the branch configured in your AWS CodePipeline.
- Head over to the AWS CodePipeline console and navigate to your pipeline.
- You should see the pipeline automatically kick off as soon as it detects the changes in your repository.
- Sit back and relax while AWS CodePipeline takes care of the rest. It will fetch the latest code, trigger the build process with AWS CodeBuild, and deploy the application if you configured the deployment stage.

 ![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/d8e6eda0-1e28-4ebc-ad5d-d48a48055804)

# Demo https://github.com/iam-veeramalla/aws-devops-zero-to-hero/tree/main/day-14

# Create Build Project

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/41d0f647-9a05-4d6b-a973-f488dc1365bc)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/f5aa3810-e63a-4fdf-98dd-9a14cc8c9cd2)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/fc39d908-f469-4e1d-a76c-eab0aafb48c3)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/954d520c-108d-4111-abd7-a725c0f1ace9)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/58c4dbd8-d203-4370-a511-a780f94b7401)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/284b3bbf-1346-48d8-b764-c631916535f0)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/ab1d24c7-2b32-45c1-b974-f11bdbb6bd5a)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/e34af55a-f338-4fae-b0d5-40754a9dbe3b)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/042afd40-b03b-4e46-b68d-549b72ca0363)

# CI - Stage

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/b24253ec-8ba8-44ea-9af1-ec89286622a1)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/84cd0b1c-e99b-4f50-b955-47763c0314da)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/3b1e446b-8886-4155-809a-23c19fffa3bd)

# now How to Store the Sensitive information 

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/b7811f81-453c-468b-886b-83c4c3d3ae75)

# in Systems manager .. select Parameter Store  @ left side of option

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/250932d3-f838-4a59-962e-b282fa73ec5b)

# create parameter 

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/9a4edb97-ce2f-48a0-8fbf-8ef65df2f7d2)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/078c9b3f-7133-454a-95ab-5f47d823bd85)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/6fcb96d9-6b11-4054-bb06-827789a95e0a)


# Make Sure username & password of the above be available before inhand( from Docker hub - to Push the Docker image)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/8e1ae9f9-556f-4c5d-98e7-9aa254307ad6)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/8910b270-ae77-419a-8730-2122a6161e4e)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/e0b5b6b2-686f-49e3-9352-fbd4e7fbe75a)

# Update the code

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/4e95876a-ea58-4366-b23e-e7efd17cb7ac)

# go to role section in IAM user & give the permissions – SSM

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/a20cbcd8-e42b-4073-9d14-05c695fdc4df)

# add permissions

# Attach Policy 

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/ebd7a166-3875-481f-8d4f-75838456e1ee)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/996bc4f0-0d1b-4585-a7e5-25d7ee5ccb0a)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/148870d3-ed1d-4bf0-84a2-5f8c96c3db35)

# error Go to environment

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/c1139823-a85c-4563-bc8f-5cb913d436fa)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/a1136db9-91fb-45b5-8086-fe4f0c36019e)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/8cf1617a-e198-4b76-821c-db3087c8a31e)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/7908ca2a-dbca-4faa-81ef-3d3bdf96add5)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/81092bfe-4720-4a0e-bbd9-8b80d6c07022)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/78f18baf-d095-4027-a527-144ab025ff43)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/7037a338-37cb-409b-acd1-be07b4b29038)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/a5cbf452-c3f6-440d-87de-8bd162bb0ac2)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/d4a31a0f-4c66-4e0d-aedd-454c9516a349)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/79a9eeef-f538-4e33-aaa9-d6d3b303e97e)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/b04c2d42-5fca-42a4-9050-43f4a7162d43)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/9d8bd90e-d4e6-4535-b97e-4609f9fd88c4)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/2749d6d2-cced-4f8f-8fe6-759efb41f07a)

# Finally Codebuild excecuted & now Check Docker hub image Uploaded

# O/P in Docker hub – CI Pipeline 

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/66cbebac-cc2b-4b4a-b9bc-a403b116a353)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/aa269865-2e1d-4a25-ab38-22cae7ab1dfe)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/f8866d76-641d-4ef6-981a-a5f1274900a7)

# Last step in CI—is integrate with pipeline …. Go to Code pipeline

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/8f04b24e-3040-4314-b3d8-1a972a3ccc34)

# Create Pipeline

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/4dcf342f-5b0d-41ee-ae21-c8068d58d366)

# Service role Automatically displayed --- highlighted below 

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/f1c5d727-fd3f-4d0d-8e5e-31e14886fd97)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/0acebd84-53ff-4a5c-a168-cc425d9e953e)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/505c0887-7d41-45b6-9f93-9ed7c5ae861d)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/18ae08ba-8d1d-478e-9623-c4c31222c9b2)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/8c35bf88-087c-4e65-a788-74ff5afde6a4)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/85d07148-8b88-4a1a-a769-2c98b05ddad5)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/a93945b6-d76c-4cc9-84b6-ce9bd0263a1d)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/d0384606-ef37-4843-821e-bac3a1b363d6)

# the below is in CD part 2  ---- that cover in next Pipeline – as if now skip it

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/807807f6-c3bb-4efa-ad1b-ee8e53212cd7)

# Verify all in last Stage – to Create Pipeline

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/71d9d3d0-5737-4e77-806d-db9e63a488b4)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/18ea7ab3-2f30-4618-900c-d39c30e327fc)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/60e3fe7c-33a7-4de1-a88c-c6e0768917b4)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/9376fac8-b073-4f6c-8812-2a1da5389566)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/ad2c3824-850e-4405-8381-7c44cd1bb4c1)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/c1a20bf4-fbb1-4125-b348-e585aebf4b16)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/c377706b-f592-454b-bf05-8ef1e76a9bb5)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/1e279748-b818-4d36-a330-9a3ef5540ac0)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/a6a991fd-20ae-424e-8ce9-1fe2f8c043ba)

# test the Code  change / Commit in  my Repo will Trigger/ update the same in the aws codepipeline

# I commented in the Py – file 

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/980ff5a1-7e35-410b-8eeb-340c3b30a441)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/a0672b2f-84bd-4700-90f6-864a61fd5482)

# Triggered The Github

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/51acc0a3-518c-47d1-b1ce-15322770d712)

# Testing passed – the CI pipeline  

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/84f2076e-87c6-4e54-98c0-254e6592ac69)

# code Build

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/da691aee-96ed-4809-9b4d-abf89056962f)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/ddd8ca36-8b02-445f-8919-a367bbdfc09d)

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/bff547e9-3df7-4cdc-a832-baf4be9f4bd7)

# docker hub – changed occurred

![image](https://github.com/Siddhartha082/aws-zero-to-hero/assets/110781138/faf13fad-d9e3-40de-954d-3cfbf74025bf)


