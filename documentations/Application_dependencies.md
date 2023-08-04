# Application dependencies

## Dependencies

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

```

## Installation

Provision the necessary AWS services needed for running the application:

1. In AWS, provision a publicly available RDS database running Postgres with host: `htfa-database.cyu4ubsohudz.us-east-1.rds.amazonaws.com` and port: `5432`.
2. In AWS, provision a s3 bucket (`http://htfa-fe.s3-website-us-east-1.amazonaws.com/`) for hosting the uploaded files.
3. Export the ENV variables needed or use a package like [dotnev](https://www.npmjs.com/package/dotenv)/:
   
   ENV variables
   ```
    POSTGRES_USERNAME
    POSTGRES_PASSWORD
    POSTGRES_DB
    POSTGRES_HOST
    JWT_SECRET
    AWS_ACCESS_KEY_ID
    AWS_BUCKET
    AWS_DEFAULT_REGION
    AWS_PROFILE
    AWS_SECRET_ACCESS_KEY
    URL
   ```

4. From the root of the repo, navigate udagram-api folder `cd starter/udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
5. Without closing the terminal in step 1, navigate to the udagram-frontend `cd starter/udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.

## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.
