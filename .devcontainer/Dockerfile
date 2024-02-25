FROM ubuntu
RUN apt update \
    && apt install -y wget xz-utils git \
    && wget "https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.19.1-stable.tar.xz" \
    && mkdir --parent /workspaces/flutter/sdk \
    && mv flutter_linux_3.19.1-stable.tar.xz /workspaces/flutter/sdk/ \
    && cd /workspaces/flutter/sdk \
    && tar xf flutter_linux_3.19.1-stable.tar.xz \
    && rm -f flutter_linux_3.19.1-stable.tar.xz \
    && echo 'export PATH="$PATH:/workspaces/flutter/sdk/flutter/bin"' >> $HOME/.bashrc \
    && git config --global --add safe.directory /workspaces/flutter/sdk/flutter \
    && apt install -y clang cmake ninja-build pkg-config libgtk-3-dev \
    && source $HOME/.bashrc   
