# Use the base image that supports ARM64 architecture
FROM ruby:3.4.1

RUN sh -c "$(wget -O- https://github.com/deluan/zsh-in-docker/releases/download/v1.2.0/zsh-in-docker.sh)" -- \
    -t https://github.com/denysdovhan/spaceship-prompt \
    -a 'SPACESHIP_DOCKER_SHOW="false"' \
    -p git \
    -p ssh-agent \
    -p https://github.com/zsh-users/zsh-autosuggestions \
    -p https://github.com/zsh-users/zsh-completions

RUN apt-get clean && rm -rf /var/lib/apt/lists/*

# Set the default user
USER root
