### QA 

## Load Balancers
- How does load balancing contribute to Fault tolerance? What about high availability? 
    - Load balancers contribute to fault tolerence because theres not a single point of failure. It sends traffic to many different servers to contribute to fault tolerence instead of overloading one or two servers.
    - It contributes to high availability by making it accessible in other regions if they're down or in maitenence. Having multiple servers available and usable in different regions.

- Do global load balancers decrease latency for end users? Why or why not? 
    - Yes it decreases the latency, it directs the incoming traffic to various servers in different regions globally. Usually to the closest in proximity.

- What are LB health checks for? Do we always need them? Is a LB different from a reverse proxy?
    - Health checks are used to make sure the backend instances are running and handles incoming traffic. 
    - Yes, we need load balancer health checks, when a health check fails, it stops sending traffic to it and sends it to other instances.
    - Yes, a reverse proxy is different from a load balancer. A load balancer is used to evenly distribute traffic to multiple different servers. A reverse proxy is used to recieve requests and forward them to the correct backend server.

- What are LB routing rules and URL maps for? Give an example or two of them in use. 
    - Routing rules and URL maps are used to help decisions on where to send traffic based on things like the request path, domain name, etc.

- Explain what an anycast IP address is used for in the context of a global load balancer. 
    - Anycast is a networking method where multiple servers share the same IP address. When it gets sent a request, it routes them to the best available server. 

## Cloud Armor
- What does Cloud Armor offer?
    - Cloud Armor usually blocks malicious requests before it reaches servers.

- Why is it used in the first place?
    - To block malicious requests before it reaches the servers.

- What layer in the OSI model does it operate at? Why is this important and how is this firewall different from VPC firewall rules? 
    - Cloud armor is at layer 7, the application layer.
    - It's important because it enables Cloud Armor to inspect http & https requests instead of only inspecting IP addresses and ports like firewalls.

- What are rate based rules for? 
    - They're used to limit the requests a clients sends in a certain time frame. 

- What is reCAPTCHA and how does it relate to this service? 
    - It helps filter whether requests are bots or not. 

## Cloud CDN
- What are POPs used for? 
    - Points of Presence is used for helping reduce latency by recieving and sending content from a nearby server than a distant server.

- What kind of files are served with Cloud CDN?
    - Cloud CDN is usually used to serve static content for images, videos, javascript files, and documents.

- What services can be used with cloud CDN for the source of content (the origin)?
    - Cloud CDN can use several services as origins which includes, backend buckets, load balancers, instance groups, network endpoint groups.

- Does Cloud CDN help protect against any types of malicious actors or cyberattacks? Explain.
    - Cloud CDN can help take in traffic to reduce the load on servers. In turn, that can also reduce the impact of denial of service attacks.

- Should an enterprise always use cloud CDN? Why or why not? 
    - No, because it wont justify the cost of the service if the enterprise is of smaller value. If it's a big enterprise with global users & uses large amounts of data, then yes. 

- What is TTL and how does it control content “freshness”? 
    - It stands for "Time to Live". It controls how long the contents stays cached. Then the CDN checks for updates.
 



Sources: https://docs.cloud.google.com/load-balancing/docs/health-checks https://www.geeksforgeeks.org/system-design/reverse-proxy-vs-load-balancer/ https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/compute_url_map https://docs.cloud.google.com/load-balancing/docs/l7-internal/traffic-management#path_rules https://docs.cloud.google.com/load-balancing/docs/url-map-concepts
Terraform registry
Google Cloud documentation and Google Cloud Console
