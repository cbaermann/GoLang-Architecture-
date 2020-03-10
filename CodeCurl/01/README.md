run program using go run main.go

through terminal you can run curl commands to interact with the program.

ex:
curl localhost:8080/register should give a 400 Bad Request 

curl -v  -XPOST -d '{"email":"test@test.com"}' should return 400 bad request, name can not be empty

curl -v  -XPOST -d '{"email":"test@test.com", "name": "BOB"}'
should return 201 created 

curl -v localhost:8080/user?email=test@test should return the query with the information associated with the given email