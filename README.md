# gen-dockercfg
Simple bash script to generate a base64 encoded dockercfg for a kubernetes
docker registry secret. This is useful for when you need to create the
dockercfg code manually instead of running: `kubectl create secret docker-registry mydockercfg \ --docker-server "your-server" ...`

### Usage

```bash
$ gen-dockercfg "your-server" "the-username" "the-password" "the-email"
```

Example output:

```
.dockercfg value:
eyJodHRwczovL215LXNlcnZlci5jb20iOnsidXNlcm5hbWUiOiJteS11c2VybmFtZSIsInBhc3N3b3JkIjoibXktcGFzc3dvcmQiLCJlbWFpbCI6Im15QGVtYWlsLmNvbSIsImF1dGgiOiJiWGt0ZFhObGNtNWhiV1U2YlhrdGNHRnpjM2R2Y21RSyJ9fQo=
```


### Quick Install

```shell
curl -L https://raw.githubusercontent.com/psaia/gen-dockercfg/master/gen-dockercfg >/usr/local/bin/gen-dockercfg \
  && chmod +x /usr/local/bin/gen-dockercfg
```
