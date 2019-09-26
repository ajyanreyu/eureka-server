# eureka-server
##Simple configuration:
 ```
     <dependency>
        <groupId>org.springframework.cloud</groupId>
        <artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
     </dependency>
 ```
 ```
   @SpringBootApplication
   @EnableEurekaServer
   public class EurekaServerApplication {

    public static void main(String[] args) {
        SpringApplication.run(EurekaServerApplication.class, args);
    }

  }
 ```

The main configuration property to form the cluster is eureka.client.serviceURL.defaultZone where a hostname list is specified where the registry and discovery servers are. 

 ```
    # Eureka is registered as both server and client, since the client is not going to be used we define
    # the configuration to false
    eureka:
      client:
        register-with-eureka: false
        fetch-registry: false
 ```
