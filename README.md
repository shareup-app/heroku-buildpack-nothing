Heroku Buildpack for Nothing
============================

This is a [Heroku Buildpack](http://devcenter.heroku.com/articles/buildpacks) for nothing.

## Usage

Assuming you have everything you need inside your repo as linux binaries or shell scripts, then:

```sh
$ heroku create --buildpack https://github.com/shareup-app/heroku-buildpack-nothing.git
$ git push heroku master
```

The buildpack will always detect as `true` any repo.

## Why?

If you have a binary and you simply want to run it on heroku to benefit from the load balancing, free SSL, etc but there is no compile step necessary, then this "nothing" buildpack will detect your app and let it continue through the slug and release processes.
