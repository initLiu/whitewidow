[![Build status](https://ci.appveyor.com/api/projects/status/o1tucilwqrvxoy80/branch/master?svg=true)](https://ci.appveyor.com/project/Ekultek/whitewidow/branch/master)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](https://github.com/Ekultek/whitewidow/blob/master/docs/LICENSE.md)

#Whitewidow
Whitewidow is an open source automated SQL vulnerability scanner, that is capable of running through a file list, or can
scrape Google for potential vulnerable websites. It allows automatic file formatting, random user agents, IP addresses, server information, multiple SQL injection syntax, and a fun environment. This program was created for learning purposes, and is intended to teach users what vulnerability looks like.

#Screenshots
[![banner credits legal new.png](https://s22.postimg.org/r4mcutbz5/banner_credits_legal_new.png)](https://postimg.org/image/c8ntn80kd/)
[![vuls_3.png](https://s11.postimg.org/bu9pwarer/vuls_3.png)](https://postimg.org/image/4r1ugolz3/)

#Download
Preferably clone repository, alternatively you can download zip and tarball [here](https://github.com/Ekultek/whitewidow/releases/tag/1.6.1)

#Usage
`ruby whitewidow.rb -h` Will print the help page

`ruby whitewidow.rb -l` Will display the legal info, can also be run in conjunction with -f or -d

`ruby whitewidow.rb -d` Will run whitewidow in default mode and scrape Google using the search queries in the lib directory

`ruby whitewidow.rb -d --banner` Will scrape Google and hide the banner

`ruby whitewidow.rb -d --random-agent` Will grab a random user agent from the YAML file. If not used will use default agent

`ruby whitewidow.rb -d --proxy 127.0.0.1:80` Proxy configuration, must use the ":"

`ruby whitewidow.rb -d --dry-run` Will do a dry run of the program, meaning it won't scan for vulnerabilities, will prompt if you want to run a scan or not

`ruby whitewidow.rb -d --dry-run --batch` Will do a dry run and not prompt you for anything, won't run a scan

`ruby whitewidow.rb -f <path/to/file>` Will run Whitewidow through a file, you will not need to provide whitewidow the
full path to the file, just provide it the paths within the whitewidow directory itself. Also you will not need a beginning
slash, example:

    - whitewidow.rb -f tmp/sites.txt #<= CORRECT
    - whitewidow.rb -f /home/users/me/whitewidow-1.0.6/tmp/sites.txt #<= INCORRECT
    
`ruby whitewidow.rb --run-x 10` Will run 10 dry runs in batch mode and display no other information (legal, banner, etc..)

`ruby whitewidow.rb -s URL` Will spider the URL and extract all the links from there, saving them to a file. Will then run the file through whitewidows file flag

#Dependencies
`gem 'mechanize'`

`gem 'nokogiri'`

`gem 'rest-client'`

To install all gem dependencies, follow the following template:

`cd whitewidow`

`bundle install`

This should install all gems needed, and will allow you to run the program without trouble.

#Contribute
Being an open source project, feel free to contribute your ideas and open pull request. You can fork it clone it do pretty
much whatever you want to do with it. For more information including copyright info please see the docs.

If you decide
to contribute to this project, your name will go in the docs under the author and credits file. It will remain there to
show that you have successfully contributed to Whitewidow. Thank you ahead of time for all contributions, this project \
wouldn't exist without your help!

<a href="https://zenhub.com"><img src="https://raw.githubusercontent.com/ZenHubIO/support/master/zenhub-badge.png"></a>
