setup AWS
Our site will be hosted on S3 and served via CloudFront CDN. You will need external access to your AWS resources so it's best to setup a new IAM user with AmazonS3FullAccess and CloudFrontFullAccess policy only.

Hosting on S3
Go to S3 in your AWS account.
Create a new bucket on S3
By default your bucket is private and no one can access it so we have to configure it to make it publicly available:
Open the properties tab, click on Static Website Hosting and check Enable Website Hosting. Also fill in the path to your index and error page (you can do this later after setting up you repo).
You also have to give read access to public otherwise no one could access the bucket although static hosting is enabled. To set the access click on Permissions and Edit bucket policy and fill in the following policy but replace YOUR_BUCKET_NAME with - you wouldn't have guessed it - your bucket name
