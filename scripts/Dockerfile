FROM python:3.8

RUN adduser --system gazette && \
	apt-get update -y && \
	apt-get -y install wait-for-it && \
	apt-get clean && \
	mkdir /mnt/code

COPY . /mnt/code
WORKDIR /mnt/code
ENV PYTHONPATH=/mnt/code

RUN pip install --no-cache-dir -r requirements.txt

USER gazette
