FROM centos-7.4.1708

LABEL name="crush" \
    vendor="CentOS" \
    license="GPLv2" \
    build-date="20170911"

RUN mkdir /etc/yum.repos.d/bak && mv /etc/yum.repos.d/*.repo /etc/yum.repos.d/bak
ADD CentOS7-Base-163.repo /etc/yum.repos.d/
ADD ceph.repo /etc/yum.repos.d/
RUN yum makecache
RUN yum install epel-release -y
RUN yum install python2-pip.noarch -y
RUN yum install ceph-common-10.2.9 -y
RUN yum install vim -y
RUN pip install crush

CMD ["/bin/bash"]
