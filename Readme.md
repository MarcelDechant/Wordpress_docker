# WordPress Containerization

This repository serves as a guide for containerizing **WordPress** using **Docker Compose**.  
  
This Repository was created as part of my training at the **Developer Academy**.  

## Table of Contents

1. [Prerequisites](#prerequisites)  
2. [Description](#description)
 

## Prerequisites

* **Docker** 24.0.7
  * **Compose** v2.32.4 (module to install, [More Information](https://docs.docker.com/compose/))

## Description

### WordPress

[WordPress](https://wordpress.com/de/) is a content management system (CMS) that allows users to easily create, manage and publish websites and blogs - without extensive programming knowledge. It is one of the most popular CMS worldwide and powers over 40% of all websites on the Internet (as of 2023).

### Containerize WordPress

Docker offers a possible [compose.yaml](https://hub.docker.com/_/wordpress) file for the WordPress containerization. It shows that **two containers are needed**: one for the WordPress application and one for the database.  

* The compose file uses the `wordpress base-image` which is provided by the official WordPress community and already contains all the essential components to run the WordPress application:
  * slim operating system
  * Apache (web server)
  * PHP (including necessary extensions for WordPress)
  * WordPress files

* For the database-container a MySQL or **MariaDB** database is recommended. In this repository the latter is used here - the open source focused and independent alternative to MySQL. Provided and maintained by the MariaDB community there is a pre-build base-image. It contains, in addition to the necessary operating system:
  * MariaDB server
  * Basic configurations required for operation
