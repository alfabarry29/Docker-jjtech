FROM ubuntu

RUN apt update -y

COPY terraform-install.sh  /tmp/terraform-install.sh

RUN cd /tmp/ && sh terraform-install.sh

RUN apt full-upgrade -y && apt install python-pip -y && pip2 install flask

# RUN pip2 install flask 

WORKDIR /opt

COPY app.py  /opt/app.py 

ENTRYPOINT FLASK_APP = /opt/app.py flask run --host= 0.0.0.0  --port= 8080

LABEL project="jjtech"


# FROM ubuntu:20.04

# RUN apt-get update && \
#     apt-get install -y python3 python3-pip && \
#     pip3 install flask

# WORKDIR /app

# COPY app.py .

# CMD ["python3", "app.py"]


