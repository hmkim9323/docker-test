# docker-test

Step 1
    Create a new directory
        mkdir docker-test && cd docker-test
Step 2
    Create a file called "index.html"
        echo "Hello world" > index.html
Step 3
    Create a file called "Dockerfile"
        touch Dockerfile
Step 4
    Open the "Dockerfile" file in a text editor and add the following lines
        FROM nginx
        COPY index.html /usr/share/nginx/html
Step 5
    Start docker & Build docker image from dockerfile
        docker build -t docker-test .
Step 6
    Run docker container from the image
        docker run -d -p 8080:80 docker-test
Step 7
    Open a browser and navigate to http://localhost:8080




* NOTE
A Dockerfile is a text file with insturctions to build a Docker image.
When we run a Dockerfile, Docker image is created.
When we run the docker image, containers are created.

The above Dockerfile defines a new Docker image that
 - uses the oficial nginx image as a base image
 - then copy the index.html file to the /usr/share/nginx/html directory(nginx default directory) in the image.