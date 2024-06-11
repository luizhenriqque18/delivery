# delivery

{"clientId":"3","routeId":"3"}

producer
route.new-position

kafka-console-producer --bootstrap-server=localhost:9092 --topic=route.new-direction

docker exec -it apache-kafka-kafka-1 kafka-console-producer --bootstrap-server=localhost:9092 --topic=route.new-direction

consumer
route.new-position

kafka-console-consumer --bootstrap-server=localhost:9092 --topic=route.new-direction

docker exec -it apache-kafka-kafka-1 kafka-console-consumer --bootstrap-server=localhost:9092 --topic=route.new-direction

consumer
route.new-direction

kafka-console-consumer --bootstrap-server=localhost:9092 --topic=route.new-position --group=terminal

docker exec -it apache-kafka-kafka-1 kafka-console-consumer --bootstrap-server=localhost:9092 --topic=route.new-position --group=terminal


docker exec -it simulator go run main.go