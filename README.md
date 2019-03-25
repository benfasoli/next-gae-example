# Next.js Google Cloud Example

This is an example of deploying a [Next.js](https://nextjs.org/) application to Google App Engine. It integrates with Google Cloud Build for triggering CI build-test-deploy triggered by new commits. This requires setting up a Google Cloud Project.

## Permissions

For cloud build to deploy a successful build result, GCP project permissions need to be modified. Navigate to **IAM & admin** in the desired GCP project and edit the built-in `<id>@cloudbuild.gserviceaccount.com` member, adding the **App Engine / App Engine Admin** role (in addition to the default **Cloud Build / Cloud Build Service Account**).

## Triggers

Triggering cloud build can be done in two ways.

1. [GCB GitHub Plugin](https://github.com/marketplace/google-cloud-build) (preferred) which enables tight build check integration with other GitHub features.
2. [GCB Triggers](https://cloud.google.com/cloud-build/docs/running-builds/automate-builds) which are well documented and more flexible to the host repository.
