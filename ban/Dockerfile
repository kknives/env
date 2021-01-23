FROM ubuntu:latest

ENV DEBIAN_FRONTEND noninteractive
ENV LANG C.UTF-8

RUN \
    apt-get update \
    && apt-get -yq install \
    build-essential \
    binutils-dev\
    libc6 \
    libncurses5 \
    libstdc++6 \
    python3 \
    python-pip-whl \
    git \
    tmux \
    gdb \
    gdb-multiarch \
    gdbserver \
    ltrace \
    strace \
    curl \
    wget \
    vim \
    zsh \
    netcat \
    qemu \
    qemu-user \
    qemu-user-static \
    ruby


# Get dotfiles
CMD git clone https://github.com/kknives/setupc $HOME/setupc && \
  chmod +x $HOME/setupc/setup.sh && \
  $HOME/setupc/setup.sh


WORKDIR /root/ctf
CMD ["/usr/bin/bash"]
