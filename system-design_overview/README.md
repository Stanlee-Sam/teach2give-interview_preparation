<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Understanding System Design](#understanding-system-design)
  - [What is the need for the System Design?](#what-is-the-need-for-the-system-design)
  - [Exploring Essential Design Methods in System Design](#exploring-essential-design-methods-in-system-design)
  - [Diving Deeper into System Design Concepts](#diving-deeper-into-system-design-concepts)
    - [1. Performance vs Scalability](#1-performance-vs-scalability)
    - [2. Latency vs Throughput](#2-latency-vs-throughput)
    - [3. Consistency Patterns and Availability Patterns](#3-consistency-patterns-and-availability-patterns)
    - [Advanced Concepts in System Design](#advanced-concepts-in-system-design)
      - [1. Content Delivery Network (CDN)](#1-content-delivery-network-cdn)
      - [2. Domain Name System (DNS)](#2-domain-name-system-dns)
      - [3. Caching](#3-caching)
      - [4. Proxies](#4-proxies)
    - [Components of System Design](#components-of-system-design)
      - [1. Microservices and Service Discovery](#1-microservices-and-service-discovery)
      - [2. Database Systems: RDBMS and NoSQL](#2-database-systems-rdbms-and-nosql)
      - [3. Communication Protocols](#3-communication-protocols)
    - [Approaching System Design Interview Questions](#approaching-system-design-interview-questions)
      - [Step-by-step Guide](#step-by-step-guide)
    - [Sample System Design Interview Questions and Solutions](#sample-system-design-interview-questions-and-solutions)
      - [1. How would you design a URL Shortening service similar to TinyURL?](#1-how-would-you-design-a-url-shortening-service-similar-to-tinyurl)
        - [Requirements clarification:](#requirements-clarification)
        - [Approach:](#approach)
      - [2. How would you design a Web Crawler?](#2-how-would-you-design-a-web-crawler)
        - [Approach:](#approach-1)
      - [3. How would you design Facebook and Instagram?](#3-how-would-you-design-facebook-and-instagram)
        - [Requirements:](#requirements)
        - [Approach:](#approach-2)
      - [4. How would you design the API rate limit?](#4-how-would-you-design-the-api-rate-limit)
        - [Approach:](#approach-3)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Understanding System Design

System Design is a step by step process of defining a particular software's architecture, modules, components, etc. It is vital in building scalable and reliable software.

It is essential to learn and clear all concepts of the system design. This allows you to understand the essence of system design and various concepts from the basics to advanced.

### What is the need for the System Design?

### Exploring Essential Design Methods in System Design

Some of the design methods used are:

1. **Architectural Design**
   It is the base of the system design. Describes the infrastructure, model, view, components and interaction.
   It includes client-server interaction, microservices, etc.

2. **ERD Diagram**
   Acronym for the entity-relationship diagram. It is mainly used in designing the application's database structure.

   In the ERD Diagram you can define multiple attributes for each entity. You can also connect two different schemas if a relationship exists between them.

3. **UML Diagram**
   Stands for Unified Modeling Language. It is used to prepare modeling software systems.

   It contains different diagrams like activity diagrams, class diagrams, sequence diagram, etc. to represent the different aspects of the system.

4. **Class Diagrams**
   They are used to represent the classes. Class diagram diagram can contain the class's attributes, methods and relationships between multiple classes.

   Provides an overview of the system's data and functionality.

5. **Sequence Diagrams**
   It represents the interaction between the various components of the system. It is used to model the behavior of the system

## Diving Deeper into System Design Concepts

### 1. Performance vs Scalability

**Performance:** Speed at which a website loads and responds, enhanced by mechanisms like caching.

**Scalability:** Ability to handle increased traffic by distributing load across multiple servers or increasing server capacity.

### 2. Latency vs Throughput

**Latency:** Time delay to complete a single request, crucial for applications like online gaming and live streaming.

**Throughput:** Number of operations the system can handle in a specific time, measured in megabytes per second.

### 3. Consistency Patterns and Availability Patterns

**Consistency:** Ensures all nodes in the system read the same data simultaneously.

**Availability:** Ensures each request receives a response with fresh or old data.

**Consistency Patterns:**

- **Strong Consistency:** Each request gets the most recent data.
- **Eventual Consistency:** Temporary inconsistencies resolve over time.
- **Weak Consistency:** Focuses on fast access, allowing some data freshness variability.

**Availability Patterns:**

- **Load Balancing:** Distributes requests across multiple servers.
- **Retry and Timeout Strategies:** Re-processes requests at intervals if the system fails.

### Advanced Concepts in System Design

#### 1. Content Delivery Network (CDN)

A Content Delivery Network (CDN) is a network of distributed servers that deliver web content based on the geographical location of the user, the origin of the web page, and a content delivery server. By caching content like images and data across multiple locations, CDNs reduce latency and improve load times. When a user requests a resource, the CDN routes the request to the nearest server. If the content is cached there, it's delivered immediately; otherwise, the server fetches it from the origin, caches it, and serves it to the user.

#### 2. Domain Name System (DNS)

The Domain Name System (DNS) is a hierarchical system that translates human-friendly domain names (like www.example.com) into IP addresses that computers use to identify each other on the network. This system simplifies the user experience by allowing the use of easily memorable domain names instead of numeric IP addresses.

#### 3. Caching

Caching involves storing copies of files or data in a temporary storage location so they can be accessed faster. This high-speed storage layer sits between the web application and the data source. When a request is made, the application first checks the cache. If the data is available, it is served from the cache, which speeds up the response time. If not, the data is fetched from the primary source, stored in the cache, and then served.

#### 4. Proxies

Proxies, or proxy servers, act as intermediaries between a client and the internet. When a user requests data from the internet, the proxy server handles the request and returns the data to the user. Proxies can provide benefits such as improved security, load balancing, and caching. Using a VPN (Virtual Private Network) involves changing the proxy server, allowing access to content that might be blocked by the user's primary proxy server.

### Components of System Design

#### 1. Microservices and Service Discovery

Microservices architecture involves breaking down a large application into smaller, independent services, each handling a specific functionality. This approach facilitates easier scaling and maintenance. Microservices have unique IDs and names for identification and can dynamically discover other services within the same network, aiding in scaling and load balancing.

#### 2. Database Systems: RDBMS and NoSQL

Choosing the right database system is crucial in system design:

- **RDBMS (Relational Database Management System):** These databases store data in structured table formats and use SQL for querying. They are vertically scalable but can be slower for certain operations due to their structured nature.
- **NoSQL:** These databases store data in key-value pairs, making them suitable for unstructured data. They are horizontally scalable, faster for certain operations, and support frequent changes in the data structure.

#### 3. Communication Protocols

Protocols define rules for data exchange between systems. Common protocols include:

- **HTTP/HTTPS:** Used for web communication, with HTTPS providing a secure connection.
- **TCP/IP:** Ensures reliable communication over the internet, often used in chat applications.
- **UDP:** Suitable for applications where some data loss is tolerable, like live streaming.
- **WebSockets:** Enables bi-directional, real-time communication between web applications.

### Approaching System Design Interview Questions

#### Step-by-step Guide

1. **Requirements Clarification:** Determine the functional and non-functional requirements of the application. Functional requirements involve user interactions (e.g., authentication, navigation), while non-functional requirements focus on performance metrics (e.g., scalability, low latency).
2. **Estimation of Resources:** Estimate the necessary resources for the application, such as server capacity based on expected request rates and database storage needs.
3. **System Interface Definition:** Define system interfaces, such as API endpoints, specifying what each endpoint does.
4. **Defining Data Model:** Choose the appropriate database type based on the nature of the data. Use relational databases for structured data and NoSQL for unstructured data.
5. **High-level Design:** Design the overall structure, including connections between servers, databases, clients, and third-party tools.
6. **Detailed Design:** Optimize the system for non-functional requirements, considering aspects like caching, load balancing, and failure handling.
7. **Identifying and Resolving Bottlenecks:** Identify potential bottlenecks in the design and propose solutions to address them, such as handling system failures and monitoring performance.

### Sample System Design Interview Questions and Solutions

#### 1. How would you design a URL Shortening service similar to TinyURL?

The URL shortening service allows users to shorten long URLs. Users can use the short URL instead of the long URL, and the short URL works the same as the long URL.

##### Requirements clarification:

- When you provide a long URL as input, it should return the shortened URL.
- When you click the shortened URL, it should redirect to the original URL.
- Consider handling 500 requests per second, and make the system scalable accordingly.
- Delete expired URLs.
- Track the number of clicks on the URL.

##### Approach:

You can discuss the following points:

- How you will use the REST API to communicate with the server.
- How you will handle 500 requests per second via load balancing.
- Using a relational database, as it doesn’t require horizontal scaling.
- How to design a table in the relational database to map long URLs with short URLs.
- The critical point is how to shorten the long URL by providing a unique ID to each shortened URL.

#### 2. How would you design a Web Crawler?

Web crawlers extract information from different web pages.

##### Approach:

- Discuss how to open multiple web pages in the web browser. It is important to consider how many browser windows you will open simultaneously to crawl multiple web pages. For example, opening 1000 browser windows together may cause the device to run out of memory.
- Discuss handling changes in web pages and domains dynamically.

#### 3. How would you design Facebook and Instagram?

Here, you are required to build a social media application.

##### Requirements:

- User signup/sign-in
- Allowing users to publish posts and short videos
- Followers and following features
- Direct messaging
- Showing the latest posts from their followers
- Showing trending posts in the feed

##### Approach:

- Discuss how to handle the relationship between users in the database.
- Discuss how to implement chat features, possibly by integrating third-party chat applications.
- Discuss how to implement authentication.
- Discuss algorithms to show trending or latest posts.
- Discuss handling user data in the database, as users will publish multiple posts.
- Discuss database replication to handle failures.
- Discuss data caching and load balancing.

#### 4. How would you design the API rate limit?

The API rate limiter allows one to make a particular number of API requests in a specified time. If the API request rate increases, it blocks the request for some time.

##### Approach:

- Discuss rate-limit metrics. How many maximum requests do you want to allow per second?
- Discuss how to handle multiple requests simultaneously.
- Discuss how to keep count of requests, possibly using the IP address received in the request header.
