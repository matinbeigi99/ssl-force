How to force SSL with .htaccess
You can force an HTTPS connection on your website by adding these rules in your website's .htaccess file:

RewriteEngine On<br>
RewriteCond %{HTTPS} off<br>
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]<br>

The .htaccess file needs to be located inside the site's document root folder. If your website is in a sub folder, then the .htaccess should be placed in the corresponding sub folder.
You can create or edit the .htaccess file either via FTP, or using with the File Manager available in cPanel.
