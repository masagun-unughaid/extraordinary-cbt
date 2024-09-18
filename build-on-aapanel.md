Install AAPanel From aapanel.com
---
Activate Docker Compose and Docker Manager
Run Code in terminal 
---
### Run Ngix Proxy Manager
-----
```bash
docker run -d \
    --name=ngixproxy \
    -p 80:80 \
    -p 443:443 \
    -p 81:81 \
    -v  ./data:/data \
    -v  ./letsencrypt:/etc/letsencrypt \
    --restart unless-stopped \
    jc21/nginx-proxy-manager:latest 
```        
-----
### Runing Extraordinary-cbt
-----
```bash
docker run -d \
  --name=extraordinary-cbt \
  -p 8080:80 \
  -e MYSQL_DATABASE=database \
  -e MYSQL_USER=user \
  -e MYSQL_PASSWORD=password \
  -e MYSQL_ROOT_PASSWORD=password \
  --restart unless-stopped \
  animegasan/extraordinary-cbt:latest
```
  ----

## Web interface Setup Ngix Proxy Manager 
Visit the url `http://<IP_ADDRESS>:81` to access ngix proxy manager
Default Password :
- Email:    admin@example.com
- Password: changeme

### Web Interface Exam Extraordinary

Visit the url `http://<IP_ADDRESS>:8080` to have access to the Extraordinary CBT's web interface.

And visit the url `http://<IP_ADDRESS>:8080/admin-system` to have access to the Extraordinary CBT's web settings.

-   Default username: `admin@shellrean.com`
-   Default password: `criticalpassword`

**It's highly recommended to change the default access credentials on first start**.