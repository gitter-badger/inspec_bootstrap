# For CircleCI
require 'bundler/setup'

# Style tests. Rubocop
namespace :style do
  require 'rubocop/rake_task'
  desc 'RuboCop'
  RuboCop::RakeTask.new(:ruby) do |task|
    task.options = ['--display-cop-names']
  end
end

desc 'Foodcritic, Rubocop & ChefSpec'
task default: %w(style:ruby)

desc 'Circle CI Tasks'
task circleci: %w(style:ruby)
