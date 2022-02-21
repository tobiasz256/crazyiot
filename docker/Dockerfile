FROM ubuntu:latest

# Avoid warnings by switching to noninteractive
ENV DEBIAN_FRONTEND=noninteractive

#Update and install necessary packages
RUN apt-get update && apt-get -y install wget \
    git
#Set workidir
WORKDIR /usr

RUN wget https://dot.net/v1/dotnet-install.sh && \
    bash dotnet-install.sh -c Current --runtime aspnetcore

#Set path
ENV PATH="/root/.dotnet:${PATH}"

