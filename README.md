# aws-lambda

Project - AWS Lambda

Create a Lambda function that will be triggered when a new object arrives in S3 bucket.

Follow given steps:

1. Create a simple, Maven project with Java 11
2. Add Maven dependencies:

- aws-lambda-java-core
- aws-lambda-java-events

3. Add class that will implement RequestHandler interface from was lambda java core library. 

4. Implement handleRequest method (input type: S3Event, output type: String). Inside this method implement given behavior: read object bucket name and url decoded key. Log those informations. 

5. Build your project to .jar file with Maven

6. Go to AWS Console and create S3 Bucket

7. In AWS console create a Lambda function and select permission to be able to read from S3.

8. Add a trigger to created Lambda function by selecting a bucket created in 5 step. Choose Event type: PUT so that your Lambda is triggered when a new file arrives in S3 bucket.

9. In Lambda configuration go to „Code” tab. In code source select „Upload from” -> .zip or .jar file -> Upload your project that was built in step 5.

10. In Lambda configuration in „Code” tab go to „Runtime settings”. Make sure that Handler property is set properly - it should have proper package and class name, according to what is in your Java project.

11. Now upload any file into your S3 bucket.

12. Go to „Monitor” tab in your Lambda configuration. Then open „View logs in CloudWatch”. 

13. Open recent logs, and see if you have logged details about given S3 object.

14. After solution review with the group, delete your Lambda function.
    
