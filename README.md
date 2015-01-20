# docker-sinopia

Docker container for `sinopia` (private `npm` registry).
Stuff borrowed from [`keyvanfatehi/sinopia`](https://registry.hub.docker.com/u/keyvanfatehi/sinopia/),
but this image is based on `debian:jessie`, and avoids using too many layers.

## Usage

If you want to expose ports, use `-p 4873:4873`.

```sh
$ docker run -d \
  -v /path/to/sinopia/:/opt/sinopia/ \
  --name sinopia
  purpose/sinopia
```

`/path/to/sinopia/` should contain `config.yaml` (otherwise a default config is created).

[`purpose/sinopia-nginx`](https://registry.hub.docker.com/u/purpose/sinopia-nginx/) provides secure reverse-proxy for `sinopia`.

## License

MIT
