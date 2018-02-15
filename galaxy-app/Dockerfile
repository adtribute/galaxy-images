FROM harrisonhuntr/alpine:0.0.1

# Make sure we have xz-utils so we can untar node binary, and jq to parse
# star.json to choose the npm version.
RUN apk update && apk upgrade
RUN apk add jq
RUN apk add xz
RUN rm -rf /var/cache/apk/*

ADD ./app /app
RUN mkdir -p /app/bundle

CMD ["/app/run.sh"]
