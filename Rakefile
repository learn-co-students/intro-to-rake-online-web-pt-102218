namespace :greeting do
  desc "outputs 'hello' to the terminal"
  task :hello do
    puts "hello from Rake!"
  end

  desc "outputs 'hola de Rake' to the terminal"
  task :hola do
    puts 'hola de Rake!'
  end
end

namespace :db do
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed DB with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

task :environment do
  require_relative './config/environment.rb'
end

desc 'open pry console'
task :console => :environment do
  Pry.start
end