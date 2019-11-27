FROM rico93/v2ray_v3:caddy_base

RUN mkdir /srv/www && mkdir /srv/www/js
COPY index.html /srv/www/index.html
COPY js/fly.js     /srv/www/js/fly.js
COPY js/paper-full.min.js /srv/www/js/paper-full.min.js
COPY fly.css /src/www/fly.css
EXPOSE 80 443 2015
VOLUME /root/.caddy /srv
WORKDIR /srv

ENTRYPOINT ["/bin/parent", "caddy"]
CMD ["--conf", "/etc/Caddyfile", "--log", "stdout", "--agree=$ACME_AGREE"]