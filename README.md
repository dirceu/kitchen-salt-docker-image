# kitchen-salt-docker-image

Small setup used to create this [Docker image](https://hub.docker.com/r/dirceutiegs/kitchen-salt/).

## Build

```sh
bundle install --path vendor/bundle
bundle exec kitchen test
docker ps # get the container ID here
docker commit $CONTAINER_ID dirceutiegs/kitchen-salt:version-$VERSION
docker push dirceutiegs/kitchen-salt:version-$VERSION
```
