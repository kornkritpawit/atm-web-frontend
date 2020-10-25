FROM ubuntu
RUN apt-get update && \
	apt-get install -y \
	git \
    maven

RUN git clone \
    https://github.com/kornkritpawit/atm-web-frontend.git

RUN cd /atm-web-frontend && pwd && ls \
    && mvn clean && mvn install && \
    ls && cd target && ls && pwd
EXPOSE 8090

WORKDIR /atm-web-frontend/target
ENTRYPOINT ["java", "-jar", "KritpawitAtmFrontDocker.jar"]