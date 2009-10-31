# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require(File.join(File.dirname(__FILE__), 'config', 'boot'))

require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

require 'tasks/rails'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "browsercms_s3"
    gem.summary = %Q{BrowserCMS is a general purpose, open source Web Content Management System (CMS), written in Ruby on Rails. This is a fork where the facility to have attachments stored on Amazon S3 has been added. Also caching has been changed to suit heroku}
    gem.email = "email2ants@gmail.com"
    gem.homepage = "http://github.com/aunderwo/browsercms_s3"
    gem.authors = ["Anthony Underwood"]

    gem.files = Dir["rails/*.rb"]
    gem.files += Dir["browsercms.gemspec"]
    gem.files += Dir["doc/app/**/*"]
    gem.files += Dir["doc/guides/html/**/*"]
    gem.files += Dir["app/**/*"]
    gem.files += Dir["db/migrate/[0-9]*_*.rb"]
    gem.files += Dir["db/demo/**/*"]
    gem.files += Dir["lib/**/*"]
    gem.files += Dir["rails_generators/**/*"]
    gem.files += Dir["public/stylesheets/cms/**/*"]
    gem.files += Dir["public/javascripts/jquery*"]
    gem.files += Dir["public/javascripts/cms/**/*"]
    gem.files += Dir["public/fckeditor/**/*"]
    gem.files += Dir["public/site/**/*"]
    gem.files += Dir["public/images/cms/**/*"]
    gem.files += Dir["public/themes/**/*"]
    gem.files += Dir["templates/*.rb"]

    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler not available. Install it with: sudo gem install technicalpickles-jeweler -s http://gems.github.com"
end

# These are new tasks
begin
  require 'rake/contrib/sshpublisher'
  namespace :rubyforge do

    desc "Release gem to RubyForge"
    task :release => ["rubyforge:release:gem"]


  end
rescue LoadError
  puts "Rake SshDirPublisher is unavailable or your rubyforge environment is not configured."
end
