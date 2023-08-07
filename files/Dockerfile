# Dockerfile

# Author       : Resonex
# Github       : https://github.com/Resonex
# Messenger    : https://m.me/Resonex
# Email        : cybersnipperz@gmail.com
# Date         : 25-08-2023
# Main Language: Python

# Download and import main images

# Operating system
FROM debian:latest
# Main package
FROM python:3

# Author info
LABEL MAINTAINER="https://github.com/Resonex/hackbank"

# Working directory
WORKDIR /hackbank/
# Add files 
ADD . /hackbank

# Installing other packages
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install php openssh-client -y
RUN pip3 install -r files/requirements.txt --break-system-packages
RUN apt-get clean

# Main command
CMD ["python3", "hackbank.py", "--noupdate"]

## Wanna run it own? Try following commnads:

## "sudo docker build . -t Resonex/hackbank:latest", "sudo docker run --rm -it Resonex/hackbank:latest"

## "sudo docker pull Resonex/hackbank", "sudo docker run --rm -it Resonex/hackbank"
