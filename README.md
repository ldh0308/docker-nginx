# Docker

sudo docker ps -a -q
이름만 보기# Docker

# Step #1
- DockerHub에서 ubuntu pull & run
```bash
$ sudo docker pull ubuntu:22.04

$ sudo docker run -it --name utuntu -d ubuntu:22.04
```

# Step #2
```bash
$ vi Dockerfile

FROM ubuntu:22.04
RUN ["apt", "update"]
RUN apt=get install -y nginx
EXPOSE 80 // 
CMD ["nginx", "-g", "daemon off"] // 1번만 와야한다

