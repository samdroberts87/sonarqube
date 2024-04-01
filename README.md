Because SonarQube uses an embedded Elasticsearch, make sure that your Docker host configuration complies with the Elasticsearch production mode requirements and File Descriptors configuration.

For example, on Linux, you can set the recommended values for the current session by running the following commands as root on the host:

sysctl -w vm.max_map_count=524288

sysctl -w fs.file-max=131072

ulimit -n 131072

ulimit -u 8192

Finally, you'll need to use admin admin to get into the sonarqube webserver initially. The rest is simple and it wlks you through it
