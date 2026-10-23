````
wget -q https://raw.githubusercontent.com/kayu55/boot/main/botvpn/install.sh && chmod +x install.sh && ./install.sh
````
## Instal 2

````
wget -q https://raw.githubusercontent.com/kayu55/boot/main/botvpn/install1.sh && chmod +x install1.sh && ./install1.sh
````

## Backup

````
cat >/etc/cron.d/backup_sellvpn <<'EOF'
SHELL=/bin/sh
PATH=/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin
0 7 * * * root /usr/bin/backup_sellvpn
EOF
````

````
chmod +x /usr/bin/backup_sellvpn
````

````
chmod +x /usr/bin/sellvpn
````

````
service cron restart
````


## Auto-start on reboot
````
npm install -g pm2
````
````
pm2 start ecosystem.config.js
````
````
pm2 save && pm2 startup
````

````
pm2 startup
````
````
pm2 save
````


