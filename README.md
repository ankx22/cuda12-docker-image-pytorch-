# Docker Image for Ubuntu 22.04 with CUDA Toolkit and pytorch 
Has most basic dependencies and more can be added by modifying the [Dockerfile](Dockerfile)

- To run the docker container:
	- Clone the repo
  - In the repo folder open a bash terminal and run
    ```bash
    docker build -t cuda12 .
    ```
  - Once the download and setup of the image is complete just run the docker image by
    ```bash
    docker run -it --rm --gpus all -v "/actual/path/to/data":/data --name name_of_the_container -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix cuda12 bash
    ```
  - To access the bash on a different terminal window run
    ```bash
    docker exec -it container_id_or_name /bin/bash
    ``` 

## Maintained by
Ankit Talele - amtalele@wpi.edu
