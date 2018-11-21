### 課程用API


##### 登入
- USE:  會員登入
- API:  http://18.219.254.101/api/login/
- Method: POST
- send formar:
  ```js
  admin: {
    account: "admin",
    password: "password"
  }
  ```
- receive format:
  ```json
    "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYmYiOjE1NDI3ODM0NzgsImV4cCI6MTU0Mjc4MzUzOCwiaWF0IjoxNTQyNzgzNDc4LCJuYW1lIjoi566h55CG5ZOhIiwiZW1haWwiOiJhZG1pbkBtYWlsLmNvbSIsImFjY291bnQiOiJhZG1pbiJ9.m51_xiL6So5BZv7nYYjCNGGdYQh1fm7w5B5642qlrE0"
  ```
***
- USE:  檢查帳號是否登入
- API:  http://18.219.254.101/api/login/check
- Method: POST
- send formar: No
- receive format:
  ```json
    true or false
    ```
***
##### 管理員資料
- USE:  取的全部管理員資料
- API:  http://18.219.254.101/api/admins/
- Method: GET
- send formar:No
- receive format:
  ```json
    [
        {
            "admin_id": "71d17645-7b36-45dc-a3e3-a9a6f3387e8f",
            "account": "test",
            "password": "123456",
            "name": null,
            "email": null,
            "permission": null,
            "status": null
        },...
    ]
  ```
***
- USE:  取的單一管理員資料
- API:  http://18.219.254.101/api/admins/{admin_id}
- Method: GET
- send formar:No
- receive format:
  ```json
    {
        "admin_id": "71d17645-7b36-45dc-a3e3-a9a6f3387e8f",
        "account": "test",
        "password": "123456",
        "name": null,
        "email": null,
        "permission": null,
        "status": null
    }
  ```
***
- USE:  更新管理員資料
- API:  http://18.219.254.101/api/admins/{admin_id}
- Method: PUT
- send formar:No
  ```json
    {
        "admin_id": "71d17645-7b36-45dc-a3e3-a9a6f3387e8f",
        "account": "test",
        "password": "123456",
        "name": "測試用戶",
        "email": "test@gmail.com",
        "permission": null,
        "status": null
    }
  ```
- receive format:
  ```json
    {
        "admin_id": "71d17645-7b36-45dc-a3e3-a9a6f3387e8f",
        "account": "test",
        "password": "123456",
        "name": "測試用戶",
        "email": "test@gmail.com",
        "permission": null,
        "status": null
    }
  ```
***
- USE:  新增管理員資料
- API:  http://18.219.254.101/api/admins/
- Method: POST
- Send Format:
  ```json
    {
        "account": "john",
        "password": "john566",
        "name": "約翰跑步",
        "email": "john@gmail.com",
    }
  ```
- Receive Format:
  ```json
    {
        "admin_id": "ccb53df9-682f-4c89-a2d7-4f4796a8be08",
        "account": "john",
        "password": "john566",
        "name": "約翰跑步",
        "email": "john@gmail.com",
        "permission": null,
        "status": null
    }
  ```  
***
- USE:  刪除管理員資料
- API:  http://18.219.254.101/api/admins/{admin_id}
- Method: DELETE
- Send Format: No
- Receive Format:
  ```json
    {
        "admin_id": "ccb53df9-682f-4c89-a2d7-4f4796a8be08",
        "account": "john",
        "password": "john566",
        "name": "約翰跑步",
        "email": "john@gmail.com",
        "permission": null,
        "status": null
    }
  ```  
