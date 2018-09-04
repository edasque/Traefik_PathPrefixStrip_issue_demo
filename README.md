Traefik_PathPrefixStrip_issue_demo
---

This repo was created to illustrate an issue with Traefik_PathPrefixStrip first commented on in this [PR](https://github.com/containous/traefik/pull/3631#issuecomment-412660594) and later reported in this [issue](https://github.com/containous/traefik/issues/3852).

Once you've clone the repo locally and providing you have docker installed, run: ```docker-compose up```

And notice the differences between running:
* the app directly: http://0.0.0.0:9000/ which works
* the app through traefik with a /my-app/ path: http://0.0.0.0:40080/my-app/, which works
* the app through traefik with a /my-app path: http://0.0.0.0:40080/my-app , which doesn't work for subfolders

Note that you can access traeffik dashboards via http://0.0.0.0:48080/dashboard/

This is in traefik:1.7-alpine which at the time of the reporting the issue was V1.7.0-RC3 / MAROILLES.



