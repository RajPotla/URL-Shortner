# URL-Shortner
A short URL:   Has one long URL   This URL shortener should have a well-defined API for URLs created, including analytics of usage.  No duplicate URLs are allowed to be created.  Short links can expire at a future time or can live forever.  


Solution supporting;
   Generating a short url from a long url    
   Redirecting a short url to a long url.   
   List the number of times a short url has been accessed in the last 24 hours, past week, and all time.    
   Data persistence ( must survive computer restarts)    
   Metrics and/or logging: Implement metrics or logging for the purposes of troubleshooting and alerting. This is optional.  
   Short links can be deleted

License: http://www.gnu.org/licenses/gpl-2.0.html

Installation

1. Make sure your server meets the requirements:
    a) Optionally you can run this from your current domain or find a short domain
    b) Apache
    c) PHP
    d) MySQL
    e) Access to run SQL queries for installation
2. Download a .zip file of the PHP URL shortener script files
3. Upload the contents of the .zip file to your web server
4. Update the database info in config.php
5. Run the SQL included in shortenedurls.sql. Many people use phpMyAdmin for this, if you can’t do it yourself contact your host.
6. If you want to use the caching option, create a directory named cache with permissions 777

Using your personal URL shortener service

- To manually shorten URLs open in your web browser the location where you uploaded the files.
- To programmatically shorten URLs with PHP use the following code:
    $shortenedurl = file_get_contents('http://yourdomain.com/shorten.php?longurl=' . urlencode('http://' . $_SERVER['HTTP_HOST']  . '/' . $_SERVER['REQUEST_URI']));
