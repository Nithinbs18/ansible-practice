FROM centos:7
RUN yum update -y 
RUN yum install -y epel-release && \ 
    yum install -y \
    nginx && \
    yum clean all
COPY ./docker-content/default.conf /etc/nginx/conf.d/
COPY ./docker-content/index.html /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]