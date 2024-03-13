# fix-sharepoint-hashbang

## About / Synopsis

This plugin provides a `routing.html` file that overrides the **WEB UI**'s `routing.js` so that incorrect URLs built by **Sharepoint** (partially encoded hashbang) work with the **Nuxeo Web UI**.


It was generated with the following commands:
```
```

## Requirements

Building requires the following software:

* git
* maven
* docker (only for **Option 1** below)
* docker-compose (only for **Option 1** below)

## Build

```
git clone ...
cd fix-sharepoint-hashbang

mvn clean install
```

if you don't want to build the **Docker** image, use:
```
mvn clean install -DskipDocker
```

## Installation

### Option 1 (using the Docker image)

* create **Docker Compose**'s `.env` file:
```
cp .env.sample .env
```
* configure variable `NUXEO_CLID` with your **Nuxeo CLID** in file `.env`
* start **Docker** container:
```
docker-compose up -d ; docker-compose logs -f ; docker-compose down -v
```

### Option 2

```
nuxeoctl mp-install fix-sharepoint-hashbang/fix-sharepoint-hashbang-package/target/fix-sharepoint-hashbang-package-*.zip
```

## Support

**These features are not part of the Nuxeo Production platform, they are not supported**

These solutions are provided for inspiration and we encourage customers to use them as code samples and learning resources.

This is a moving project (no API maintenance, no deprecation process, etc.) If any of these solutions are found to be useful for the Nuxeo Platform in general, they will be integrated directly into platform, not maintained here.


## License

[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)

## About Nuxeo

Nuxeo Platform is an open source Content Services platform, written in Java. Data can be stored in both SQL & NoSQL databases.

The development of the Nuxeo Platform is mostly done by Nuxeo employees with an open development model.

The source code, documentation, roadmap, issue tracker, testing, benchmarks are all public.

Typically, Nuxeo users build different types of information management solutions for [document management](https://www.nuxeo.com/solutions/document-management/), [case management](https://www.nuxeo.com/solutions/case-management/), and [digital asset management](https://www.nuxeo.com/solutions/dam-digital-asset-management/), use cases. It uses schema-flexible metadata & content models that allows content to be repurposed to fulfill future use cases.

More information is available at [www.nuxeo.com](https://www.nuxeo.com).

