ARG SCRAPER_BASE_VERSION=latest
FROM typesense/docsearch-scraper-base:$SCRAPER_BASE_VERSION
LABEL maintainer="contact@typesense.org"
LABEL org.opencontainers.image.source="https://github.com/full-enterprise-operations-platform/typesense-docsearch-scraper"
LABEL org.opencontainers.image.licenses=MIT

WORKDIR /home/seleuser
USER 1000
COPY scraper/src ./src

ENTRYPOINT ["pipenv", "run", "python", "-m", "src.index"]
