## Dockerize PHP Application

![](https://binus.ac.id/knowledge/wp-content/uploads/2020/12/docker-php-logo.png)

Easily setting up docker environment , to run simple php script, here already provide Dockerfile and docker-compose.yml . Just follow these instruction to dockerize php application 

disclaimer : only provided simple setup for development / research purpose only . 

Technical notes : 
- PHP version is php php:7.4-apache
- image: mydemophpimage
- ports:
   - "80:80"
   - "443:443"
- volumes:
   - ./app:/var/www/html
- network : test

Here we will run php script inside **app** folder kindly follow these detail instruction :
- Initate with clone repository 
- Enter root directory with terminal 
- Run this command
`docker build -t mydemophpimage .` 

	###### 	notes :  mydemophpimage is image name
- Make sure u get succes message without error 
- Then you can display docker image that already create with : 
`docker image ls | grep mydemophpimage `
- After image already succesfully create we can run this commad to run the image 
`docker compose up` you can add **-d ** if you want run in it , in the background

> Additonal notes : 
- `docker ps | grep mydemophpimage` : command for check exisiting proses .
- `docker exec -it docker_file_container_name bash` : commad for acces the docker server more less ssh access . 

