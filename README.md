# Deploy-nodejs-app-to-eks-using-github-actions

1. Create an EKS Cluster using this command:

``
eksctl create cluster --name nodeapp --region us-east-1 --nodegroup-name linux-nodes --node-type t2.micro --nodes 2
`` <br>
Note: Make sure you install eksctl on you machine in other to run the above command. if you are on mac os simply use this command ``brew install eksctl`` on you terminal
nodeapp is the name of my cluster, please feel free to use whatever name of your choice

2. Then create .github folder and then create workflow folder inside .github folder 
3. create file with .yml extension and write the workflow code
4. Create a github repository 
5. Go to AWS and create ECR (Amazon Container Registry)
6. Create secrets in github repo
        Go to your repo settings
        click on secrets and variables
7. Test application by getting the dns name and going to a web browser

Clean up: Run: eksctl delete cluster --name nodeapp to delete your cluster to avoid unecessary billings on your account
