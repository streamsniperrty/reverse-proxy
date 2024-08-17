# NGINX Proxy Configuration

After installing Nginx, go to the configuration file in:
`etc/nginx/sites-available/default`

Then, place the code from the repo into the configuration file.

The most import lines to change are:
```
server_name eushavh.xyz;
...
location /  {
  proxy_pass http://192.168.1.162:80;
```

Assign your main page and subdomains and change the IP addresses according to your machine IP addresses. Make sure to forward the reverse proxy to port 80, not any of the other machines!!
