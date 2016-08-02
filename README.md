# Docker Compose: Drupal

Drupal/OSX development environment using [Docker Compose](https://docs.docker.com/compose/).

## Prerequisites

1. [Docker for Mac](https://docs.docker.com/docker-for-mac/) or [Docker toolbox](https://www.docker.com/products/docker-toolbox)

## Usage

1. Place Drupal in the `/docroot/` directory.
2. Run `docker-compose up -d`
3. Visit [http://localhost:8080](http://localhost:8080) or [http://192.168.99.100](http://192.168.99.100) in your browser.
4. Use `drupal:drupal@mysql/drupal` for the database settings. e.g. `docker-compose exec web drush si minimal --db-url="mysql://drupal:drupal@mysql/drupal"`
5. To run a [Drush](http://drush.org) command, execute `docker-compose exec web drush status`
6. Run `docker-compose exec web bash` to start an interactive shell _(ssh equivalent)_

## Known issues

Xdebug requires the following be performed to standardise the loopback IP: https://gist.github.com/ralphschindler/535dc5916ccbd06f53c1b0ee5a868c93
