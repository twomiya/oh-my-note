#### Gem安装源替换
  gem sources --add https://gems.ruby-china.org/ --remove https://rubygems.org/ -v
  bundle config mirror.https://rubygems.org https://gems.ruby-china.org
#### 终端运行产生安全密钥
  (bundle exec) rake(rails) secret RAILS_ENV=production
  echo $SECRET_KEY_BASE
#### ubuntu 部署环境变量添加位置 ~/.bashrc
If you're on a normal Ubuntu machine just put export SECRET_KEY_BASE=" <<< output from rake secret here >>> " in your `~/.bashrc`.
Run `source ~/.bashrc` and restart the app.

#### Rails template 引用(github上的code row Url)
  rails app:template LOCATION=https://raw.githubusercontent.com/guxiaobai/oh-my-rails/master/capistrano.rb

#### AssetsPipeline预编译命令
  rake(rails) assets:precompile RAILS_ENV=production
