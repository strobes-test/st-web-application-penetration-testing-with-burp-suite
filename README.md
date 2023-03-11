- [Set up DVWA inside a Docker container](https://github.com/digininja/DVWA#docker-container)
```bash
docker run --rm -it -p 80:80 vulnerables/web-dvwa
```
- The `--rm` flag is there to tell the Docker Daemon to clean up the container and remove the file system after the container exits.
- `-it` is short for `--interactive` + `--tty`. When you `docker run` with this command it takes you straight inside the container.
- To make a port available to services outside of Docker, or to Docker containers which are not connected to the container's network, use the `--publish` or `-p` flag. This creates a firewall rule which maps a container port to a port on the Docker host to the outside world.
- http://localhost/setup.php -> http://localhost/login.php -> http://localhost/index.php

- Instead of `Xmx2g` in can be `Xmx1024m` (the amount of RAM memory given for this process):

```cmd 
C:\Users\You\Desktop\BurpSuite>"C:\Program Files\Java\jdk-13.0.2\bin\java.exe" -jar -Xmx2g burpsuite_pro_v2022.5.1.jar
```

Burp -> Proxy -> Intercept -> switch to 'Intercept is off'

- Configure Burp to run over HTTPS: with BurpSuite turned on, go to http://burp/ then click 'CA Certificate', save the certificate locally. In Firefox, go to `about:preference` then search for `Certificates` then click `View Certificates`. From the `Authorities` tab, click `Import`, select the certificate saved previously then check `Trust this CA to identify websites`.