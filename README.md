<!--
SPDX-FileCopyrightText: NOI Techpark <digital@noi.bz.it>

SPDX-License-Identifier: CC0-1.0
-->

# Ummadum - Alto Adige
Repository for the [Carpooling](#) website created with [Hugo](https://gohugo.io/).

[![REUSE Compliance](https://github.com/noi-techpark/it.bz.carpooling/actions/workflows/reuse.yml/badge.svg)](https://github.com/noi-techpark/odh-docs/wiki/REUSE#badges)
[![CI/CD](https://github.com/noi-techpark/it.bz.carpooling/actions/workflows/main.yml/badge.svg)](https://github.com/noi-techpark/it.bz.carpooling/actions/workflows/main.yml)

## Table of contents

- [Gettings started](#getting-started)
- [Deployment](#deployment)
- [Docker environment](#docker-environment)
- [Information](#information)

## Getting started

These instructions will get you a copy of the project up and running
on your local machine for development and testing purposes.

### Prerequisites

To build the project, the following prerequisites must be met:

- [Hugo](https://gohugo.io/)

If you don't want to install all prerequisites directly on your machine and instead use a Docker environment with all prerequisites already installed and configured, you can check out the [Docker environment](#docker-environment) section.

### Source code

Get a copy of the repository:

```bash
git clone git@github.com:flashbeing/carpooling-website.git
```

Change directory:

```bash
cd carpooling-website
```

### Development

To start a local webserver that serves the project, simply run the following command:

```bash
hugo server -s src
```

The website will be available at [http://127.0.0.1:1313](http://127.0.0.1:1313). It also recompiles automatically if you make any change to the source code.

## Deployment

**Note: this part still has to be implemented. The documentation is taken from other hugo projects of NOI**

To deploy the website, simply run the command `hugo -s src -d ../target` from the root folder of the project. The final version of the website will then be generate inside the `target` folder.

## Docker environment

**Note: this part still has to be implemented. The documentation is taken from other hugo projects of NOI**

For the project a Docker environment is already prepared and ready to use with all necessary prerequisites.

These Docker containers are the same as used by the continuous integration servers.

### Customization

Simply edit, for the language you want to customize, the config file in src/data/ using the yml language format.

### Installation

Install [Docker](https://docs.docker.com/install/) (with Docker Compose) locally on your machine.

### Start and stop the containers

Before start working you have to start the Docker containers:

```
docker-compose up --build --detach
```

The website will be available at [http://127.0.0.1:1313](http://127.0.0.1:1313). It also recompiles automatically if you make any change to the source code.

After finished working you can stop the Docker containers:

```
docker-compose stop
```

## Information

### Support

For support, please contact [info@software.bz.it](mailto:info@software.bz.it).

### Contributing

If you'd like to contribute, please follow the following instructions:

https://docs.opendatahub.com/en/latest/guidelines/contributors.html

### Documentation

More documentation can be found at [https://opendatahub.readthedocs.io/en/latest/index.html](https://opendatahub.readthedocs.io/en/latest/index.html).

### Boilerplate

The project uses this boilerplate: [https://github.com/idm-suedtirol/hugo-boilerplate](https://github.com/idm-suedtirol/hugo-boilerplate).

### License

The code in this project is licensed under the Mozilla Public License 2.0 license.
See the LICENSE.md file for more information.

### REUSE

This project is [REUSE](https://reuse.software) compliant, more information about the usage of REUSE in NOI Techpark repositories can be found [here](https://github.com/noi-techpark/odh-docs/wiki/Guidelines-for-developers-and-licenses#guidelines-for-contributors-and-new-developers).

Since the CI for this project checks for REUSE compliance you might find it useful to use a pre-commit hook checking for REUSE compliance locally. The [pre-commit-config](.pre-commit-config.yaml) file in the repository root is already configured to check for REUSE compliance with help of the [pre-commit](https://pre-commit.com) tool.

Install the tool by running:
```bash
pip install pre-commit
```
Then install the pre-commit hook via the config file by running:
```bash
pre-commit install
```
