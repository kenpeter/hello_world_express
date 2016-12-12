## Intro

This is a simple hello world app using express. It is listening at port 8002.
The app is running on http://hello.shopshop.space

## Install

* npm install
* npm install -g forever

## Start the app

* ./start.sh

## Stop the app

* ./stop.sh

## What I learned

* var express = require('express');
* app.get to match /
* app.listen to any port

* How to configure nginx with a simple app
```

server {
  listen 80;
  server_name hello.shopshop.space;

  location / {
    proxy_pass http://0.0.0.0:8002;
    include /etc/nginx/proxy_params;
  }
}

```
