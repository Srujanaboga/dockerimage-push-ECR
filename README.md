# dockerimage-push-ECR
step1: Install the Dockerdesktop local machine

step2: Create a Docker image(created ubuntu image)

step3: In AWS console search for security credentials and aws configure to local terminal

step3: In Aws console search for Elastic Container Repository-->create the repository-->select the repository and       click on view push commands (created repository name with ubuntu-image)

step4: Use the AWS CLI:Retrieve an authentication token and authenticate your Docker client to your registrycopy       the command : aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin       025066281033.dkr.ecr.us-east-1.amazonaws.com

step5: Build your Docker image using the following command:docker build -t ubuntu-image

step6: After the build completes, tag your image so you can push the image to this repository:docker tag  
       ubuntu-image:latest 025066281033.dkr.ecr.us-east-1.amazonaws.com/ubuntu-image:latest

step7: Run the following command to push this image to your newly created AWS repository:
       docker push 025066281033.dkr.ecr.us-east-1.amazonaws.com/ubuntu-image:latest

step8: Can check the image at ECR repository





