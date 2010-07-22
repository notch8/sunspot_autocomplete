require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |s|
    s.name = "sunspot_autocomplete"
    s.summary = ""
    s.description = "A Rails plugin encapsulating autocompletion of HTML text input using Solr and Sunspot"
    s.homepage = "http://github.com/haitham/sunspot_autocomplete"
    s.authors = ["Haitham Mohammad"]
    s.add_dependency("sunspot_rails")
  end
rescue LoadError
  puts "Jeweler not available. Install it with: gem install jeweler"
end

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the sunspot_autocomplete plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.libs << 'test'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the sunspot_autocomplete plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'Sunspot Autocomplete'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README.rdoc')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
