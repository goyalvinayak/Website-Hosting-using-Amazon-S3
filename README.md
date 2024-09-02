# Static Website Hosting using Amazon S3
## About Amazon S3
Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. Amazon S3 provides management features so that you can optimize, organize, and configure access to your data to meet your specific business, organizational, and compliance requirements.

Using Amazon S3, I will create two buckets:
> Bucket 1- To store files and folders related to website
>
> Bucket 2- To store Access Logs

## Creating bucket for Website and Access Logs
Bucket1 Name- gotojobweb

Bucket2 Name- gotojobaccesslogs

Turning off block all public access for bucket 1. Bucket Versioning disabled for both buckets.
![image](https://github.com/user-attachments/assets/20692012-e741-413e-9061-c5f4355b4822)

## Uploading files to bucket 1
I have used tooplate.com for a free website template.
![image](https://github.com/user-attachments/assets/48591ba9-4b9e-40c1-814b-2bb6ada27408)
After uploading files and folders, bucket will look like this- 
![image](https://github.com/user-attachments/assets/04c58c54-7481-47b0-984f-d03c6acbda76)

## Hosting Website 
To host website, first we need to make files and folders public using ACL (and unblock the public access in the permissions tab, if blocked).
![image](https://github.com/user-attachments/assets/dff5ad26-a601-4302-9f8b-32eb9a638442)
After that, we can go to static website hosting settings in properties tab and enable it-
![image](https://github.com/user-attachments/assets/89ba21bd-5112-461e-a7a1-bc1935a57ee8)
After enabling, a link will be generated which is Bucket website endpoint-
![image](https://github.com/user-attachments/assets/0b278cb2-ce58-4b6e-ba81-77bbb1b00a77)
Our website is running-
![image](https://github.com/user-attachments/assets/a114cb39-901e-42a0-b0e1-8b1a3a1fefad)

## Access Logs
To store access logs in bucket 2, we will go to server access logging settings in properties tab of bucket 1 and enable Server access logging and choosing bucket 2 `s3://gotojobweaccesslogs` as destination-
![image](https://github.com/user-attachments/assets/e0fcc8f7-c4c9-4b86-bc0b-8d9ed73ad328)
After taking sometime, logs will appear as objects in bucket 2-
![image](https://github.com/user-attachments/assets/f416e02d-1973-4e8c-927b-757850325532)




