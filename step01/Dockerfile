FROM openresty/openresty:alpine-fat

RUN luarocks install lua-resty-redis

COPY nginx.conf /etc/nginx/nginx.conf
COPY resty.conf /usr/local/openresty/nginx/conf/nginx.conf

CMD ["/usr/local/openresty/bin/openresty", "-c", "/etc/nginx/nginx.conf", "-g", "daemon off;"]