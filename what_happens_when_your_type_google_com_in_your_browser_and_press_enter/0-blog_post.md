# What Happens When You Type `https://www.google.com` in Your Browser?

When you type `https://www.google.com` into your browser and press "Enter", a fascinating series of steps occur in the background to deliver the requested webpage. This document explains each step in detail.

---

## DNS (Domain Name System)

The browser first resolves the domain name `google.com` into an IP address. Here's how:

- **Cache Check**: The browser looks for the IP in its local cache.
- **DNS Query**: If not found, a DNS query is sent to a recursive DNS server (usually provided by your ISP).
- **Resolution**: The DNS server resolves the domain or forwards the query to an authoritative DNS server.
- **IP Address**: The resolved IP address (e.g., `172.217.7.206`) is returned to the browser.

---

## TCP/IP Connection

Once the IP address is known, the browser establishes a connection with the server using TCP/IP:

1. The client sends a `SYN` packet to the server.
2. The server responds with a `SYN-ACK` packet.
3. The client confirms with an `ACK` packet, completing the handshake.

---

## Firewalls

The request passes through firewalls:

- **Client-Side Firewall**: Ensures outgoing traffic is safe.
- **Server-Side Firewall**: Protects Google’s infrastructure from malicious activity.

---

## HTTPS/SSL

To secure communication, the browser and server use HTTPS and SSL/TLS protocols:

1. The browser verifies the server's SSL certificate.
2. Data exchanged is encrypted to prevent interception.

---

## Load Balancer

Google employs load balancers to manage traffic:

- Distributes requests across multiple servers.
- Ensures servers are not overloaded.
- Optimizes performance by routing to the nearest or healthiest server.

---

## Web Server

Once routed, the request reaches a web server:

- Handles HTTP/HTTPS requests.
- Serves static resources like HTML, CSS, and JavaScript.
- For dynamic content, passes the request to the application server.

---

## Application Server

Dynamic content requires processing by the application server:

- Executes logic to generate responses.
- Communicates with the database for necessary data.

---

## Database

The application server interacts with Google’s database to retrieve or manipulate data:

- **Scalable Architecture**: Handles billions of queries simultaneously.
- **Query Execution**: Retrieves relevant information (e.g., search results).

---

## Conclusion

The process of accessing `https://www.google.com` is a seamless integration of technologies, ensuring speed, reliability, and security. Each component—DNS, TCP/IP, firewalls, SSL, load balancers, web servers, application servers, and databases—plays a critical role in delivering the webpage.

---

### Author

Feel free to contribute or suggest improvements to this documentation!
