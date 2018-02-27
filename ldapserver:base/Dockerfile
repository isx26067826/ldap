# @edt ASIX-M11 Curs 2017-18
# ldapserver:base
# servidor ldap creacio interactiu
#----------------------------------------------------
FROM fedora:24
MAINTAINER asixm11edt "@edt ASIX-M11 Curs 2017-2018"
RUN dnf -y update vi
RUN dnf -y install vim procps iputils iproute tree nmap openldap openldap-clients openldap-servers mlocate man-db 
RUN mkdir /opt/docker
COPY ldap.conf /etc/openldap/
COPY * /opt/docker/
RUN chmod +x /opt/docker/install.sh /opt/docker/startup.sh
RUN echo "PS1='\[\e[1;32m\][\u@\h \W]\$\[\e[0m\] '" >> /etc/bashrc
WORKDIR  /opt/docker
CMD ["/bin/bash"]

