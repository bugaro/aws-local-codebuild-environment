# AWS LOCAL CODEBUILD ENVIRONMENT

## Pull docker image for local build

`docker pull public.ecr.aws/codebuild/local-builds:latest`

## For test `cd` to project folder **[buildspec.yml](https://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html)** run in terminal:

`./codebuild_build.sh -i public.ecr.aws/codebuild/local-builds -a ./artifacts`

## Variables

- **`-i`** Used to specify the customer build container image."
- **`-a`** Used to specify an artifact output directory."
- **`-e`** FILE Used to specify a file containing environment variables."
- **`-c`** Use the AWS configuration and credentials from your local host. This includes ~/.aws and any AWS\_\* environment variables."
- **`-p`** Used to specify the AWS CLI Profile."
- **`-b`** FILE Used to specify a buildspec override file. Defaults to buildspec.yml in the source directory."
- **`-m`** Used to mount the source directory to the customer build container directly."

### [MORE DETAILS](https://github.com/aws/aws-codebuild-docker-images/blob/master/local_builds/codebuild_build.sh#L31)
