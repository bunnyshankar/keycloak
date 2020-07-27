FROM quay.io/keycloak/keycloak:10.0.2

USER root

RUN microdnf update -y && microdnf install -y python3 && pip3 install awscli

ADD entry.sh /entry.sh
ADD realm.json /realm.json

USER jboss

ENTRYPOINT /entry.sh

EXPOSE 8080
