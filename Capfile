default_run_options[:pty] = true

role :app, "cardinal.stanford.edu"
role :web, "cardinal.stanford.edu"
role :db,  "cardinal.stanford.edu", :primary => true

set :user, "lreilly"
set :destination, "/afs/ir.stanford.edu/users/l/r/lreilly/WWW"
set :deploy_to, "/afs/ir.stanford.edu/users/l/r/lreilly/WWW/"

set :scm, "git"
set :repository, "git://github.com/leereilly/stanford-personal-page.git"
set :repository_cache, "git_cache"
set :deploy_via, :remote_cache

namespace :deploy do
  desc "Deploy web site"
  task :default do
    run "cd /tmp"
    run "git clone #{repository}"
    run "cp -r stanford-personal-page/* WWW/"
    run "rm -rf stanford-personal-page"
  end
end