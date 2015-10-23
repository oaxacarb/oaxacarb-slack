[![Code Climate](https://codeclimate.com/github/railslink/railslink/badges/gpa.svg)](https://codeclimate.com/github/railslink/railslink)
[![Dependency Status](https://gemnasium.com/railslink/railslink.svg)](https://gemnasium.com/railslink/railslink)
[![Circle CI](https://circleci.com/gh/railslink/railslink.svg?style=shield)](https://circleci.com/gh/railslink/railslink)
[![Coverage Status](https://coveralls.io/repos/railslink/railslink/badge.svg?branch=coverage&service=github)](https://coveralls.io/github/railslink/railslink?branch=coverage)

# Oaxaca.rb Slack 

https://oaxacarb.herokuapp.com

http://oaxacarb.org/

Official website of Oaxaca.rb Link.


## Getting Started
 
### Dependencies
Make sure you have installed bundler and PostgreSQL.

```
# if you need to install PostgreSQL on Mac with Homebrew

brew install postgresql
```

### Setup

Clone this repo and configure database.

If you already have a local PostgreSQL superuser, make `.env` file on project root and configure like this:

```
PG_USER=mysuperuser
PG_PASSWORD=mypassword
SLACK_API_TOKEN=your-slack-api-token
```

You can get your Slack API token at https://api.slack.com/web#authentication

If you don't have a superuser yet, create oaxacarb user, with password "oaxacarb"

```
createuser -P -s -e oaxacarb
```

Then run:

```
bundle
bundle exec rake db:create
bundle exec rake db:migrate
bundle exec rake slack:update
bundle exec rails s
````
