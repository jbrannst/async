# async
1. Sign up for Confluent cloud at http://confluent.io
1. Sign up for Kong at http://konghq.com
1. Generate Kong API token. Set it.
```
export TOKEN=kpat_2yT9uYd9eJY931VNxrnKgK4zJMm9Fo3y5xbNBYt00EmAGF1od  
``` 
1. Sign up for google developer. Instructions at https://docs.konghq.com/hub/kong-inc/openid-connect/how-to/third-party/google/
1. Update the confluent.yaml with your credentials (Confluent, Google Auth) and Redirect URI (domain name)
1. Tie it all together with DecK (below)
1. Enjoy!


```
deck gateway sync --konnect-token $TOKEN --konnect-control-plane-name serverless-default --select-tag kafka  confluent.yml
```
