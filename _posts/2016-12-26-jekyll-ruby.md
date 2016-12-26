---
layout: post
title: Set up a jekyll local environment
---

安装ruby
----
1.  gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
2.  \curl -sSL https://get.rvm.io | bash -s stable
3. source ~/.bashrc
source ~/.bash_profile
4. echo "ruby_url=https://cache.ruby-china.org/pub/ruby" > ~/.rvm/user/db
修改 RVM 的 Ruby 安装源到 Ruby China 的 Ruby 镜像服务器，这样能提高安装速度
5. rvm install 2.3.0
rvm list known


安装jekyll
---
sudo apt-get install ruby-dev
gem install minima -v "2.0.0"
gem install rdiscount
gem install Jekyll 

清除非rvm安装的ruby
---
rm -rf /usr/local/lib/ruby
rm -rf /usr/lib/ruby
rm -f /usr/local/bin/ruby
rm -f /usr/bin/ruby
rm -f /usr/local/bin/irb
rm -f /usr/bin/irb
rm -f /usr/local/bin/gem
rm -f /usr/bin/gem

Q&A
--
如果出现下面错误
/usr/lib/ruby/1.9.1/rubygems/custom_require.rb:36:in `require': cannot load such file -- mkmf (LoadError)

解决方法：sudo apt-get install ruby-dev
