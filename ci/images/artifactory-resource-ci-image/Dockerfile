FROM ubuntu:bionic-20181018

RUN apt-get update
RUN apt-get install --no-install-recommends -y ca-certificates net-tools libxml2-utils git curl
RUN rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME /opt/openjdk
ENV PATH $JAVA_HOME/bin:$PATH
RUN mkdir -p /opt/openjdk && \
    cd /opt/openjdk && \
    curl https://java-buildpack.cloudfoundry.org/openjdk/bionic/x86_64/openjdk-1.8.0_192.tar.gz | tar xz

ADD https://raw.githubusercontent.com/spring-io/concourse-java-scripts/v0.0.2/concourse-java.sh /opt/
