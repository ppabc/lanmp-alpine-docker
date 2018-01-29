# lanmp-alpine-docker
基于alpine构建lanmp环境docker镜像


mkdir -p /tmp/rpm /data/nginx/conf/vhost /data/php /data/nginx/logs /data/nginx/run /data/wwwroot/default

docker run -d --name mysql -v /data:/data --net=host -it ppabc/lanmp-alpine-docker:mysql-1.0
docker run -d --name php5  -v /data:/data --net=host -it ppabc/lanmp-alpine-docker:php-1.0
docker run -d --name nginx -v /data:/data --net=host -it ppabc/lanmp-alpine-docker:nginx-1.0

