# omnido.me

README

Omnidome Website is built with the following tools:

CMS: Locomotive CMS
Deployment Engine : Wagon
Template: Bootstrap

Wagon Engine is built on Ruby on Rails.

Written in Liquid & Less

How to install the development environment.

First install wagon

http://doc.locomotivecms.com/get-started/install-wagon

With Wagon installed go to the omnido.me/site folder and run the following command to serve a local instance of the site:

bundle exec wagon serve

When updating the stylesheets it is necessary to recompile the Less Source with lessc. Do so with the following command.

lessc theme.less > ../public/stylesheets/theme.css

(or if you have multiple lessc versions installed and the default isn’t working then call the newer lessc directly from the correct folder.)

Deployment

Deployment key is not in the Github Repo and should not be added. It can be found in the fileserver in the omnidome website.

to deploy to the server run the following command from the omnido.me/site folder

bundle exec wagon push production 

OR

bundle exec wagon push production —data


General Info about the site design…

The site is made of one main single page layout, which is loaded from the index.liquid page, this contains the site info, analytics and meta data for the whole Omnidome site. All subpages are made using snippets that are included within the index page.

Except for the manual page which works as a second index page with it’s own snippets included.

Manual snippets have the prefix manual- so for example manual-index.liquid

Linking pages is done with anchors, with the exception of the imprint / privacy & manual.
