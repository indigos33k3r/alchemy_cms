source 'http://rubygems.org'

gemspec

#For some strange reason it's only loaded outside any group
gem 'jasmine'
gem 'jasminerice'

group :test do
  gem 'sqlite3'               if ENV['DB'].nil? || ENV['DB'] == 'sqlite'
  gem 'mysql2'                if ENV['DB'] == 'mysql'
  gem 'pg'                    if ENV['DB'] == 'postgresql'
  gem 'poltergeist', '0.6.0'
  unless ENV['CI']
    gem 'launchy'
  end
end

group :assets do
  gem 'sass-rails', '~> 3.2.3'
  gem 'coffee-rails', '~> 3.2.1'
  gem 'uglifier', '>= 1.0.3'
  gem 'sassy-buttons', :github => 'tvdeyen/Sassy-Buttons'
end

group :development do
  unless ENV['CI']
    #gem 'localeapp'
    gem 'guard-spork'
    gem 'ruby-debug19', :require => 'ruby-debug', :platform => :ruby_19
    gem 'ruby-debug', :platform => :ruby_18
  end
end
