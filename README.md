## Minimal Docker image with Java [![Circle CI](https://circleci.com/gh/zpaulo19/docker-java/tree/master.svg?style=shield)](https://circleci.com/gh/zpaulo19/docker-java/tree/master)

Basic [Docker](https://www.docker.com/) image to run [Java](https://www.java.com/) applications.
This is based on [Alpine Linux](http://alpinelinux.org/) to keep the size minimal (about 25% of an ubuntu-based image).

### Tags

* [`latest` or `8` or `serverjre-8`](https://github.com/zpaulo/docker-java/blob/master/serverjre/Dockerfile): Oracle Java 8 (Server JRE) [![](https://images.microbadger.com/badges/image/zpaulo/java.svg)](https://microbadger.com/images/zpaulo/java "Get your own image badge on microbadger.com")
* [`jdk-8`](https://github.com/zpaulo/docker-java/blob/master/jdk/Dockerfile): Oracle Java 8 (JDK) [![](https://images.microbadger.com/badges/image/zpaulo/java:jdk-8.svg)](https://microbadger.com/images/zpaulo/java:jdk-8 "Get your own image badge on microbadger.com")
* [`jre-8`](https://github.com/zpaulo/docker-java/blob/master/jre/Dockerfile): Oracle Java 8 (JRE) [![](https://images.microbadger.com/badges/image/zpaulo/java:jre-8.svg)](https://microbadger.com/images/zpaulo/java:jre-8 "Get your own image badge on microbadger.com")

Additionally, tags are created for each oracle release (e.g. `8u161`, `jdk-8u161` or `jre-8u161`).

Note: Sometimes Oracle releases two versions at the same time : a CPU (Critical Patch Update) with only critical bug
fixes, and a PSU (Patch Set Update) with additional "non-critical fixes". In this case, the CPU will be the default,
as [recommended by oracle](http://www.oracle.com/technetwork/java/javase/cpu-psu-explained-2331472.html).
If needed, PSU releases are still accessible, by using their specific release tag (e.g `jdk-8u162`)

### Usage

Example: 

    docker run -it --rm zpaulo/java:8 java -version
