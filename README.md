# quarkus
Quarkus


# Quarkus 3

(https://quarkus.io/blog/road-to-quarkus-3/)

- Jakarta EE 10
- Eclipse MicroProfile 6
- Virtual threads (loom)
- New vert,x-based gRPC server
- Hibernate ORM 6
- Extended Lifecycle
- Buildpack Support
- HTTP/3 (Quic)
- io_uring
- Reactive Streams -> java.util.concurrent.flow
                   -> Adapters for migration
- New Dev UI
- Migration Tooling


# Basic Quarkus Lab
- Quarkus concepts
- Building a Quarkus App
- Live Coding/Live Reload


https://github.com/redhat-middleware-workshops/quarkus-workshop

<!-- [https://red.ht/quakus-lab-mpa](https://quarkus.io/guides/getting-started#the-jax-rs-resources) -->

https://github.com/RedHat-Middleware-Workshops/quarkus-workshop-m1m2-labs

```
package org.acme.people.rest;

import javax.enterprise.context.ApplicationScoped;
import javax.ws.rs.GET;
import javax.ws.rs.Path;
import javax.ws.rs.PathParam;
import javax.ws.rs.Produces;
import javax.ws.rs.QueryParam;
import javax.ws.rs.core.MediaType;

import org.slf4j.Logger;
import org.slf4j.LoggerFactory;

import io.smallrye.common.annotation.NonBlocking;

@Path("/quarkus")
@ApplicationScoped
public class GreetingResource {

    public static final Logger log = LoggerFactory.getLogger(GreetingResource.class);
    @Path("/hello")
    @GET
    @Produces(MediaType.TEXT_PLAIN)
    @NonBlocking
    public String hello() {
        return "Hola!! Welcome to Quarkus!!";
    }
    @Path("/welcome")
    @GET
    @Produces(MediaType.TEXT_PLAIN)

    public String welcome(@QueryParam(value = "name")String name) {
        return "Hola! Welcome " + name + "!";
    }
}
```

<!--<img width="597" alt="image" src="https://user-images.githubusercontent.com/17950332/206992535-8937f30a-134c-4edf-86b6-c9bf1938b01d.png"> -->


- https://red.ht/idc-quarkus-study
- https://red.ht/try-quarkus
- https://code.quarkus.io
- https://red.ht/quarkus-spring-devs
- https://developers.redhat.com/e-books
