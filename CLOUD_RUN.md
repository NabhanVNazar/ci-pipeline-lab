# Cloud Run Deployment Mapping

- Registry: Docker Hub → Google Artifact Registry
- Authentication: Docker Hub secrets → Google Cloud authentication
- Push: Push the image tagged with the Git commit SHA to Artifact Registry.
- Deploy: Use `gcloud run deploy` with the published image.
- Verification: Check the Cloud Run service URL and health endpoint.

Example:

gcloud run deploy app --image REGION-docker.pkg.dev/PROJECT_ID/REPOSITORY/app:COMMIT_SHA --region REGION

Cloud Run deployment is documentation only for this assignment.