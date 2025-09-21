FROM --platform=linux/amd64 mcr.microsoft.com/vscode/devcontainers/base:0-bullseye

ENV DEBIAN_FRONTEND=noninteractive
RUN apt update && apt upgrade -y

ENV ZIG_VERSION=0.16.0-dev.254+6dd0270a1
RUN wget "https://ziglang.org/builds/zig-x86_64-linux-${ZIG_VERSION}.tar.xz"
RUN tar Jxvf "zig-x86_64-linux-${ZIG_VERSION}.tar.xz" -C /usr/local && rm "zig-x86_64-linux-${ZIG_VERSION}.tar.xz"
RUN mv /usr/local/zig-x86_64-linux-${ZIG_VERSION} /usr/local/zig-linux
ENV PATH=/usr/local/zig-linux:${PATH}

ENV ZLS_VERSION=0.15.0
RUN wget "https://github.com/zigtools/zls/releases/download/${ZLS_VERSION}/zls-x86_64-linux.tar.xz"

RUN tar Jxvf zls-x86_64-linux.tar.xz -C /usr/local && rm zls-x86_64-linux.tar.xz
