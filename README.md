#AWS_WEBAPP_SETUP_Lift_and_Shift
AWS WEBAPP SETUP using Lift_and_Shift strategy

Architecture of Project

![Architecture of Project](https://user-images.githubusercontent.com/74285496/212277845-a8ad62f0-40dc-495c-b59a-470b07c76c0b.jpg)

Flow of Executions!!
1.LOGIN INTO AWS CONSOLE
2.CREATE KEY PAIRS AND SAVE THE CREDENTIALS
3.CREATE 3 SECURITY GROUPS FOR 
    A.Tomact EC2 instance
    B.Backend EC2 instance(memcache,rabbitmq,Mysql)
    C.Load Balancer
4.Launch instance with user data from bash scripts
5.Update IP to name mapping in Route 53
6.Building app from source code
7.Upoadling artifacts to S3 bucket
8.Download artifacts to Tomact EC2 instance
9.Setup ELB with HTTPS (with certificates from AMAZON CERTIFICATE MANAGER)
10.Mapping ELB endpoints to website name in Godaddy DNS
11.Buildauto Scaling Group for Tomcat instace