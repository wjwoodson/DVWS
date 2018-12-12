This fork of DVWS enables:
1. Included Dockerfile/container
1. Configurable target for the websockets server: `-e DVWS_WS_HOST=mydomain.is.not.local` and `-e DVWS_WS_PORT=8081`

It is a horrible kludge of things including https://github.com/tssoffsec/docker-dvwsocket/ , https://github.com/interference-security/DVWS , and tweaks by someone who does not understand php.

To build image:
```
git clone https://github.com/wjwoodson/DVWS && cd DVWS/docker-dvwsocket
docker build . -t docker-dvws

```
and run:
```
docker run --name dvws -id --restart always -e DVWS_WS_HOST=mydomain.is.not.local -e DVWS_WS_PORT=8081 -p 80:80 -p 8081:8081 docker-dvws
```

---

# OWASP Damn Vulnerable Web Sockets (DVWS)
OWASP Damn Vulnerable Web Sockets (DVWS) is a vulnerable web application which works on web sockets for client-server communication. The flow of the application is similar to [DVWA](https://github.com/ethicalhack3r/DVWA). You will find more vulnerabilities than the ones listed in the application.

https://www.owasp.org/index.php/OWASP_Damn_Vulnerable_Web_Sockets_(DVWS)

## Screenshot
![image](https://cloud.githubusercontent.com/assets/5358495/21744843/e8e70fc4-d543-11e6-9c97-763f21b09d12.png)
