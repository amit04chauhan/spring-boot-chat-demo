# spring-boot-chat-demo
user can send message and delete

Signup API

curl --location --request POST 'http://localhost:8080/user/signUp' \
--header 'Content-Type: application/json' \
--data-raw '{
    "username" : "user4",
    "email" : "user4@test.com",
    "address" : "home4",
    "mobileNo" : "9898978740"
}'
[7:02 pm, 07/02/2022] Aditya Pandey Exm: send message

curl --location --request POST 'http://localhost:8080/chat/sendMessage' \
--header 'Content-Type: application/json' \
--data-raw '{
    "senderUserId" : "620104f67cdc376c87c59d4f",
    "receiverUserId" : "62011be1443f787b58896c6b",
    "message" : "Hi from user-3 "
}'
[7:02 pm, 07/02/2022] Aditya Pandey Exm: read message

curl --location --request GET 'http://localhost:8080/chat/readMessage?senderUserId=6200fca03a8e577e8a35f975&receiverUserId=6200fc833a8e577e8a35f974'
[7:02 pm, 07/02/2022] Aditya Pandey Exm: delete message 

curl --location --request PUT 'http://localhost:8080/chat/deleteMessage' \
--header 'Content-Type: application/json' \
--data-raw '{
    "chatId":"6201094b3123a4595c624392",
    "userStatus": 1
}'
