# Docker Scrapyd deploy files

This docker compose file can be used to deploy a scrapyd + scrapyd web combo service to manage multiple scrapy projects.

## How to use this image

From the project root, just run:

```{bash}
docker compose up

```

This should start two services:

- scrapyd server, api and minimal UI. Accessible on port 6800.
- the scrapyd web interface. Accessible on port 5000.

## Directory structure

It assumes the project will be organized with the following directory structure:
`

```
<project-root>
├── projects/
│  ├── spider-1/
│  └── spider-2/
├── scrapyd/
│  ├── logs/
│  ├── database/
│  ├── data/
└── docker-compose.yml
```

## Dependencies

Obviously: [docker](https://www.docker.com/get-started/).

The docker compose file also assumes you have already built the following images LOCALLY. They are not available for download from Docker Image Library as of now.

- [docker-scrapyd](https://github.com/fsorodrigues/docker-scrapyd)
- [docker-scrapydweb](https://github.com/fsorodrigues/docker-scrapydweb)

These are both images forked from [Zentekmx](https://github.com/zentekmx).
