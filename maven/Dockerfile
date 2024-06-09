# # Use a base image with Java already installed
# FROM openjdk:11

# # Set environment variables
# ENV MAVEN_VERSION=3.8.4
# ENV MAVEN_HOME=/usr/share/maven

# # Install Maven
# RUN wget -q -O - https://archive.apache.org/dist/maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION-bin.tar.gz | tar -xzf - -C /usr/share \
#     && mv /usr/share/apache-maven-$MAVEN_VERSION $MAVEN_HOME \
#     && ln -s $MAVEN_HOME/bin/mvn /usr/bin/mvn

# # Set Maven path
# ENV PATH=$MAVEN_HOME/bin:$PATH

# # Specify default command
# CMD ["mvn", "--version"]


# Use an official OpenJDK runtime as a parent image
FROM openjdk:11-jdk-slim

# Install Maven
RUN apt-get update && \
    apt-get install -y maven && \
    rm -rf /var/lib/apt/lists/*

CMD ["mvn", "--version"]