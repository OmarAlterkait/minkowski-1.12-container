# minkowski-1.12-container
This is a singularity container for particle reconstruction usage. You can build the container using (you need root access to build)

`sudo singularity build mink-pytorch1.12.sif minkowski-pytorch1.12.def`

You can run the container using

`singularity shell --nv mink-pytorch1.12.sif`


## Packages
This package contains many common packages. Mainly

| Package           | Version |
|-------------------|---------|
| python            | 3.9     |
| cuda              | 11.6    |
| pytorch           | 1.12.0  |
| lightning         | 2.0.3   |

You can install any other package by going into the container then installing with `pip install --user`

## ROOT
A ROOT version is also available. Run `source /usr/local/root/bin/thisroot.sh` upon starting the container to initialize root.

## Jupyter 
To run a jupyter notebook through the container. On the server, run

`singularity exec --nv mink-pytorch1.12.sif jupyter notebook --no-browser --ip=0.0.0.0 --port=8888`

then on your machine tunnel using

`ssh -L localhost:8888:localhost:8888 user@your_remote_server`

You can add `-N -f` to send it to the background.

## Container Location
The container can be found at:
 - mayer:
     - `/home/oalterkait/minkowski-1.12-container/mink-pytorch1.12.sif`
     - ROOT: `/home/oalterkait/minkowski-1.12-container/mink-pytorch1.12-root.sif`

If you face any problems, please feel free to contact me
`Omar.Alterkait@tufts.edu`

