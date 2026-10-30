FROM nginx:alpine

LABEL org.opencontainers.image.title="codyssey-nginx" \
      org.opencontainers.image.authors="Zino03"

ENV APP_ENV=dev

COPY site/ /usr/share/nginx/html/

EXPOSE 80

HEALTHCHECK --interval=30s --timeout=3s --retries=3 \
  CMD wget -q --spider http://localhost/ || exit 1