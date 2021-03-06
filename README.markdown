netty-tools
============

A small collection of tools useful when working with [JBoss Netty](http://www.jboss.org/netty).
The HTTP tools are useful for adding simple web features to your server.

### Included
* **HTTP File Server**<br>
 A file serving handler based on Trustin Lee's example. Supports serving from file system or class path.
* **HTTP Cache**<br>
A simple cache to be used in conjunction with the file server (see above). Will cache served files in-memory. Intended for caching smaller files.
* **HTTP Router**<br>
Simple router that can route incoming HTTP requests to different ChannelHandlers.
Supports very basic matching rules.
* **Bandwidth meter**<br>
A monitor to measure the use of bandwidth in your Netty application. Place it first in your pipeline and it will measure the size of sent/received ChannelBuffers.
* **Async WebSocket client**<br>
A WebSocket client in pure Java with Netty. Useful for integration testing. Being event-driven, it's also perfect for doing heavy load testing of WebSocket servers.
* **Thrift server support**<br>
An RPC processor for Thrift is included together with a ChannelBuffer transport.
* **Thrift client support**<br>
Transport for enabling Thrift clients to connect to remote Thrift servers through Netty. Thanks Davide Inglima!
* **Flash Policy file handling**<br>
Can detect and respond to Adobe Flash Policy file requests. When not used, it can simply remove itself providing minimal performance hit.


Netty is not a web server and these tools are quite "raw" in the HTTP sense. If you intend to do anything moderately complex, please look [elsewhere](http://jetty.codehaus.org/jetty/).
I've used it for creating small HTTP-based admin interfaces for my Netty servers. That's one use case where these tools may come in handy.

This project is used in two applications the main author is working on. First one is [Beacon Push](http://beaconpush.com), a real-time push server browsers supporting a wide array
of transports including WebSockets. And the second one is [Sonar Voice](http://sonar-api.com), which is an embeddable VoIP solution for the web/desktop/mobile with distributed voice servers.

Getting started
----------
To get up and running try one of the following:
### A) Download the binary
Get the pre-compiled JAR and put it on your class path. Easy as pie!
### B) Compile it yourself
You can also compile it yourself using Maven. Get the source code and run:

    mvn install

This will install the library in your local Maven repository.
Use the following dependency block to import:

    <dependency>
        <groupId>se.cgbystrom.netty</groupId>
        <artifactId>netty-tools</artifactId>
        <version>1.1.0</version>
    </dependency>

## Examples
As of now, please see the tests for example usage.

## Version history
* 1.1.0 - Thrift client and Flash Policy file handler
* 1.0.2 - Async WebSocket client, Thrift support + various bug fixes
* 1.0.1 - Internal version
* 1.0.0 - Initial version

## Authors

- Carl Bystr&ouml;m <http://www.pedantique.org/>
- Davide Inglima (Thrift client support)

## License

Open source licensed under the MIT license (see _LICENSE_ file for details).
