FROM centos:7.5.1804
ENV ERLANG_VERSION=21.0

RUN yum -y -q install epel-release &&  \
    yum -y -q install gcc gcc-c++ glibc-devel make ncurses-devel wget \
                   openssl-devel autoconf java-1.8.0-openjdk-devel \
                   git unzip which \
                   libGL libGLU unixODBC wxBase wxGTK wxGTK-gl  && \
    yum clean all && \
    localedef -i en_US -f UTF-8 en_US.UTF-8

RUN wget http://packages.erlang-solutions.com/site/esl/esl-erlang/FLAVOUR_1_general/esl-erlang_${ERLANG_VERSION}-1~centos~7_amd64.rpm && \
    rpm -Uvh esl-erlang_${ERLANG_VERSION}-1~centos~7_amd64.rpm
RUN yum install -y -q esl-erlang


