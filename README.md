# Assignment CE 3.5
1. In VS code, create a folder.
2. In the terminal - Git clone git@github.com:su-ntu-ctp/6m-cloud-3.4-cloud-native-application-containerization-i.git
3. In the explorer - Copy files from "hello-node-app" into the same working directory
4. In the terminal - Run "npm install"
5. Own Github - create a new github repo
6. In the terminal - push into the new repo
7. In the terminal - Run "AWS Configure" // config access and secret key access
8. ECR - For private Repo - //Permission needed: ecr:GetAuthorizationToken
In the terminal - Run 
"aws ecr get-login-password --region ap-southeast-1 |
docker login --username AWS --password-stdin <aws account number>.dkr.ecr.ap-southeast-1.amazonaws.com"
9. Build docker image - 
In the terminal - Run "docker build -t <IMAGE_NAME>:<IMAGE_TAG> . // docker build -t express-app:v1.0 ."
alternative - Pull iamge -
In the terminal - Run "docker image pull debian" 
10. Re-tag image - docker tag <current image name>:<current image tag> <new image name>:<new image tag> //docker tag debian:latest <aws account number>.dkr.ecr.ap-southeast-1.amazonaws.com/lwj-express-app:v1.0
11. docker push <aws account number>.dkr.ecr.ap-southeast-1.amazonaws.com/lwj-express-app:v1.0