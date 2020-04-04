FROM openjdk:8u242-jdk-buster

MAINTAINER  DBpedia Spotlight Team <dbp-spotlight-developers@lists.sourceforge.net>

RUN apt-get update && \
  apt-get install maven -y && \
  git clone https://github.com/mat-piech/model-quickstarter.git && \ 
  git clone https://github.com/mat-piech/wikistatsextractor.git && \ 
  git clone https://github.com/mat-piech/dbpedia-spotlight-model.git

RUN cd /dbpedia-spotlight-model && mvn install
RUN cd /wikistatsextractor && mvn install
RUN cd /model-quickstarter && chmod +x index_db.sh

SHELL ["/bin/bash", "-c"]
