FROM ruby:2.6.3

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN mkdir /docker_hub_test
WORKDIR /docker_hub_test
COPY Gemfile /docker_hub_test/Gemfile
COPY Gemfile.lock /docker_hub_test/Gemfile.lock
RUN bundle install
ADD . /docker_hub_test

# CMD ["rails", "server", "-b", "0.0.0.0"]
