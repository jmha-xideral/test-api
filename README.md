## Deployment

To deploy this api run

```bash
  yarn dev
```
o
```bash
  npm run dev
```

## API Reference

#### Areas

```http
  GET /areas
  GET /areas/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |

#### Employees

```http
  GET  /employees
  GET  /employees/${id}
  POST /employees
  PUT  /employees/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |

Example json

```json
  {
    "id": "1",
    "empName": "name",
    "empFirstName": "first name",
    "empLastName": "last name",
    "empBirthDate": "14-02-2024",
    "empSystemAccess": false
  }
```

#### Users

```http
  GET    /users
  GET    /users/${id}
  POST   /users
  PUT    /users/${id}
  DELETE /users/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |

Example json

```json
  {
    "id": "1",
    "employeeId": "1",
    "usrEmail": "user@mail.com",
    "usrName": "userName",
    "usrPassword": "12r1sd23r",
    "usrAreas": ["1","2"]
  }
```

#### Users with employee object

```http
  GET /users?_embed=employee
  GET /users/${id}?_embed=employee
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |
