# jwtAuth-pernstack
Reverse proxies are typically implemented to help increase security,performance and reliability and reliabiluty.In order to better understand how a reverse proxy works and the benefit ir can provide 
Aforward proxy often called proxy server or web proxy is a server that sits in front of a group of client machinse
.When those computers make requests to sites and services on the internet the proxy server intercepts those requests and then communicates with webservers on behalf of thoese clients like a middleman
lets say name 3 computers involved in a typical forward proxy communication
A this is a user's home computer
This is a forward proxy server
This is a website'origin server where the website data is stored
difference between forward proxy and reverse proxy
forward proxy: a proxy server which sits at client sides or works as a middleman to server the req
reverese proxy: a proxy or a server which sits at server side to serve response 
# Load balancing
A popular website that gets millions of users every data may not be able to handle all of its incoming site trafffic with a single origin server
A popular website that gets millions of users every data may not be able to handle all of its incoming site traffic with a single origin server
Instead the site can be distributed among a pool of different servers all handling requests for the same site
In this case a reverse p[rxy can provide a load balancign solution which will distribute the incomso traffoc evenly amont hr different servers 
Protection from attacks
With the reverse proxy in place a website or service never needs to reveal the IP address of their origin server
This makes it much harder for attackers to leverage a targetted attack against them,such as DDoS attack,instead the attackers will only be able to target the reverse proxy such as Cloudflare's CDN which will have tighter security and more resources to fend off cyber attack
Global server load balancing
In this form of load balancing, a website can be distributed on several servers around the globe and the reverse proxy will send clients to the server that's geographically closest to them.This decreases the distance that requests and responses need to travel minimizing load times
Caching:
A reverse proxy can also cache content, resulting in faster performance For example if a user in paris visits a reverse -proxied website with web servers in Los Angeles the user mihht actualluy connect to a local reverse proxy server in Paris which will then have to commuciate wit hthr origin server in LA
# SSL encryption
Encrypting and decrypting SSL or TLS  communication for each client can be configured to decrypt all incoming request
load balancing 
Ingres
Canary Deployment
Microservices
What is Ingress
Ingress exposes HTTP and HTTPS routes from outside the cluster to services within the cluster
Traffic routing is controlled by rules defined on the Ingress resources


client -->Ingres - managed-load balancer ->
Ingress-> routing rule ->         Pod
                                   Service -
                                                pod

an Ingres may be configured 
JWT web token
Completely stateless
Three parts,Header,Data,signature
Signature encryption can be symmetrical or asymmerical
Symmtrical require same key to create JWT and validate
Asymmetrical private key create JWT public key validates
.Once stolen we can't do anything
So we must make it short-lived
But can't force users to login every 15 minutes
Need a way to get JWT evry
Need a way to get new JWT evry 15 minutes
Refresh token means the token which gets renewed every 15 minutes 
and gets encrypted token
Refresh token:

The moment we authenticate the user we generate two keys
Access token - short lived
Refresh token - long lived


