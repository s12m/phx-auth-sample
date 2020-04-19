# AuthSample using phx_gen_auth

[phx_gen_auth](https://hex.pm/packages/phx_gen_auth)

To start your Phoenix server:

  * Setup the project with `docker-compose run --rm web mix setup`
  * Start Phoenix endpoint with `docker-compose up`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

Ready to run in production? Please [check our deployment guides](https://hexdocs.pm/phoenix/deployment.html).

## Deploying on Heroku

**WARNING: Emails are not sending!**

https://hexdocs.pm/phoenix/1.5.0-rc.0/heroku.html

Add buildpacks.

```
$ heroku buildpacks:add https://github.com/HashNuke/heroku-buildpack-elixir.git
$ heroku buildpacks:add https://github.com/gjaldon/heroku-buildpack-phoenix-static.git
```

Add postgresql addon.

```
$ heroku addons:create heroku-postgresql:hobby-dev
```

Configure `SECRET_KEY_BASE`.

```
$ docker-compose run --rm web mix phx.gen.secret | xargs -I{} heroku config:set SECRET_KEY_BASE="{}"
```

Deploy!

```
$ git push heroku master
```

## Learn more

  * Official website: https://www.phoenixframework.org/
  * Guides: https://hexdocs.pm/phoenix/overview.html
  * Docs: https://hexdocs.pm/phoenix
  * Forum: https://elixirforum.com/c/phoenix-forum
  * Source: https://github.com/phoenixframework/phoenix
