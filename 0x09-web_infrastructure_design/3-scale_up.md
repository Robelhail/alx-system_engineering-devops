Let me explain some specifics about this infrastructure:

I added 1 server to host the application server component. An application server is a software platform that provides the logic and functionality of an application, such as business rules, transactions, security, etc. An application server typically communicates with a web server and a database server to process requests and generate dynamic content.

I added 1 load-balancer (HAproxy) configured as cluster with the other one. A load balancer is a device or software that distributes incoming requests across multiple servers to optimize performance, availability, and scalability. HAproxy is an open source load balancer that supports various protocols, such as HTTP, TCP, and UDP. By clustering two load balancers, we can achieve high availability and failover in case one of them fails or becomes overloaded.

I split the components (web server, application server, database) with their own server. This improves the separation of concerns and modularity of the application. Each component can be developed, deployed, and scaled independently. It also improves the security and reliability of the application, as each component can be isolated and protected by firewalls and access control mechanisms.
