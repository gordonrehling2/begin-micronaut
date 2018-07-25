# begin-micronaut

First play with micronaut

# Groovy

Create and run a groovy app
```
$ mn create-app hello-world --lang groovy
$ cd hello-world-groovy
$ ./gradlew run
```
In a browser go to
```http://localhost:8080/hello/John```
[Read more...](https://docs.micronaut.io/latest/guide/index.html#groovy)

# Java
Create and run a Java app
```
$ mn create-app hello-world
$ cd hello-world
$ ./gradlew run
```
In a browser go to
```http://localhost:8080/hello/John```
[Read more...](https://docs.micronaut.io/latest/guide/index.html#creatingServer)

# When working behind a proxy

## Java
```
JAVA_FLAGS=-Dhttp.proxyHost=10.0.0.100 -Dhttp.proxyPort=8800
java ${JAVA_FLAGS} ...
```

Non Proxy Hosts
```
-Dhttp.nonProxyHosts="localhost|127.0.0.1|10.*.*.*|*.foo.com‌​|etc"
```
[Read more...](https://stackoverflow.com/questions/120797/how-do-i-set-the-proxy-to-be-used-by-the-jvm)

##Gradle

Create 
```
~/.gradle/gradle.properties
```

containing
```
systemProp.http.proxyHost=YourProxyHost
systemProp.http.proxyPort=8080
systemProp.http.proxyUser=YourDomainUserID
systemProp.http.proxyPassword=YourDomainPassword
systemProp.http.nonProxyHosts=localhost,127.0.0.1,.others
systemProp.https.proxyHost=YourProxyHost
systemProp.https.proxyPort=8080
systemProp.https.proxyUser=YourDomainUserID
systemProp.https.proxyPassword=YourDomainPassword
systemProp.https.nonProxyHosts=localhost,127.0.0.1,.others
```
[Read more...](https://stackoverflow.com/questions/5991194/gradle-proxy-configuration)

