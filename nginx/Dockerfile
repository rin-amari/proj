FROM nginx:stable-alpine
COPY default.conf /etc/nginx/conf.d/default.conf
COPY ./html /var/www/html/
RUN mkdir /etc/nginx/certs/  && \
    chown nginx /var/cache/nginx /var/run /etc/nginx/certs/fullcain.pem /etc/nginx/certs/privkey.pem
USER nginx

EXPOSE 80 443
CMD ["sh", "-c", " nginx -g 'daemon off;'"]
