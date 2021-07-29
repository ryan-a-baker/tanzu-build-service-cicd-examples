# Archived Pipelines

These pipelines are in here for archived purposes.  They were done as a proof of concept but shouldn't be used other than just explorations.

## azure-pipleines-cicd

This pipeline is a full cicd pipeline that will initiate the build of an image in TBS as well as the full deploy.  This was a proof of concept to determine the easiest way to capture the image digest from TBS and pass it through to the deployment.

Ultimately, this was scraped because it does not support the "patch" part of the use case.

## azure-pipelines-cicd-devops

This pipeline builds upon azure-pipelines-cicd and adds the ability to capture webhook calls for OS updates.  This was very tricky as build of an image via a normal code commit was also triggering a webhook call.  I had to do some very interesting logic to determine if the source was a webhook, and if it was, was it from a stack deploy or a normal commit build.

This pipeline got very complicated very quickly and so it was scrapped.  It may be of use in the future to have a nice - single flow pipeline from a UI and tracking perspective.