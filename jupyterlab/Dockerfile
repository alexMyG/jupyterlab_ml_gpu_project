FROM alexmyg/jupyterlab_ml_gpu_base:latest


# Defining ARG variables passed from docker-compose
ARG UID
ARG GID
ARG USER

RUN echo ${UID}

RUN echo ${GID}

RUN echo ${USER}

RUN addgroup --gid $GID $USER 
RUN adduser --disabled-password --gecos '' --uid $UID --gid $GID $USER 

# Giving root permissions to $USER
RUN adduser $USER sudo
RUN echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers



USER $USER


WORKDIR /home/$USER/work

ENV SHELL=/bin/zsh