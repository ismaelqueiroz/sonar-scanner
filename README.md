# Sonar Scanner
[![GitHub issues](https://img.shields.io/github/issues/ismaelqueiroz/docker-sonar-scanner.svg "GitHub issues")](https://github.com/ismaelqueiroz/docker-sonar-scanner)
[![GitHub stars](https://img.shields.io/github/stars/ismaelqueiroz/docker-sonar-scanner.svg "GitHub stars")](https://github.com/ismaelqueiroz/docker-sonar-scanner)

The unofficial image of the Sonar Scanner, made with love by the community.

## Table of Contents

  - [What is Sonar scanner?](#what-is-sonar-scanner)
 
- [How to use this image](#how-to-use-this-image)
  - [Create a `Dockerfile` in your app project](#create-a-dockerfile-in-your-app-project)
  - [Best Practices](#best-practices)
  - [Run a single script](#run-a-single-script)
  - [Verbosity](#verbosity)
    - [Dockerfile](#dockerfile)
    - [Docker Run](#docker-run)
- [Image Variants](#image-variants)
  - [`sonar-scanner:<version>`](#sonar-scannerversion)
  - [`sonar-scanner:alpine`](#sonar-scanneralpine)
- [License](#license)
- [Supported Docker versions](#supported-docker-versions)


# Supported tags and respective `Dockerfile` links

-	[`3.3.0.1492`, `alpine` `latest` (*Dockerfile*)](https://github.com/ismaelqueiroz/docker-sonar-scanner/blob/master/3.3.0.1492/Dockerfile)
-	[`3.0.3.778` (*Dockerfile*)](https://github.com/ismaelqueiroz/docker-sonar-scanner/blob/master/3.0.3.778/Dockerfile)
-	[`3.0.0.702` (*Dockerfile*)](https://github.com/ismaelqueiroz/docker-sonar-scanner/blob/master/3.0.0.702/Dockerfile)


## What is Sonar Scanner?

The SonarQube Scanner is recommended as the default launcher to analyze a project with SonarQube.

See: http://ismaelqueiroz.github.io

# How to use this image

## Create a `Dockerfile` in your Sonar Scanner app project

# specify the sonar-scanner base image with your desired version sonar-scanner:<version>

```dockerfile
FROM ismaelqueiroz/sonar-scanner
```

You can then run the Docker image:

```console
$ docker run --rm ismaelqueiroz/sonar-scanner sonar-scanner -v
```

Just replace YOUR-SONAR-SERVER with the IP-Address of your Sonar-Server of your choice.

## Environment variables

When you start the sonar-scanner image, you can adjust the configuration of the instance by passing one or more environment variables either on the docker run command line. If you want to add a new environment variable:

 * Execution add a `-e` option with each variable and value:

```console
 $ docker run --rm ismaelqueiroz/sonar-scanner \
     -e SONAR_SCANNER_VERSION=3.3.0.1492 \
     /bin/sh -c "update; sonar-scanner -v"
```

Available variables:
 - `SONAR_SCANNER_HOME`: Sonar Scanner home. Default: **/sonarscanner**
 - `SONAR_SCANNER_VERSION`: Sonar Scanner version. Default: **3.3.0.1492**

# License

The Dockerfiles and associated scripts are licensed under the [MIT License](https://github.com/ElectroStar/Sonar-Scanner/blob/master/LICENSE).
