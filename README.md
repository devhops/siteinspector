# SiteInspector

![Build](https://img.shields.io/github/workflow/status/siteinspector/siteinspector/Rspec)
![Version](https://img.shields.io/docker/v/siteinspector/siteinspector)
![Pulls](https://img.shields.io/docker/pulls/siteinspector/siteinspector)

[![Screenshot](https://www.getsiteinspector.com/screenshot.png)](https://www.getsiteinspector.com)

SiteInspector is a free, open-source tool that helps to find spelling errors, grammatical errors, and broken links on websites. It's written in Ruby/Rails with Vue.js front-end and uses a PostgreSQL database and Sidekiq with Redis to perform concurrent crawling.

Visit [getsiteinspector.com](https://www.getsiteinspector.com)

## Installation

### Docker

Install docker and docker-compose on your host machine and run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/siteinspector/siteinspector/master/scripts/docker-install.sh)"
```

Open the app locally on port 808 ([http://localhost:808/](http://localhost:808/)) or using your remote server IP.

### Heroku


Deploy on Heroku using the button below:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

Make sure that you have at least one worker dyno running - `heroku ps:scale worker=1 -a <app_name>`.

### Manually using docker-compose.yml

```bash
mkdir siteinspector && cd siteinspector

wget https://raw.githubusercontent.com/siteinspector/siteinspector/master/docker-compose.yml

docker-compose up
```

## License

SiteInspector is licensed under the AGPL v3 license.
