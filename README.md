CloudSpokes API I/O Docs
=================================

Live demo:
http://spokesdocs.herokuapp.com

Created for [a CloudSpokes challenge](http://www.cloudspokes.com/challenges/1548).

## How it works

The CloudSpokes API is described in the `./public/data/apiconfig.json` and
`./public/data/cloudspokes.json` files. Everything else (client rendering,
request handling) is handled by [I/O Docs](https://github.com/mashery/iodocs) itself.

## Modifications made

There has been minor modifications made to I/O Docs (`app.js`) itself:

* The CloudSpokes API is available under `'/'` not only through `'/cloudspokes'`
* `app.address().port` was throwing exception on node 6.19, changed to `port`

## Deployment on Heroku

* Issue `heroku create [app-name] --stack cedar` in a terminal, then clone the prompted git URL
* Copy content of this repository to the empty heroku repo
* Optional: modify config.json accordingly for local development
* Create a redis-to-go add-on on the heroku website, and assign it to your new application
* `git commit -a` and `git push origin master` to push&deploy the repository on heroku
* `heroku open` will open your brand new application in a browser

## Lecense

The MIT license.
