# docker_nginx_ssl

This docker image is based on :

https://hub.docker.com/r/marvambass/nginx-ssl-secure/

To **build** the image :

sudo docker build -t lcbruit/nginx_ssl:v1.1 .

To **run** the docker container :

sudo docker run -d -p 80:80 -p 443:443 -e 'DH_SIZE=512' -v /share:/etc/nginx/external/ lcbruit/nginx_ssl:v1.1

**Ensure** you have the directory /share on your host machine.

Copy nginx.conf to /share

Create a directory  /share/cert/live ***ensure*** the files .cer .csr .key already exist

***Configure*** /share/nginx.conf as necessary to include files and other application forwards. 

Test Nginx :

  * http://XXXXXXXXXXXXXX.xuhl-tr.nhs.uk


