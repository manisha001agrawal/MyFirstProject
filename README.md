# MyFirstProject
Step 1 :- Create Dockerfile which will create httpd image                                                                                                                     
step 2 :- Create index.html which contain the webserver code                                                                                                                   
step 3 :- Launch Aws ec2 instance using ansible playbook                                                                                                                      
step 4 :- Launch Jenkins                                                                                                                                                       
       -> Create 3 Jobs which will run one after one automatically                                                                                                           
       -> First job will pull the DockerFile from github, build image and push into Docker hub                                                                                 
       -> The duty of second job is to install the docker, deamon docker service on the aws instance which launched using ansible.                                             
       -> And Finally, the duty of third job to launch docker container using that image which created by Dockerfile.                                                         
step 5 :- search url( <public of instance>:port )                                                                                                                             
  
Command for build docker image and push into docker hub                                                                                                                      
              "sudo docker build -t httpd:v1 ."                                                                                                                               
              "sudo docker tag httpd:v1 manisha001agrawal/httpd:v1"                                                                                                           
              "sudo docker push manisha001agrawal/httpd:v1"                                                                                                                   
     
Command for install docker                                                                                                                                                  
              "sudo yum install docker -y"                                                                                                                                    
              
Command for deamon docker service                                                                                                                                             
              "sudo systemctl start docker"                                                                                                                                   
              
Command for deamon docker service                                                                                                                                             
              ##### "sudo docker pull manisha001agrawal/httpd:v1"                                                     # pull image from docker hub                                   
              ##### "sudo docker run -dit -p 81:80 --name os1 manisha001agrawal/httpd:v1"

## Image of webserver:-                                                                                                                                                           
![image](https://user-images.githubusercontent.com/67043518/115163104-db681e00-a0c4-11eb-97d2-87165efbbc27.png)

## AWS EC2-Instance                                                                                                                                                               
![image](https://user-images.githubusercontent.com/67043518/115163074-b5427e00-a0c4-11eb-94dd-d33da5c0673f.png)

## Job1 running Output

![image](https://user-images.githubusercontent.com/67043518/115163953-bfb34680-a0c9-11eb-8ea4-6c801f52d250.png)

## Job2 running Output                                                                                                                                                           
![image](https://user-images.githubusercontent.com/67043518/115163967-d22d8000-a0c9-11eb-8066-b438d50c0d4c.png)

## Job3 running Output                                                                                                                                                           
![image](https://user-images.githubusercontent.com/67043518/115164121-ea9d9a80-a0c9-11eb-8454-d8c5c98731be.png)

# Thank You
