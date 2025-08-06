# Serverless-Image-Resizer-using-AWS-S3-Lambda-Event-Triggers
# NandiniDuggineni-Serverless-Image-Upload-and-Resizer-using-AWS-S3-Lambda-Event-Triggers
In this post, I'll walk you through how I built a serverless image upload and thumbnail resizer using AWS services — Amazon S3, Lambda, and S3 Event Triggers.
Whether you're building a photo-sharing app or an internal dashboard, this pattern helps you resize images on the fly with zero manual intervention and minimal cost. 💡

🛠️ Tech Stack
Amazon S3 – Storage for original and resized images
AWS Lambda – Serverless function to resize images
S3 Event Triggers – Automatically trigger Lambda on image upload
Python + Pillow – Image processing in the Lambda function

📈 Architecture Flow
Upload Image to S3 (original bucket)
S3 Event triggers Lambda function
Lambda resizes the image using Pillow
Resized image is saved to another S3 bucket (thumbnail bucket)

🧰 Bucket Setup
Create two S3 buckets:
image-uploads-original – for raw uploads
image-thumbnails – for resized versions

Enable event notifications on the first bucket to trigger Lambda on .jpg/.png uploads.

🧪 Lambda Function Code (Python) - File has been attached.
⚙️ Permissions - File has been attached.
Attach the following permissions to your Lambda’s IAM role:

✅ Testing the Flow
Upload a .jpg or .png file to image-uploads-original.
Lambda auto-triggers, resizes the image, and stores it in image-thumbnails.
Open the thumbnail URL or view it in the AWS console.

📌 Use Cases
Social media apps
Profile picture uploaders
Product listing images

Any app that needs fast, serverless image optimization

🔚 Conclusion
This architecture is scalable, cost-effective, and completely serverless — perfect for production use with minor enhancements like file type validation, error handling, or integration with CloudFront for CDN.

If you're working on an image-heavy application, this pattern is a must-have in your AWS toolkit.

If you need step-by-step implementation, with screenshots, check out - https://nandiniduggineni.hashnode.dev/serverless-image-upload-and-resizer-using-aws-s3-lambda-and-event-triggers

💬 Let’s Connect!
Have questions or suggestions? Feel free to drop a comment or connect with me on Hashnode/LinkedIn. Happy building! 🚀

Hashnode: https://nandiniduggineni.hashnode.dev/
LinkedIn: www.linkedin.com/in/nandiniduggineni
