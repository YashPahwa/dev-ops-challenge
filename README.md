# Devops Challenge

# Assignment 1

This assignment is to create an AWS CDN for your static content website which you have to host on S3 bucket with domain name (https://devopschallenge.postfix.in)

*For Assignment 1: I have created an AWS CDN static content website which I have hosted on two S3 buckets(yash-s3-website & yash-s3-devops).*

Case A. If the user opens (https://devopschallenge.postfix.in) it should be seen "Hello, CDN origin is working fine"

*For this domain to be used, please add an A record for the same in your hosting panel which points to "54.192.166.65", which is my CloudFront domain name's "d3ss20uuge90p9.cloudfront.net" address resolution. It was working fine when tested on my domain (https://penutg.com/)*

      A.1 Create SSL in AWS(Certificate Manager) for the domain name with DNS verification and provide us CNAME record for validation
      *I have created a SSL certificate(ACM) for the same to validate it please add a CNAME record, use Name = "_21fc320b627be52cc375e6932bbd5387" with Value = "_86d962d82e59da4fc49ac4faadc23dd6.hkmpvcwbzw.acm-validations.aws"*

      A.2 This behavior object content stays in an Edge Cache at for at least 48 hours
      *I have made a custom Cache policy for the same to store the cache for 48 hours in Edge Cache.* 

Case B. If user opens (https://devopschallenge.postfix.in/devops-folder/) it should fetch from other S3 bucket and user should see "Hello, CDN 2 origin is working fine"
*This is also working fine  when tested with my domain(https://penutg.com/devops-folder/index.html)*

      B.1 This behavior header should base caching on HOST and CloudFront-Viewer-Country
      *I have made a custom Cache policy for the same to store both these headers.*

# NOTE: Please provide a CNAME record for the validation of SSL and domain to add in our DNS.
*Both have been provided above.*


# Assignment 2

We want to gather some basic statistics for our security team. They want to know the top 8 IP addresses that hit our web servers.

Your task will be the following:
Implement a script (use any language you want) to get the top 8 IP addresses out of an existing log file
Save your script with no file extension
It has to be an executable file
there is no need for using arguments
The output format will be the following:(8 lines - top saw IP addresses by the number of hits):

<ip_address><space><number_of_hits>

A real example output would look like this:

$ count

92.6.41.236 22

186.248.72.9 19

81.243.137.36 18

217.118.78.16 15

213.118.39.51 15

93.146.139.64 14

80.116.15.0 14

186.213.159.176 11

Logfile: [Click here](https://github.com/bluestacks/dev-ops-challenge/blob/master/logfile)

# NOTE: Use AWS free tier for hosting.

*For this assignment follow the below mentioned steps:*
```sh
    git clone https://github.com/YashPahwa/dev-ops-challenge.git
    cd dev-ops-challenge
    sudo ./count
```
*The above command will give the output as per the requirement stated.*
