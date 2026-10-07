# AWS S3 Static Website Hosting

## Overview

This project demonstrates how to host a static website using **Amazon S3**. The website contains information about **Sahyadri College of Engineering and Management** and is hosted using Amazon S3 Static Website Hosting.

## Technologies Used

- HTML5
- CSS3
- Amazon S3

## Project Structure

```text
AWS-Static-Website/
│
├── index.html
└── README.md
```

## Implementation Steps

### 1. Create an S3 Bucket

An Amazon S3 bucket was created to store the website files.

### 2. Enable Static Website Hosting

Static website hosting was enabled from the **Properties** section of the S3 bucket.

The following configuration was used:

- **Static Website Hosting:** Enabled
- **Hosting Type:** Host a static website
- **Index Document:** `index.html`

### 3. Configure Bucket Policy

A bucket policy was configured to allow public read access to the website objects.

The policy uses the `s3:GetObject` permission so that visitors can access the website files.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::BUCKET-NAME/*"
    }
  ]
}
```

> `BUCKET-NAME` represents the S3 bucket used for the experiment.

### 4. Create the Website

An `index.html` file was created containing a simple website about Sahyadri College of Engineering and Management.

The website includes:

- College title
- About the college
- Departments
- Campus information
- Navigation links
- Basic CSS styling
- Interactive button

### 5. Upload the Website

The `index.html` file was uploaded to the S3 bucket through:

**S3 → Bucket → Objects → Upload**

### 6. Access the Website

The **S3 Bucket Website Endpoint** available under the Static Website Hosting section was opened in a web browser.

The website was successfully displayed through the S3 website endpoint.

## Result

The static website was successfully hosted using **Amazon S3** and accessed through the S3 static website endpoint.


## Conclusion

This experiment demonstrates the deployment of a simple static website using **Amazon S3 Static Website Hosting**. S3 provides a simple way to store and serve HTML, CSS, and other static website files without requiring a traditional web server.
