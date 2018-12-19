FROM jupyter/base-notebook:27ba57364579

# conda/pip/apt install additional packages here, if desired.

# pin jupyterhub to match the Hub version
# set via --build-arg in Makefile
ARG JUPYTERHUB_VERSION=0.8
RUN pip install --no-cache jupyterhub==$JUPYTERHUB_VERSION

## Install R Kernel and SQL magic queries
RUN conda install -c r r-irkernel
RUN conda install -c r pyzmq
RUN conda install -c conda-forge ipython-sql
