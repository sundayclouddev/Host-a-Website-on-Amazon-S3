# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** Sunday Obikoya  
**Email:** princelyob@gmail.com

---

![Image](http://learn.nextwork.org/loving_pink_serene_kea/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to use Amazon S3 to host a static website. My goal is to gain hands-on experience with AWS cloud services and understand how they can be used not only for object storage but also for hosting websites.

### Tools and concepts

The key service I used in this project was Amazon S3. Hosting a static website, I learned several concepts, including how bucket policies work, the role of the index.html file, how bucket endpoints and URLs function, and how ACLs control access to ob

### Time, challenges, and wins

This project took me less than an hour to complete. The most challenging part was fixing the “403 Forbidden” error, but the most rewarding moment was seeing my static website become live and publicly accessible.

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will open Amazon S3 and create a storage bucket where I can upload and manage the files for my website.

### How long it took to create the bucket

Creating an S3 bucket took me few minutes. 

### Region selection

The Region I picked for my S3 bucket was us-east-1 because is the region closet to me. It is best practise to pick a region closet to us to save cost and for low latency

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means no two  S3 buckets can share the same name at the same time, once a name is taken, it cannot be used again unless the original bucket is deleted.

![Image](http://learn.nextwork.org/loving_pink_serene_kea/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will upload the website files into my S3 bucket, because with this files I can host my website.

### Files I uploaded

I uploaded two files to my S3 bucket: the index.html file and a folder containing all the files and images needed for my static website.

### How the files work together

Both files are necesssry because they work together to create the website. The index.html file is the main page the browser loads, while the folder contains images, and other resources that enhance the appearance and functionality of the website.

![Image](http://learn.nextwork.org/loving_pink_serene_kea/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will make my static website public, also known as enabling website hosting—because without this step, the site cannot be accessed by anyone online.

### Understanding website hosting

Website hosting means storing our website files on a web server, a computer designed to serve these files as web pages that can be accessed online.

### How I enabled website hosting

To enable website hosting for my S3 bucket, I opened the Properties tab, enabled the Static Website Hosting, and set index.html as the index document—the main file I want the site to load.

### Access Control Lists (ACLs)

An Access Control List (ACL) is a permissions system used in Amazon S3 to control access to buckets and its objects. It allows you to specify which AWS accounts or predefined groups can read or write to a bucket or object. 

![Image](http://learn.nextwork.org/loving_pink_serene_kea/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website hosting is enabled, S3 generates a bucket endpoint URL. This URL allows the public to access the bucket and its objects as a webpage.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw an “403 Forbidden” error because, although the bucket had public access, the objects were private by default and restricted by ACL settings which needed to be managed seperately to make the public.


![Image](http://learn.nextwork.org/loving_pink_serene_kea/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will make the objects in my bucket public, allowing everyone to view the content of my static website and making the site officially live and accessible on the internet.

### How I resolved the 403 error

To resolve this 403 Forbidden error, I followed three basic steps: Step 1: I ensured S3 Block Public Access settings is public. Step 2: Add a bucket policy that allowed my S3 bucket publicly accessible. Step 3: Object access control lists was public.

![Image](http://learn.nextwork.org/loving_pink_serene_kea/uploads/aws-host-a-website-on-s3_5d4474f9)

---


---
