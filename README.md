# React | Springboot | AWS | Github Actions

This project consists of a frontend React application deployed on S3 and a Spring Boot backend API deployed on EC2


## Deployment

##### Frontend

The frontend React application is automatically deployed to S3 using GitHub Actions. The workflow is defined in `.github/workflows/cd_react_frontend.yml`.

##### Backend

The backend Spring Boot application is built and pushed to Docker Hub then deployed to EC2 using GitHub Actions. The workflow is defined in `.github/workflows/cd_spring_backend.yml`.

---

## Frontend

The frontend React application is deployed on S3 and can be accessed here:
http://coin-fibonacci-frontend.s3-website-us-east-1.amazonaws.com/

## Backend

The backend Spring Boot API can be tested with the following endpoint:
http://34.207.129.46:8080


<br>


#### Example Request

To test the coin change API, you can send a POST request to the backend with the following JSON body:

```json
{
    "amount": 7.01,
    "denominations": [0.1, 0.5, 0.01, 1, 5, 10]
}
```

#### Example Response

The API will respond with the minimum number of coins needed to make the given amount.

```json
{
    "coins": [
        0.01,
        1.0,
        1.0,
        5.0
    ]
}
```

## Docker

The Docker image for the Spring Boot backend is available at:

gk22a/coin-fibonacci:36249c78075f7fbba6e5946bacdd433da7794f04



