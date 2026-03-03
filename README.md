<img width="1920" height="1080" alt="Cuplikan layar 2026-03-03 110331" src="https://github.com/user-attachments/assets/66df4b82-f4e5-4e5f-84e9-002d2c675565" />

# User API Spec

## Create User

Endpoint : POST /api/users

Request Body :

```json
{
  "name": "GoYounjung",
  "age": 27
}
```

Response Body (Success, 201) :

```json
{
  "status": "success",
  "data": {
    "id": "f096d1dd-4ae6-4526-93a3-6ea97fa646c9",
    "name": "GoYounjung",
    "age": 27
  }
}
```

Response Body (Failed) :

```json
{
  "status": "error",
  "message": "Validation failed"
}
```

---

## Get All User

Endpoint : GET /api/users

Response Body (Success, 200) :

```json
{
  "status": "success",
  "data": [
    {
      "id": "4027cbee-997a-4d52-8542-cf433887d943",
      "name": "Galang",
      "age": 21
    },
    {
      "id": "91138c16-117a-4368-bd55-ad3d258b336c",
      "name": "Kang Hyeon",
      "age": 25
    },
    {
      "id": "f096d1dd-4ae6-4526-93a3-6ea97fa646c9",
      "name": "GoYounjung",
      "age": 27
    }
  ]
}
```

Response Body (Failed) :

```json
{
  "status": "error",
  "message": "Internal server error"
}
```

---

## Get User By ID

Endpoint : GET /api/users/{id}

Example :  
GET /api/users/91138c16-117a-4368-bd55-ad3d258b336c

Response Body (Success, 200) :

```json
{
  "status": "success",
  "data": {
    "id": "91138c16-117a-4368-bd55-ad3d258b336c",
    "name": "Kang Hyeon",
    "age": 25
  }
}
```

Response Body (Failed) :

```json
{
  "status": "error",
  "message": "User not found"
}
```

---

## Update User

Endpoint : PUT /api/users/{id}

Example :  
PUT /api/users/91138c16-117a-4368-bd55-ad3d258b336c

Request Body :

```json
{
  "name": "Kang Hyeon MyIstri",
  "age": 25
}
```

Response Body (Success, 200) :

```json
{
  "status": "success",
  "data": {
    "id": "91138c16-117a-4368-bd55-ad3d258b336c",
    "name": "Kang Hyeon MyIstri",
    "age": 25
  }
}
```

Response Body (Failed) :

```json
{
  "status": "error",
  "message": "User not found"
}
```

---

## Delete User

Endpoint : DELETE /api/users/{id}

Example :  
DELETE /api/users/4027cbee-997a-4d52-8542-cf433887d943

Response Body (Success, 200) :

```json
{
  "status": "success delete user with id 4027cbee-997a-4d52-8542-cf433887d943"
}
```

Response Body (Failed) :

```json
{
  "status": "error",
  "message": "User not found"
}
```
