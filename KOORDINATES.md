# Build geoserver.war
(at `vendor/geoserver/src/web/app/target/geoserver.war`):

```shell
mvn clean install -f vendor/geoserver/src -Dmaven.test.skip=true
```

(tests are currently failing due to koordinates-applicationContext.xml)

# Build docker image

```shell
docker build -t {YOUR_TAG} .
```

# Run

```shell
docker run -it -p 80:8080 {YOUR_TAG}
```

