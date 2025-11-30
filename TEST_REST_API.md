# Test REST API

Use the following commands to test the REST API.

## 1. Get All Accounts
```bash
curl -X GET http://localhost:8081/api/bankAccounts
```

## 2. Get Account by ID
Replace `{id}` with an actual ID from the previous response.
```bash
curl -X GET http://localhost:8081/api/bankAccounts/{id}
```

## 3. Create Account
```bash
curl -X POST http://localhost:8081/api/bankAccounts \
     -H "Content-Type: application/json" \
     -d '{
           "balance": 5000,
           "currency": "USD",
           "type": "SAVING_ACCOUNT"
         }'
```

## 4. Update Account
```bash
curl -X PUT http://localhost:8081/api/bankAccounts/{id} \
     -H "Content-Type: application/json" \
     -d '{
           "balance": 6000
         }'
```

## 5. Delete Account
```bash
curl -X DELETE http://localhost:8081/api/bankAccounts/{id}
```
