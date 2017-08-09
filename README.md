## Liberty App Accelerator
This project was generated by the [Liberty app accelerator](http://ibm.biz/appaccelerator)

[![](https://img.shields.io/badge/bluemix-powered-blue.svg)](https://bluemix.net)
[![Platform](https://img.shields.io/badge/platform-java-lightgrey.svg?style=flat)](https://www.ibm.com/developerworks/learn/java/)

### Table of Contents
* [Summary](#summary)
* [Requirements](#requirements)
* [Configuration](#configuration)
* [Project contents](#project-contents)
* [Run](#run)
* [Notices](#notices)

### Summary

The Liberty App Accelerator provides a starting point for creating applications running on [WebSphere Liberty](https://developer.ibm.com/wasdev/).


### Requirements
* [Maven](https://maven.apache.org/install.html)
* Java 8: Any compliant JVM should work.
  * [Java 8 JDK from Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
  * [Java 8 JDK from IBM (AIX, Linux, z/OS, IBM i)](http://www.ibm.com/developerworks/java/jdk/),
    or [Download a Liberty server package](https://developer.ibm.com/assets/wasdev/#filter/assetTypeFilters=PRODUCT)
    that contains the IBM JDK (Windows, Linux)

### Configuration
The application is configured to provide various technologies and features. These capabilities are provided through dependencies in the pom.xml file and Liberty features enabled in the server config file found in `src/main/liberty/config/server.xml`.

### Project contents
The context root is set in the `src/main/webapp/WEB-INF/ibm-web-ext.xml` file. The ports are set in the pom.xml file.   

* **REST** : Inside the project there is a application.rest package containing the `LibertyRestEndpoint` class. This adds a REST endpoint which you can access at `http://localhost:9080/<context>/rest`. There is also a test class named `it.rest.LibertyRestEndpointTest` that will test the REST endpoint to ensure it is working. For the complete feature documentation, see the [jaxrs-2.0](http://www.ibm.com/support/knowledgecenter/en/SSEQTP_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/rwlp_feature_jaxrs-2.0.html) feature description in IBM Knowledge Center. 

* **Servlet** : Inside the project there is a application.servlet package containing the `LibertyServlet` class. This adds a servlet with an endpoint which you can access at `http://localhost:9080/<context>/servlet`. There is also a test named `it.servlet.LibertyServletTest` that will test the servlet's endpoint to ensure it is working. For the complete feature documentation, see the [servlet-3.1](http://www.ibm.com/support/knowledgecenter/en/SSEQTP_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/rwlp_feature_servlet-3.1.html) feature description in IBM Knowledge Center. 

* **Springboot** : Inside the project there is a application.springboot.web package containing two classes:
    * `SpringBootLibertyApplication`: The entry point for the SpringBoot application.
    * `LibertyHelloController`: A Spring REST endpoint which you can access at `http://localhost:9080/<context>/springbootweb`

There is also a test class named `it.springboot.web.HelloControllerTest` that will test the Spring REST endpoint to ensure it is working.    
### Run

To build and run the application:
1. `mvn install`
1. `mvn liberty:run-server`
 

### Endpoints

The context root is set in the `src/main/webapp/WEB-INF/ibm-web-ext.xml` file. The ports are set in the pom.xml file.

### Notices

This project was generated using:
* generator-java v1.9.1
* java-common v2.0.6
* generator-liberty v5.1.2
