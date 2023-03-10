# microservices
Микросервисная архитектура на примере Python и gRPC.

Платформа gRPC более эффективна, чем использование обычных HTTP-запросов. 
gRPC построен на основе HTTP/2, позволяющем выполнять несколько запросов параллельно поточно-безопасным способом. 
Сообщения gRPC хранятся в бинарном виде и весят меньше, чем JSON. 
Кроме того, HTTP/2 имеет встроенное сжатие заголовков, а gRPC – встроенную поддержку потоковой передачи запросов и ответов. 
В общем, попутно мы получаем отличную инфраструктуру.

Созданы два микросервиса: recommendations, marketplace.

recommendations отвечает за составление рекомендации книг пользователю.
marketplace отвечает за отправку запроса на микросервис recommendations, а затем передача ответа клиенту. Реализован на основе Flask.

Созданы докерфайлы для каждого микросервиса, а также docker-compose для запуска сразу двух сервисов.

Проект создан по туториалу https://proglib.io/p/mikroservisnaya-arhitektura-na-primere-python-i-grpc-2021-02-12
