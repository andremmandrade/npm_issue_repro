# npm_issue_repro
Yamls for reproduce the NPM issue

Azure NPM isn’t blocking traffic going to the load balancer EXTERNAL-IP unless the service externalTrafficPolicy is set to Local, starting to forward the client IP address instead of node IP address.


The desired scenario is quite simple:

Any ingress traffic coming from anywhere other than “source” namespace AND pod labeled as “app=niginx” must be blocked.
