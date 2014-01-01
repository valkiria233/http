source 'http://rubygems.org'

gem 'rake'
gem 'jruby-openssl' if defined? JRUBY_VERSION

group :development do
  gem 'pry'
  gem 'pry-rescue'
  platforms :ruby_19, :ruby_20 do
    gem 'pry-debugger'
    gem 'pry-stack_explorer'
  end
  platforms :ruby_19, :ruby_20, :ruby_21 do
    gem 'celluloid-io'
    gem 'guard-rspec'
  end
end

group :test do
  gem 'coveralls', :require => false
  gem 'rspec', '>= 2.14'
  gem 'rubocop', '>= 0.16', :platforms => [:ruby_19, :ruby_20, :ruby_21]
  platforms :jruby, :ruby_18 do
    gem 'json', '>= 1.8.1'
    gem 'mime-types', '~> 1.25'
  end
end

platforms :rbx do
  gem 'racc'
  gem 'rubinius-coverage', '~> 2.0'
  gem 'rubysl', '~> 2.0'
  gem 'rubysl-json', '~> 2.0'
end

# Specify your gem's dependencies in http.gemspec
gemspec
