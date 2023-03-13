# yevis-cromwell-test

```bash
# At host
$ docker run -t --rm -v /var/run/docker.sock:/var/run/docker.sock -v /tmp:/tmp ghcr.io/sapporo-wes/sapporo-service:1.4.9 bash

# Inside sapporo-container
$ docker run -t --rm -v /var/run/docker.sock:/var/run/docker.sock -v /usr/bin/docker:/usr/bin/docker -v /tmp:/tmp --entrypoint="" broadinstitute/cromwell:80 bash

# Inside cromwell container
$ docker run hello-world
```

That is:

```bash
$ docker run -t --rm -v /var/run/docker.sock:/var/run/docker.sock -v /tmp:/tmp ghcr.io/sapporo-wes/sapporo-service:1.4.9 docker run -t --rm -v /var/run/docker.sock:/var/run/docker.sock -v /usr/bin/docker:/usr/bin/docker -v /tmp:/tmp --entrypoint="" broadinstitute/cromwell:80 docker run hello-world
```

Do:

- [`./.github/workflows/ubuntu-20.yml`](./.github/workflows/ubuntu-20.yml)
- [`./.github/workflows/ubuntu-latest.yml`](./.github/workflows/ubuntu-latest.yml)
