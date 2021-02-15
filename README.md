# container-from-scratch-python
This is building a container from scratch

## Build the Container Yourself and Push to Docker Hub

### Build image
*(If you want to develop yourself)* 
docker build --tag=hello-world-js .

### List docker images
docker image ls

### Run my newly built container

docker run -it hello-world-js python app.py --name "Big John"

### Tag the image to match your DockerHub Repo Name

docker tag hello-world-js:latest jingjingshi09/hello-world-js:latest

### Push to Docker Hub

*Note:  You will need to change for your Docker Hub Repo*
docker push jingjingshi09/hello-world-js:latest

## Run it yourself

```bash
docker pull jingjingshi09/hello-world-js:latest
docker run -it jingjingshi09/hello-world-js:latest

#then run python app.py --help
```

## Pass in a command

```bash
docker run -it jingjingshi09/hello-world-js:latest python app.py --name "Big John"
#the output
Hello Big John!
```

### More things Do

* Lint the code with Github Actions (see the Makefile)
* Automatically build the container after lint, and push to DockerHub or some other Container Registery



