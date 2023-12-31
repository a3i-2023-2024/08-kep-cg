---
title: AI in the Industry Tutorials (RUL-based maintenance policies)
author: michele.lombardi2@unibo.it
---

# Column Generation for More Scalable Combinatorial Optimization #

This is the eight lecture block for the 2023/2024 edition of the "AI in the Industry" course, from [University of Bologna](https://www.unibo.it). Each lecture consists of a tutorial that tackles a simplified industrial problem my means of AI techniques, from Machine Learning to Combinatorial Optimization (and later on their combination).

While the whole course looks like cookbook, the real goal is using examples to teach how industrial problem can be methodically approaches, analyzed, and tackles using a combination of techniques.

This tutorial in particular tackles a use case involving the management of an organ transplantation problem, tackle via Mathematical Programming and Column Generation.


# Accessing the Lecture #

## Local Execution (Preferred) ##

Students are strongly encouraged to _run all lectures locally_. Doing this will require to:

* Install Docker, by following the [online instructions](https://docs.docker.com/get-docker/).
* Install Docker Compose, by following the [online
instructions](https://docs.docker.com/compose/install/)
* Clone the repository with the tutorial, in this case via the command:
```sh
git clone https://github.com/a3i-2023-2024/08-kep-cg
```
* Start the container via Docker Compose, from the main directory of the
tutorial:
```sh
docker-compose up
```

On linux systems, you may need to start the docker service first.

No matter which OS your are running, the first execution of this process will be fairly long, since Docker will need to download a base image for the container (think of a virtual machine disk) and then some boilerplate configuration steps will need to be performed (e.g. installing jupyter in the container). Subsequent runs will be much faster.

The process will end with a message such as this one:
```sh
To access the notebook, open this file in a browser:
    file:///home/lompa/.local/share/jupyter/runtime/nbserver-1-open.html
Or copy and paste this URL:
    http://127.0.0.1:39281/?token=0cd92163797c3b3abe67c2b0aea57939867477d6068708a2
```
Copying one of the two addresses in a file browser will provide access to the Jupyter server running in the spawned container. By default, the main lecture folders is shared with the container environment, so any modification you make in the contain will reflect in the host system, and the other way round.

Once you are done, pressing CTRL+C on the terminal will close the Docker container.

For more information about how Docker works (such as the difference between images and containers, or how to get rid of all of them once you are done with the tutorial), you can check the [Docker documentation](https://docs.docker.com/).

**A note on using this lecture without Docker:** some plotting function in the lecture require the graphviz system, which will be automatically installed in the container if you are using docker. If you don't use docker, make sure you also have graphviz installed.

## Read-only Access and PDF Notes ##

You can inspect the individual notebooks in by just clicking on any `*.ipynb` file in the `notebooks` directory: github provides a notebook viewer that mostly works, though this access method may occasionally have issue when displaying plots.

The repository contains PDF notes for all the notebooks. They can be used for read-only access (with more consistent results compared to the github notebook viewer), but more importantly they can be useful to add annotations. Just keep in mind that in case of updates, cloning the repository will replace the PDF files.
