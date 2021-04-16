# Questions and Answers System Design

The questions and answers service is designed to handle up to 10,000 RPS by catering to the corresponding section within the [front-end client codebase](https://github.com/async-anonymous/FECClient).

### Database
Implemented and seeded PostgreSQL database with over 19 million records. The database utilized indexing and aggregate table for optimaziton to ensure quick query times.

### Load Balancer
Two different iterations of load balancing were introduced to compare distribution efficiency; one being an AWS load balncer and the other, NGIX. Ultimately the AWS load balancer was executed due to superior performance.

### Server
The PostgreSQL database and load balancer connected and communicated with several Node servers.

### Deployment
Deployment was executed through 17 AWS EC2 micro-instances, consisting of 16 servers and 1 database instance, and 1 AWS load balancer.

### Engineering Team
This service and design was built by Emma Knor.
See Product Overview and Product Reviews to see engineering work by [Jim Burch](https://github.com/async-anonymous/product-overview-db) and [Dennis Arnold](https://github.com/async-anonymous/reviews-db/tree/fcdfe3d2dc492f59f982acae73a3b99bf4ed1a43).
