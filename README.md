# Golang Health Check
Booster demonstrating health checks and recovery using the kubernetes/openshift
`liveliness` and `readiness` probes.


# How to run
The project uses openshift s2i to build docker image. Run the following command
to build the docker image

```s2i build . centos/go-toolset-7-centos7:latest golang-health-check-app```

To start the web service, run

```docker run -p 8080:8080 golang-health-check-app```

The web service should now be accessible on `http://localhost:8080`