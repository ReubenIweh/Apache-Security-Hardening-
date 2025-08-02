# Apache-Security-Hardening
A step-by-step guide to hardening Apache web server on Linux.

## Audience
This is designed for linux system engineers, Apache admin, Middleware Administrator, Application Support, System Analyst, or anyone working or eager to learn Hardening & Security guidelines.
Fair knowledge of Apache Web Server & UNIX command is mandatory.

This Security hardening is for Red Hat/CentOS-based Systems or any system using httpd

You require some tool to examine HTTP Headers for some of the implementation verification. There are two ways to do this.

1. Use browser inbuilt developer tools to inspect the HTTP headers. Usually, it’s under Network tab
2. Use online HTTP response header checker tool

## Table of content 
- [Checking the Apache version](#checking the apache version)
- [Remove Server Version Banner](#remove server version banner) 
- [Security Hardening Directives](#security hardening directives)
- [HTTP Request Methods](#http request methods)
- [CORS Headers](cros headers)
- [Configuring TLS for Apache](#configuring tls for apache)
- [Configuring Mod Security](#configuring mod security)
- [Performance and Request Controls](#performance and request controls)
- [Enable Apache Logging](#enable apache logging)

## checking the Apache version
On Red Hat-based systems, which use yum or dnf, run the following commands to check the running version of apache
`httpd -v`

## Remove Server Version Banner
Here you don’t want to expose what web server version you are using. Exposing version means you are helping hacker to speedy the reconnaissance 
The default configuration will expose Apache Version and OS type. To change that go to the web httpd config folder /etc/httpd/conf
