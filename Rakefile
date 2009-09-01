# encoding: utf-8
PROJECT_SUMMARY     = "Remarkable DataMapper: collection of matchers and macros with I18n for DataMapper"
PROJECT_DESCRIPTION = PROJECT_SUMMARY

GEM_NAME   = "remarkable_datamapper"
GEM_AUTHOR = [ "Carlos Brando", "José Valim", "Diego Carrion", "Blake Gentry" ]
GEM_EMAIL  = [ "eduardobrando@gmail.com", "jose.valim@gmail.com", "dc.rec1@gmail.com", "blakesgentry@gmail.com" ]

EXTRA_RDOC_FILES = ["README", "LICENSE", "CHANGELOG"]

require File.join(File.dirname(__FILE__), "..", "rake_helpers.rb")

########### Package && release

configure_gemspec! do |s|
  s.add_dependency('remarkable', "~> #{GEM_VERSION}")
end

########### Specs

RAILS_VERSIONS = ['2.1.2', '2.2.2', '2.3.2', '2.3.3']

desc "Run the specs under spec with supported Rails versions"
task :pre_commit do
  RAILS_VERSIONS.each do |version|
    ENV['RAILS_VERSION'] = version
    puts "\n=> #{GEM_NAME}: rake spec RAILS_VERSION=#{version}"
    Rake::Task[:spec].execute
  end
end
