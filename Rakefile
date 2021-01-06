namespace :greeting do
desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

desc 'outputs hola to the terminal'
task :hola do
  puts "hola de Rake!"
end

desc 'ouputs goodbye to the terminal'
task :goodbye do
  puts "goodbye from Rake!"
end

desc 'outputs adios to the terminal'
task :adios do
  puts "adios de Rake!"
end
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do  #creating task dependency by requiring environment.rb file
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do #seed data from seeds.rb file within db directory
    require_relative './db/seeds.rb' 
  end
end

task :environment do
  require_relative './config/environment'
end

desc 'drop into the Pry console'
task :console => :environment do  #allow user to open Pry console after using migrate to create table (and inserted dummy data)
  Pry.start
end

