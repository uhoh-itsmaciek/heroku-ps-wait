# Deprecated

This plugin has been [incorporated into the Heroku
CLI](https://github.com/heroku/cli/pull/1175) and the functionality is
now available natively as of Heroku CLI v7.21. If you have installed
it previously, you can start using the native version by uninstalling
this plugin:

```bash
heroku plugins:uninstall heroku-ps-wait
```

For historical documentation, see below.

# heroku-ps-wait

When a release is created, it may take a while for all dynos to be
running the new version. This is especially true for applications in
Heroku Private Spaces or using the common runtime preboot feature,
where dynos cycle in gradually when a new release is deployed. This
command allows you to wait until all dynos are on the latest release
version.

### Usage

`heroku ps:wait --app sushi`

This can be especially useful combined with desktop
notifications. E.g., on Ubuntu, you can use `notify-send`:

```bash
heroku ps:wait --app sushi && notify-send 'your sushi is ready!'
```

### Installation

```bash
$ heroku plugins:install heroku-ps-wait
```

#### Update

```bash
$ heroku plugins:update heroku-ps-wait
```

## THIS IS BETA SOFTWARE

Thanks for trying it out. If you find any problems, please report an
issue and include your Heroku toolbelt version and your OS version.
