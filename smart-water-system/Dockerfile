FROM nginx:alpine
ARG BREAK_HEALTH=false
COPY index.html /usr/share/nginx/html/index.html
RUN printf 'OK\n' > /usr/share/nginx/html/health.txt && \
    if [ "$BREAK_HEALTH" = "true" ]; then rm /usr/share/nginx/html/health.txt; fi
EXPOSE 80
