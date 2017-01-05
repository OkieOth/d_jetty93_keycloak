Based on official jetty image with additional keycloak adapter files

[More information here](https://keycloak.gitbooks.io/securing-client-applications-guide/content/topics/oidc/java/jetty9-adapter.html)

Version: 0.1

Using examples:

Set DEBUG-Loglevel for jetty:
```bash
# set DEBUG-Loglevel for jetty
docker run --rm -e JAVA_OPTIONS="-Dorg.eclipse.jetty.LEVEL=DEBUG" -p 8000:8080 \
 -v /home/eiko/tmp/jettyTest:/var/lib/jetty/webapps okieoth/d_jetty9.3_keycloak2.4:0.1

# start jetty container in Debug-Mode
docker run --rm -p 8000:8080 -p 9000:9999 -e JAVA_OPTIONS="-Xdebug -agentlib:jdwp=transport=dt_socket,address=9999,server=y,suspend=n" \
 -v /home/eiko/tmp/jettyTest:/var/lib/jetty/webapps okieoth/d_jetty9.3_keycloak2.4:0.1
```


