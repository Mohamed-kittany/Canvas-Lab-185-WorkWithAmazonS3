# Working with Amazon S3

## Lab Overview

In this project, I created and configured an Amazon Simple Storage Service (Amazon S3) bucket to share images with an external user from a media company, mediacouser, who was hired to provide pictures of the café's products. The S3 bucket was also configured to automatically send an email notification to the administrator whenever the bucket contents were modified.

## Diagram

<img width="534" alt="Architecture" src="https://github.com/Mohamed-kittany/Canvas-Lab-185-WorkWithAmazonS3/assets/161580792/22753967-a1d5-4d61-84bb-704aea9baabb">


The diagram illustrates the component architecture of the Amazon S3 file-sharing solution and its usage flow.

## Objectives

By the end of this lab, I accomplished the following:

- Used the s3api and s3 AWS CLI commands to create and configure an S3 bucket.
- Verified write permissions for a user on an S3 bucket.
- Configured event notifications on an S3 bucket.

## Tasks Completed

### 1. Creating and Configuring an S3 Bucket

- **Created S3 Bucket**:
  - Utilized the AWS CLI `s3api` and `s3` commands to create a new S3 bucket for storing product images.

- **Configured Bucket Permissions**:
  - Set appropriate bucket policies and permissions to allow the IAM user mediacouser to add, change, or delete images from the bucket.
  - Reviewed and verified Amazon S3 permissions to ensure secure and appropriate access for each role.

### 2. Verifying Write Permissions

- **Verified User Permissions**:
  - Confirmed that the IAM user mediacouser had the necessary permissions to upload, modify, and delete objects in the S3 bucket.
  - Tested access by signing in as mediacouser and performing various actions on the bucket contents via the AWS Management Console and AWS CLI.

### 3. Configuring Event Notifications

- **Set Up SNS Topic**:
  - Created an Amazon Simple Notification Service (SNS) topic named s3NotificationTopic for sending email notifications.
  
- **Configured S3 Event Notifications**:
  - Configured the S3 bucket to send notifications to the SNS topic whenever changes were detected in the bucket contents.
  
- **Subscription to SNS Topic**:
  - Subscribed the administrator's email address to the s3NotificationTopic SNS topic to receive email notifications of any changes to the bucket contents.

### Usage Flow

1. **External User Uploads/Modifies Images**:
   - The external user (mediacouser) signs in to the AWS Management Console or uses AWS CLI to upload, change, or delete images in the S3 bucket.
   
2. **Event Detection and Notification**:
   - When changes are detected in the S3 bucket, Amazon S3 triggers an event notification.
   - The event notification is sent to the s3NotificationTopic SNS topic.
   - The administrator receives an email with the details of the changes made to the bucket contents.

## Conclusion

This project provided hands-on experience in configuring Amazon S3 for secure file sharing, managing user permissions, and setting up automated notifications for bucket events. By completing these tasks, I demonstrated my ability to effectively manage and monitor data within an AWS S3 environment.

