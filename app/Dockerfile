FROM redmine:5.1.2-alpine3.20

RUN apk add --no-cache musl-locales cvs
RUN echo "gem 'sidekiq'" >> /usr/src/redmine/Gemfile
RUN bundle install
RUN echo "config.active_job.queue_adapter = :sidekiq" >> /usr/src/redmine/config/additional_environment.rb
