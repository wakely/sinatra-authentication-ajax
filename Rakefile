require 'rubygems'
require 'rake'
#require 'spec/rake/spectask'

begin
  require 'jeweler'
  
  Jeweler::Tasks.new do |gemspec|
    gemspec.name           = 'sinatra-authentication-ajax'
    gemspec.version        = '0.4.2'
    gemspec.description    = "Simple authentication plugin for sinatra, with ajax"
    gemspec.summary        = "Simple authentication plugin for sinatra, with ajax"
    gemspec.homepage       = "http://github.com/wakely/sinatra-authentication-ajax"
    gemspec.author         = "Max Justus Spransy, Scott Wakely"
    gemspec.email          = "wakely@uchicago.edu"
    gemspec.add_dependency "sinatra"
    gemspec.add_dependency "dm-core"
    gemspec.add_dependency "dm-migrations"
    gemspec.add_dependency "dm-validations"
    gemspec.add_dependency "dm-timestamps"
    gemspec.add_dependency "rufus-tokyo"
    gemspec.add_dependency "sinbook"
    gemspec.add_dependency "rack-flash3"
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it first!"
end

Dir["#{File.dirname(__FILE__)}/tasks/*.rake"].sort.each { |ext| load ext }

require 'rake/testtask'

Rake::TestTask.new do |t|
  t.libs << "test"
  t.test_files = FileList['test/activerecord_test.rb']
  t.verbose = true
end

#desc 'Run all specs'
#Spec::Rake::SpecTask.new('specs') do |t|
#  t.spec_files = FileList['spec/**/*.rb']
#end
