# Pet Social BE

BackEnd for Pet Social with nodejs

## Feature

Similar Facebook but focus on Pet. Features: 
- auth
- profile
- post 
- chat

## Project Setup

```sh
npm install
```

### Migrate Database

```sh
npm run migrate
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Backend run at port
PORT=8000
API_BASE_PATH=/api
PORT_SOCKET=8001

### Example call Backend API
```sh
# Register
curl http://localhost:8000/api/auth/register \
	-H "Content-Type: application/json" \
	--request POST \
	-d '{"email":"cong@gmail.com","password":"123456Aa","confirm_password":"123456Aa"}' 

# Login
curl http://localhost:8000/api/auth/login \
	-H "Content-Type: application/json" \
	--request POST \
	-d '{"email":"cong@gmail.com","password":"123456Aa"}' 

# Get info - replace TOKEN with your token
curl http://localhost:8000/api/auth/info \
	-H "Content-Type: application/json" \
	-H "Authorization: ${TOKEN}" \
	--request GET 

```

### Run FrontEnd

[pet-social-fe](https://github.com/codegram01/pet-social-fe)
