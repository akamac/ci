FROM openjdk:8

ENV SCALA_VERSION=2.11.7
ENV SBT_VERSION=0.13.9
ENV NODEJS_VERSION=11

RUN curl -sL https://deb.nodesource.com/setup_${NODEJS_VERSION}.x | bash - && \
	apt install -y nodejs fakeroot && \
	wget -nv http://dl.bintray.com/sbt/debian/sbt-${SBT_VERSION}.deb && \
    dpkg -i sbt-${SBT_VERSION}.deb && \
    wget -nv https://downloads.lightbend.com/scala/${SCALA_VERSION}/scala-${SCALA_VERSION}.deb && \
    dpkg -i scala-${SCALA_VERSION}.deb && \
    rm sbt-${SBT_VERSION}.deb scala-${SCALA_VERSION}.deb
