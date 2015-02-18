# This file manages Puppet module dependencies.
#
# It works a lot like Bundler. We provide some core modules by
# default. This ensures at least the ability to construct a basic
# environment.

# Shortcut for a module from GitHub's boxen organization
def github(name, *args)
  options ||= if args.last.is_a? Hash
    args.last
  else
    {}
  end

  if path = options.delete(:path)
    mod name, :path => path
  else
    version = args.first
    options[:repo] ||= "boxen/puppet-#{name}"
    mod name, version, :github_tarball => options[:repo]
  end
end

# Shortcut for a module under development
def dev(name, *args)
  mod "puppet-#{name}", :path => "#{ENV['HOME']}/src/boxen/puppet-#{name}"
end

# Includes many of our custom types and providers, as well as global
# config. Required.

github "boxen", "3.10.1"

# Support for default hiera data in modules

github "module_data", "0.0.3", :repo => "ripienaar/puppet-module-data"

# Core modules for a basic development environment. You can replace
# some/most of these if you want, but it's not recommended.

github "brewcask",    "0.0.4"
github "dnsmasq",     "2.0.1"
github "foreman",     "1.2.0"
github "gcc",         "2.2.0"
github "git",         "2.7.1"
github "go",          "2.1.0"
github "homebrew",    "1.11.2"
github "hub",         "1.3.0"
github "inifile",     "1.1.1", :repo => "puppetlabs/puppetlabs-inifile"
github "nginx",       "1.4.4"
github "nodejs",      "4.0.0"
github "openssl",     "1.0.0"
github "phantomjs",   "2.3.0"
github "pkgconfig",   "1.0.0"
github "repository",  "2.3.0"
github "ruby",        "8.1.7"
github "stdlib",      "4.2.1", :repo => "puppetlabs/puppetlabs-stdlib"
github "sudo",        "1.0.0"
github "xquartz",     "1.2.1"

# Optional/custom modules. There are tons available at
# https://github.com/boxen.

# Optional/custom modules. There are tons available at
# https://github.com/boxen.

github "alfred",            "1.4.0"
github "dropbox",           "1.4.1"
github "chrome",            "1.2.0"
github "firefox",           "1.2.3"
github "spotify",           "1.0.2"
github "onepassword",       "1.1.5"
github "osx",               "2.8.0"
github "property_list_key", "0.1.0"
github "sysctl",            "1.0.1"
github "zsh",               "1.0.0"
github "iterm2",            "1.2.4"
github "vlc",               "1.0.5"
github "postgresql",        "2.0.1"
github "mysql",             "1.99.19"
github "mysql_workbench",   "1.0.5", :repo => "freakphp/puppet-mysql_workbench"
github "hipchat",           "1.1.3"
github "skype",             "1.1.0"
github "cyberduck",         "1.0.1"
github "virtualbox",        "1.0.13"
github "vagrant",           "3.2.2"
github "vagrant_manager",   "0.0.1"
github "netbeans",          "1.0.1"
github "eclipse",           "2.5.0"
github "textmate",          "1.1.0"
github "gimp",              "1.0.1"
github "emacs",             "1.3.0"
github "groovy",                        "1.0.0", :repo => "idris/puppet-groovy"
github "intellij",          "1.5.1"
github "groovy",                        "1.0.0", :repo => "idris/puppet-groovy"
github "googledrive",		"1.0.2"
github "evernote",			"2.0.7"
github "keepassx",			"1.0.0"
github "sourcetree", 			"1.0.0"

