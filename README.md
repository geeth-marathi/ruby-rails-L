# RVM, RUBY, BUNDLER

## Install RVM

- Apt-get is to install linux packages(applications) some of the needed applications
```
sudo apt-get update
sudo apt-get install -y curl gnupg build-essential
```

- GPG includes the tools you need to use public key encryption and digital signatures on your Linux system. means it setups keys(Just like vindows activation key works differently) to install packages.
```
gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```

- curl is just like searching in browser. it brings whatever it hit on command line.

```
\curl -sSL https://get.rvm.io | bash
- "|" in above is called pipe. What pipe does is, it passes the output of left command to right command.
output of curl passed as input to command bash
- Bash is a linux shell, a cli package
```
 
- Install specific version of ruby
```
rvm install ruby --stable //stable not latest(Preferrable)
rvm install ruby-x.x.x

Note: You can install multiple versions of ruby

```

- To use specific version of ruby use below command.
```
rvm use ruby-x.x.x
```

- Then you need to know something called gemset. gemset is to group gems together.
```
rvm gemset create <gemset-name>
```

Senerio:
1. Create 2 gemsets.

```
rvm gemset create set-1
rvm gemset create set-2
```

2. Use set-1 gemset to install rails
```
(To use specific gemset use below command)
rvm gemset use set-1
```
Install some Gems
```
gem install bundler
gem install rails

gem install <gem-name>
Above command is used to install gems(gems means libraries in ruby)
```
4. To verify list of gems 
```
gem list
```

5. But set-2 keep empty don't install anything. Now, move to set-2
```
rvm gemset use set-2

(do "gem list" again)
gem list

(you won't find any gems.)
Note: what you need to understand is every project we need to maintain it's own gemset.
Note: Also try useing project name as gemset name
```
Scenerio Finished..................

- Create a new rails project
```
rails create a new project
rails new <> --db mysql

--db helps to create a project and use specfic database by default sqlite 
```

- Know about bundler (to install gems automatically)
```
bundle install 
```
Which will read all code in "Gemfile" (this file importent and is generated when you create a project using "rails new")

[Refer in rails project structure(Click here...)](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.javatpoint.com%2Fruby-on-rails-directory-structure&psig=AOvVaw3LSF_W0YhpIcTbkfQFmxtE&ust=1583940321938000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCJjo1NSbkOgCFQAAAAAdAAAAABAI)


[How to write a README(For Cheatsheet Click Here...)](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
