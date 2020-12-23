
ENC='$(echo -n '<user>:<pass>' | openssl base64 -base64)'

```
 wget --quiet \
  --method POST \
  
  --header 'Authorization: <your eCX API token key goes here>' \
  or
  --header 'Authorization:Basic ${ENC}'
  
  --header 'Content-Type: application/json' \
  
  --body-data '{"url": "http://schoolbusinessalert.space/sd/","brand": "University of South Wales","date_discovered": 1539429978,"confidence_level": 100}' \
  or 
  --body-file request-v1.json \
  
  --output-document \
  - https://api.ecrimex.net/phish
 ```
