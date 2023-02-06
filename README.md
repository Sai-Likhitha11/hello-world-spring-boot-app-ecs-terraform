# hello-world-spring-boot-app-ecs-terraform

### Testing the Application Locally

* So for this I have downloaded all the required applications to test the application code and corrected few of the code and built it by using Maven where it's not redirecting. Attached are the screenshots which shows application is running in localhost

![image](https://user-images.githubusercontent.com/72379684/217105927-11c8dc97-7e3b-4900-8aae-e19e2f5428e5.png)

![image](https://user-images.githubusercontent.com/72379684/217106090-d6e626f5-2a70-43ec-b31f-f8afd7d54390.png)

### Creating Docker Image and Pushing to ECR

* The next step for me is to write the Dockerfile which you can find https://github.com/Sai-Likhitha11/hello-world-spring-boot-app-ecs-terraform/blob/main/Hello-world/target/Dockerfile
* Once the Dockerfile is ready then I have built an Dockerimage, Created Repository and pushed to AmazonECR. Attached are the screenshots
![image](https://user-images.githubusercontent.com/72379684/217107245-deaddcd0-dc28-4835-92cc-55b8cac1e160.png)
![image](https://user-images.githubusercontent.com/72379684/217107377-48b341f2-8b41-4ae3-b839-a21a3f3a152e.png)
![image](https://user-images.githubusercontent.com/72379684/217107400-1daef8f0-ecd5-40ae-9da3-58b1b46c869c.png)

### Creating a Cluster, Task Definitions, and Service in ECS
* This has been achieved by using Infra-as-a-code Terraform https://github.com/Sai-Likhitha11/hello-world-spring-boot-app-ecs-terraform/tree/main/Hello-world/infrastructure. 
* Created Task Defination using ECR Image that we pushed 
![image](https://user-images.githubusercontent.com/72379684/217108701-bc0d93dc-120c-4056-a1df-27043964f16c.png)
* Created a Cluster and added Service which runs 2 tasks
![image](https://user-images.githubusercontent.com/72379684/217108796-8680b7b6-184d-42d0-b405-ae7ac0bdec71.png)
![image](https://user-images.githubusercontent.com/72379684/217108859-d70a4027-7bd9-4f30-8ce9-df13ab601dd3.png)
![image](https://user-images.githubusercontent.com/72379684/217108961-2a0a1e81-c890-4e18-91b2-e50279770ffb.png)
* Finally, checked the logs and application is running sucessfully
![image](https://user-images.githubusercontent.com/72379684/217109147-4741dae7-d1c2-4f02-96c6-551d5bd4410a.png)
![image](https://user-images.githubusercontent.com/72379684/217109181-c37ffe2f-148c-494e-b3ee-745f176e1657.png)

* TO expose it to HTTPS we need to buy SSL certificate and configure domain in Route 53 which will resolve this. 





