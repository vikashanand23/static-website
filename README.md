##**Static Website Hosting**
create s3 bucket in AWS, block public access by default
Enable static website hosting
Upload relevant files
Note: if we try to access website through s3 endpoint, it should show 403, since we have blocked public access
create cloudfront distribution, origin domain,s3 endpoint selection, origin access configure, update bucket policy, select default file, create distribution.
Now we can access website using cloudfront domain endpoint.

##**Continuous integration via AWS codepipeline and github webhooks**
create codepipeline
define execution mode(queued mode)
create new service role
select service provider(github oAuth)
mention repository and branch
select change detection options as github webhooks
create pipeline

Made some changes in my index.html, in the 2nd commit and pushed the code
changes were reflected instantly on website
if not, we can create invalidations.
