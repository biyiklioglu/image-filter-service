# Orhan Bıyıklıoğlu Submission Notes

- :ballot_box_with_check: Created git repository with Udacity starter code
- :ballot_box_with_check: Created dev brach
- :ballot_box_with_check: npm run dev runs local instance of the server with no errors
- :ballot_box_with_check: implemented /filteredimage/ endpoint in src/server.ts and works as expected
- :ballot_box_with_check: Successful responses return HTTP 200, errors return HTTP 400 or 422
- :ballot_box_with_check: npm run build creates the application archive for deployment
- :ballot_box_with_check: Created and deployed Elastic Beanstalk application
- :ballot_box_with_check: Added Elastic Beanstalk application dashboard screenshot
- :ballot_box_with_check: Merged all changes from dev to master branch
- :ballot_box_with_check: Elastic Beanstalk application endpoint URL: [http://tcobiyiklioglu-image-filter-service-dev.eu-central-1.elasticbeanstalk.com/](http://tcobiyiklioglu-image-filter-service-dev.eu-central-1.elasticbeanstalk.com/)
- :ballot_box_with_check: Elastic Beanstalk application call example: [Wikimedia Golden tabby and white kitten n01.jpg](http://tcobiyiklioglu-image-filter-service-dev.eu-central-1.elasticbeanstalk.com/filteredimage?image_url=https://upload.wikimedia.org/wikipedia/commons/b/bd/Golden_tabby_and_white_kitten_n01.jpg)

# Udagram Image Filtering Microservice

Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

The project is split into three parts:
1. [The Simple Frontend](https://github.com/udacity/cloud-developer/tree/master/course-02/exercises/udacity-c2-frontend)
A basic Ionic client web application which consumes the RestAPI Backend. [Covered in the course]
2. [The RestAPI Backend](https://github.com/udacity/cloud-developer/tree/master/course-02/exercises/udacity-c2-restapi), a Node-Express server which can be deployed to a cloud service. [Covered in the course]
3. [The Image Filtering Microservice](https://github.com/udacity/cloud-developer/tree/master/course-02/project/image-filter-starter-code), the final project for the course. It is a Node-Express application which runs a simple script to process images. [Your assignment]

## Tasks

### Setup Node Environment

You'll need to create a new node server. Open a new terminal within the project directory and run:

1. Initialize a new project: `npm i`
2. run the development server with `npm run dev`

### Create a new endpoint in the server.ts file

The starter code has a task for you to complete an endpoint in `./src/server.ts` which uses query parameter to download an image from a public URL, filter the image, and return the result.

We've included a few helper functions to handle some of these concepts and we're importing it for you at the top of the `./src/server.ts`  file.

```typescript
import {filterImageFromURL, deleteLocalFiles} from './util/util';
```

### Deploying your system

Follow the process described in the course to `eb init` a new application and `eb create` a new environment to deploy your image-filter service! Don't forget you can use `eb deploy` to push changes.

## Stand Out (Optional)

### Refactor the course RESTapi

If you're feeling up to it, refactor the course RESTapi to make a request to your newly provisioned image server.

### Authentication

Prevent requests without valid authentication headers.
> !!NOTE if you choose to submit this, make sure to add the token to the postman collection and export the postman collection file to your submission so we can review!

### Custom Domain Name

Add your own domain name and have it point to the running services (try adding a subdomain name to point to the processing server)
> !NOTE: Domain names are not included in AWS’ free tier and will incur a cost.
