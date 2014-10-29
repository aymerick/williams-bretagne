williams-bretagne
=================

Site web de l'association Williams Bretagne: <http://www.williams-bretagne.org>


Development
===========

Install tools:

    $ npm install -g grunt-cli
    $ npm install -g bower
    $ gem install bundle

Install dependencies:

    $ npm install
    $ bower install
    $ bundle install

Build the site and watch for changes:

    $ grunt -v

Browse <http://127.0.0.1:4100>

Deploy to Github Pages:

    $ rake deploy


Repository setup
================

Rename local `master` to `source`:

    $ git branch -m master source

Push `source` to remote:

    $ git push -u origin source

Delete remote `master`:

    $ git push origin :master

Create new local `gh-pages` (empty):

    $ git checkout --orphan gh-pages
    $ git rm --cached -r .
    $ echo 'Coming soon' > index.html
    $ git add index.html
    $ git commit -m "init"

Push `gh-pages` to remote:

    $ git push -u origin gh-pages

Checkout `gh-pages` in `_site` subdirectory:

    $ git clone git@github.com:aymerick/williams-bretagne.git -b gh-pages _site


References
==========

- <http://www.aymerick.com/2014/07/22/jekyll-github-pages-bower-bootstrap.html> (`master` branch is replaced by `source` branch)
