# DevOps Challenge

Fork this project and build the infrastructure of this API the way you want, you can use Docker Compose, AWS or any other way you like, the goal here is to analyze your commits to understand the way you work.

You have one week to complete the test, when you're done send an email to [anderson.lima@shawandpartners.com](mailto:anderson.lima@shawandpartners.com)
We will schedule a meeting for you to explain your solution

Tips:

The application runs on port 8888

This app only has two endpoints, the / which returns the following string:

```jsx
{"App Test": "Alive"}
```

And the Healthcheck endpoint that returns the following string:

```jsx
{"Status": "heart beating steady and strong"}
```

Run the application
```jsx
pip install -r src/requirements.txt
cd src
gunicorn --bind 0.0.0.0:8888 wsgi:app
```



Any questions please contact: [anderson.lima@shawandpartners.com](mailto:anderson.lima@shawandpartners.com)

## first solution ( google cloud plataform)
After evaluating many approaches to solve this problem I decided to deploy the API on a Kubernetes cluster using, Docker, Artifact Registry, GKE , Google Cloud Platform ( as cloud provider) and Github Actions for CI/CD.

the result can be checked by accessing the fallowing ip addresses
```jsx
http://34.27.93.29/
http://34.27.93.29/healthcheck
```

# second solution ( amazon web services)

this time I am using the same approach , but working with amazon web services (aws) as a cloud provider, the solution consistis in creating a CI/CD pipeline with Github actions, connecting  to aws using IAM roles and Identity provider for github, bulding, tagging and pushing  the image to ECR ( elastic container registry) and deploying to image to ECS ( elastic container service) cluster , so that it will be available to the internet.

the result can be checked by accessing the fallowing ip addresses
```jsx
http://52.15.210.126:8888
http://52.15.210.126:8888/healthcheck
```
contact me for further explanation: [vagneralves997@gmail.com](mailto:vagneralves997@gmail.com)
