# Employee JML REST API using MuleSoft

This is an Employee REST API implementated using MuleSoft ESB to Create and retrieve employee(s) data from back systems like Database, Salesforce etc.


## API Reference

#### Create Employee

```http
  POST /api/accounts
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `authorization` | `string` | **Required**. authorization Credentials like Client Id and Client Secret |
| `X-Correlation-Id` | `string` | **Required**. 16 didgits UUID |
| `content-type` | `string` | **Required**. Application/json |

#### Get all Employess

```http
  GET /api/accounts
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `authorization` | `string` | **Required**. authorization Credentials like Client Id and Client Secret |
| `X-Correlation-Id` | `string` | **Required**. 16 didgits UUID |

#### Get Employee

```http
  GET /api/accounts/${empId}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `empId`      | `string` | **Required**. Employee Id to fetch respective employee data |

## Authors

- [@sudharshankatha](https://github.com/KathaSudharshan)


## Tech Stack

**Client:** MuleSoft

**Server:** MuleSoft CloudHub Runtime Manager


## Run Locally

Go to the project directory and open command promt run the below command to create a build(JAR) file

```bash
  mvn clean install
```
Open MuleSoft Cloudhub Runtime Manger and select environment. Follow below steps
```bash
  1. Click on "Deploy Application"
  2. provide application name as "employee-jml-api-v1"
  3. Select deployable JAR from local machine and click on upload file.
  4. Runtime manager automatically selects vCore and Workers which required for application to be created in VM
  5. Click on START and wait for a while application deploying
  6. once deployed your applocatuin status shows as green like below snapshot.
  
```


