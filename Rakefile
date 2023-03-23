require 'rake'
require 'rake/testtask'
require 'rdoc/task'
require 'bundler/gem_tasks'

desc 'Default: run unit tests.'
task :default => :test

desc 'Run all tests.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'Globalize Versioning'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('readme.rb')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
