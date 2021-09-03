# ml_cloud_run

- Step 1: Train ML Model and save the model file.
- Step 2: Create an endpoint for prediction and write predict function using the saved model file.
- Step 3: Create new project in https://console.cloud.google.com/
        Enable Google Cloud Run API and Cloud Build API
- Step 4: Install and init Google Cloud SDK https://cloud.google.com/sdk/docs/install
- Step 5: Create requirements.txt, Dockerfile, .dockerignore in the root folder
        Root folder contains endpoint app file, saved model file, requirements.txt, .dockerfile and Dockerfile
- Step 6: Add Dockerfile code from the documentation https://cloud.google.com/run/docs/quickstarts/build-and-deploy/python
- Step 7: Run below two commands with google cloud project id
```
gcloud builds submit --tag gcr.io/<project_id>/<function_name>
gcloud run deploy --image gcr.io/<project_id>/<function_name> --platform managed
```
