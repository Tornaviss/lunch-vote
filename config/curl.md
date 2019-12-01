### curl samples (application deployed in application context `mealvote`).
> For windows use `Git Bash`

#### get All Users
`curl -s http://localhost:8081/mealvote/admin/users --user admin@gmail.com:admin`

#### get Users 100001
`curl -s http://localhost:8081/mealvote/admin/users/100001 --user admin@gmail.com:admin`

#### get Users by email
`curl -s http://localhost:8081/mealvote/admin/users/by?email=user@yandex.ru --user admin@gmail.com:admin`

#### update Users 100000
`curl -s -X PUT -d '{"name":"updatedUser","email":"updated@gmail.com","password":"updatedPass","roles":["ROLE_USER"]}' -H 'Content-Type: application/json' http://localhost:8081/mealvote/admin/users/100000 --user admin@gmail.com:admin`

#### create Users
`curl -s -X POST -d '{"name":"newUser","email":"newUser@gmail.com","password":"newpass","roles":["ROLE_USER"]}' -H 'Content-Type:application/json;charset=UTF-8' http://localhost:8081/mealvote/admin/users --user admin@gmail.com:admin`

#### delete Users
`curl -s -X DELETE http://localhost:8081/mealvote/admin/users/100000 --user admin@gmail.com:admin`
___

#### register Profile
`curl -s -X POST -d '{"name":"newUser","email":"newUser@gmail.com","password":"newpass"}' -H 'Content-Type:application/json;charset=UTF-8' http://localhost:8081/mealvote/profile/register`

#### get Profile
`curl -s http://localhost:8081/mealvote/profile --user user@yandex.ru:password`

#### update Profile
`curl -s -X PUT -d '{"name":"updatedUser","email":"updated@gmail.com","password":"updatedPass"}' -H 'Content-Type: application/json' http://localhost:8081/mealvote/profile --user user@yandex.ru:password`

#### delete Profile
`curl -s -X DELETE http://localhost:8081/mealvote/profile --user user@yandex.ru:password`
___

#### get Choice
`curl -s http://localhost:8081/mealvote/profile/choice --user user@yandex.ru:password`

#### create Choice: choose Restaurants 100002
`curl -s -X POST http://localhost:8081/mealvote/profile/choice/100002 --user admin@gmail.com:admin`

#### update Choice: choose Restaurants 100003
`curl -s -X PUT http://localhost:8081/mealvote/profile/choice/100003 --user user@yandex.ru:password`
___

#### create Restaurants
`curl -s -X POST -d '{"name":"Genazvale&Khinkali"}' -H 'Content-Type:application/json;charset=UTF-8' http://localhost:8081/mealvote/restaurants --user admin@gmail.com:admin`

#### get Restaurants 100002
`curl -s http://localhost:8081/mealvote/restaurants/100002 --user user@yandex.ru:password`

#### get All Restaurants
`curl -s http://localhost:8081/mealvote/restaurants --user user@yandex.ru:password`

#### update Restaurants 100003
`curl -s -X PUT -d '{"id":100003,"name":"Shaurma"}' -H 'Content-Type: application/json' http://localhost:8081/mealvote/restaurants/100003 --user admin@gmail.com:admin`

#### delete Restaurants 100003
`curl -s -X DELETE http://localhost:8081/mealvote/restaurants/100003 --user admin@gmail.com:admin`
___

#### create Menus for Restaurants 100004
`curl -s -X POST -d '{"dishes":[{"name":"kartoshka","price":"300"},{"name":"kompot","price":100}]}' -H 'Content-Type:application/json;charset=UTF-8' http://localhost:8081/mealvote/restaurants/100004/menu --user admin@gmail.com:admin`

#### get Menus 100002
`curl -s http://localhost:8081/mealvote/menus/100002 --user user@yandex.ru:password`

#### update Menus 100002
`curl -s -X PUT -d '{"dishes":[{"name":"backed fork meat","price":"10000"},{"name":"red vine","price":800}]}' -H 'Content-Type: application/json' http://localhost:8081/mealvote/menus/100002 --user admin@gmail.com:admin`

#### delete Menus 100002
`curl -s -X DELETE http://localhost:8081/mealvote/menus/100002 --user admin@gmail.com:admin`

___

#### create Dishes for Menus 100002
`curl -s -X POST -d '{"name":"Toni Papperoni","price":1000}' -H 'Content-Type:application/json;charset=UTF-8' http://localhost:8081/mealvote/menus/100002/dishes --user admin@gmail.com:admin`

#### get Dishes 100005
`curl -s http://localhost:8081/mealvote/dishes/100005 --user user@yandex.ru:password`

#### get All Dishes
`curl -s http://localhost:8081/mealvote/dishes --user user@yandex.ru:password`

#### update Dishes 100006
`curl -s -X PUT -d '{"name":"updatedDish","price":100}' -H 'Content-Type: application/json' http://localhost:8081/mealvote/dishes/100006 --user admin@gmail.com:admin`

#### delete Dishes 100006
`curl -s -X DELETE http://localhost:8081/mealvote/dishes/100006 --user admin@gmail.com:admin`