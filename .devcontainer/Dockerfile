FROM mcr.microsoft.com/devcontainers/base:noble

RUN apt-get update && apt-get upgrade -y && apt-get install -y \
    neovim \
    unzip \
    curl \
    zip

SHELL [ "/bin/bash", "-c" ]

RUN su vscode -c 'curl -s "https://get.sdkman.io" | bash'
RUN su vscode -c 'source "$HOME/.sdkman/bin/sdkman-init.sh" \
    && sdk install java 23-graal \
    && sdk install maven \
    && sdk install quarkus'
