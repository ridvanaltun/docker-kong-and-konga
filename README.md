# Kong & Konga in Docker Compose

This repo based on [offical Docker Compose template for Kong](https://github.com/Kong/docker-kong).

# How to use this template

This Docker Compose template provisions a Kong container with a Postgres database, konga, plus a nginx load-balancer. After running the template, the `nginx-lb` load-balancer will be the entrypoint to Kong.

To run this template execute:

```shell
$ docker-compose up
```

To scale Kong (ie, to three instances) execute:

```shell
$ docker-compose scale kong=3
```

Kong will be available through the `nginx-lb` instance on port `8000`, and `8001`. You can customize the template with your own environment variables or datastore configuration.

Konga will be available through on port `1337`.

Kong's documentation can be found at https://docs.konghq.com/

Konga's documentation can be found at https://github.com/pantsel/konga
