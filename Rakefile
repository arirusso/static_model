%w[rubygems rake psych rake/clean rake/testtask fileutils].each { |f| require f }
require File.dirname(__FILE__) + '/lib/static_model'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |s|
    s.name = %q{static_model}
    s.version = StaticModel::VERSION
    s.email = %{aaron@quirkey.com}
    s.homepage = "http://github.com/quirkey/static_model"
    s.authors = ["Aaron Quint"]
    s.date = %q{2009-12-03}
    s.summary = 'ActiveRecord like functionalities for reading from YAML with a simple class implementation'
    s.description   = %q{StaticModel provides a Base class much like ActiveRecord which supports reading from a YAML file and basic associations to ActiveRecord}
    s.rubyforge_project = %q{quirkey}
    s.add_development_dependency(%q<Shoulda>, [">= 1.2.0"])
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

Rake::TestTask.new do |t|
  t.libs << "test"
  t.test_files = FileList["test/**/*_test.rb"]
  t.verbose = true
end

Dir['tasks/**/*.rake'].each { |t| load t }

task :default => :test
