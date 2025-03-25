# mTLS
-------
* Istio provides two types of authentication
    - Transport Authentication (service to Service) using mTLS
    - Origin authentication (end-user authentication)
        - verifying the end user using a JSON web token (JWT)

## Mutual TLS in ISTIO
- can be turned on **without having to change the code of applications** (because of sidecar deployments)
- It provides each service with a strong identity
    - attacks like impersonation by routing DNS record will fail, because a fake application can't prove its identity using the certificate mechanism.
    - **Secures(encrypt)** service to service and enduser to service communication
    - Provides key and certificate management to **manage generation, distribution, and rotation**
    