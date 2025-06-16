# 🚀 HealthTech Landing Page – Cloud Deployment (DigitalOcean)

This is my submission for the AltSchool Tinyuka Second Semester Cloud Engineering exam. It showcases a deployed landing page for a HealthTech startup on a **DigitalOcean Droplet**, with Nginx and GitHub integration.

---

### ✅ Project Information
🔗 Live IP: https://healthtech.duckdns.org/

🖼️ Screenshot: 

🧑‍💻 Author: Adefehinti Mary – ALT/SOE/024/2406


## 📌 Steps Completed

### 1. ✅ Created Droplet on DigitalOcean
-  **Ubuntu 20.04**
- Set up using **SSH key authentication**
- Connected via terminal using:
  ```bash
  ssh root@165.232.109.97
### 2. ✅ Installed Nginx
-Updated packages:

```bash
sudo apt update
sudo apt install nginx -y
```
-Allowed traffic:

```bash
sudo ufw allow 'Nginx Full'
```

-Visited:
http://https://healthtech.duckdns.org/ to confirm Nginx is running.

### 3. ✅ Created Landing Page
-Created HTML file at:
/var/www/healthtech/index.html
-Used Tailwind CSS via CDN for styling:
html

### 4. ✅ Node.js Setup (Optional Enhancement)
Created a Node.js app (app.js) to serve content.

Installed Node and PM2:

```bash
sudo apt install nodejs npm -y
npm install -g pm2
Started the app:
```
```bash
pm2 start app.js
```
### 5. ✅ Configured Nginx Reverse Proxy
   
-Edited config:
/etc/nginx/sites-available/healthtech

Set up proxy to forward to Node.js on port 3000.

### 6. 🌐 Domain Configuration with DuckDNS
To make the deployed web application accessible using a custom domain instead of just the IP address, I used DuckDNS, a free and simple dynamic DNS service.

Steps Taken:
Visited duckdns.org

Signed in using my GitHub account.

Created a subdomain

I chose a unique subdomain name, for example:
healthtechproject.duckdns.org

Linked the subdomain to my Droplet's public IP address

I entered the IP address of my DigitalOcean droplet in the DuckDNS dashboard under that subdomain.

Configured Nginx to use the domain

I edited the Nginx configuration file:

bash
Copy
Edit
sudo nano /etc/nginx/sites-available/default
I updated the server_name field to:

nginx
Copy
Edit
server_name healthtechproject.duckdns.org;
Restarted Nginx to apply changes:

bash
Copy
Edit
sudo systemctl restart nginx
✅ Now I can access my website via http://healthtechproject.duckdns.org



### 7. ✅ GitHub Integration
Initialized Git:

```bash
git init
git remote add origin git@github.com:nikehcodes/healthtech-exam.git
git add .
git commit -m "Initial commit"
git push -u origin main
SSH key added to GitHub to allow pushing via SSH.
```





