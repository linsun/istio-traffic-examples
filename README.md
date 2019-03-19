# istio-traffic-examples

## httpbin

`k apply -f httpbin-gateway2.yaml`

You should be able to reach:
`curl -I -HHost:httpbin2.example.com  {ingress-ip}:{port}/status/200`

In namespace default, run 
`k apply -f vs-default.yaml`

Or in namespace ns1, run
`k apply -f vs-ns1.yaml`

When either vs-default.yaml or vs-ns1.yaml is applied, you should be able to reach :

`curl -I -HHost:httpbin2.example.com  {ingress-ip}:{port}/delay/200`
