# Changelog

## 2017-02-12

### Enhancements

- **Issue 31:** Use `debian:jessie-slim` as base image,
    and perform the same cleaning on documentation after package installation.
- **Issue 66:** Remove npm and grunt from akeneo images
    (use dedicated images for that, like [digitallyseamless](https://hub.docker.com/u/digitallyseamless/) images).
- **Issue 115:** Configure `carcel/fpm` to use port 9001 instead of socket.

## 2017-01-05

### Enhancement

- **Issue 24:** Add a basic CI on Travis (ensure all images can be built before merge).

## 2016-12-21

### Enhancements

- **Issue 106:** Enhance compose examples and documentation.
- **Issue 108:** Enhance helper commands.

### Bug fix

- **Issue 110:** Add missing "user" option in compose files.

## 2016-12-18

### Enhancements

- **Issue 99:** Deactivate Xdebug by default.
- **Issue 100:** Add a script to easily perform "cache:clear" on Akeneo. Assets are also dumped as symlinks now.

### Bug fix

- **Issue 75:** Allow to properly restart apache container by removing `/var/run/apache2/apache2.pid` in
    `carcel/apache-php` image entry point. 

## 2016-12-12

### Enhancements

- **Issue 88:** Allow user to config Xdebug from environment variables.

## 2016-12-05

### Enhancement

- **Issue 74:** Add a default Xdebug configuration in `carcel/php` image.

## 2016-11-28

### Enhancement

- **Issue 66:** Add npm and grunt on akeneo development images (needed to run JavaScript and CSS static analysis).

### Bug fixes

- **Issue 62:** Improve package install and cleaning.
- **Issue 68:** Update compose documentation.

## 2016-11-21

### Bug fixes

- Fix some broken links in documentation.

### Bug fixes

## 2016-10-31

### Enhancement

- **Issue 53:** Reorganize documentation (minimalist READMEs, all important documentation in `COMPOSE.md`).

## 2016-10-22

### Bug fixes

- **Issue 51:** Fix an issue when running behat tests (add missing environment variable and volume sharing in compose
    examples).
- **Issue 52:** Add `perceptualdiff` package in behat images (required to run Akeneo Enterprise Edition behats).

## 2016-10-15

### Enhancements

- **Issue 22:** Add `carcel/akeneo-fpm` and `carcel/akeneo-behat-fpm` images (based on `carcel/fpm`),
    and `carcel/akeneo-nginx` and `carcel/akeneo-behat-nginx` (based on `carcel/nginx`).
- **Issue 23:** Add `carcel/nginx` image.

### Bug fixes

- **Issue 34:** Fix user declaration in Dockerfiles by placing it at the end.
- **Issue 36:** Raise PHP upload size limit to 20 MB.
- **Issue 37:** Fix Selenium container usage in compose file example.
- **Issue 45:** Fix an issue with composer installation during `carcel/php` image build.

## 2016-10-09

### Enhancements

- **Issue 5:** Add `carcel/fpm` image (extends `carcel/php`). Introduce a new docker compose file example dedicated to FPM.
- **Issue 20:** Split `carcel/apache-php` image to introduce a new `carcel/php` image (the first one extends the second).

## 2016-10-07

### Enhancement

- **Issue 13:** Add images `carcel/akeneo` and `carcel/akeneo-behat`.
    These new images extends the original one, which is now known as `carcel/apache-php` image.
    Each image is in its own subfolder, with its own README. A compose file example was added.

## 2016-10-03

### Enhancement

- Optimize packages installation and cleanup to reduce image size.

## 2016-09-25

### Enhancement

- **Issue 6:** Run only Apache daemon as foreground process. MySQL and MongoDB are removed and to be launched in other containers.

## 2016-08-22

### Enhancement

- **Issue 1:** Add imagemagick and its php extension.

## Initial commit (2016-08-15)

- One dockerfile providing a complete LAMP environment, based on `debian/jessie` image.
    Processes are launched through `supervisord`.