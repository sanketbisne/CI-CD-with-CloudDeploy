# CI-CD-with-CloudDeploy

" This Repository Walks you through Cloud Build "
We will create a Trigger in Cloud Build , so whenever developer will push the code in the github repository , the build will be started in the Google Cloud Build,
So start with following steps:
- Create a repository in Github
- Create a Trigger in Cloud Build and Authenticate with Git
- Now Create a Dockerfile in project
- add application Code
- add cloudbuild.yaml which contains the steps about 
   > Building the image
   > Pushing into Google Container Regisitry
   > Deploying into K8s cluster
- Now we can  see the Cloud builds in the GCP console and see the Workloads runnning in the GCP.


1. Applying the Clouddeploy.yaml File to Register Our Clusters in Pipeline

gcloud deploy apply --file clouddeploy.yaml --region=asia-east1 --project=PROJECT_ID

2. After you Push your Code changes in master branch, Cloud Build will get Trigger and then Steps will be Executed from cloudbuild.yaml file

3. We can see the Realease been deployed inside our pipeline

4. After Release get Deployed in Our DEV environment we can then Promote our Release to Prod Clusters