# sushi-delivery-system
Docker-based sushi delivery application

1. **Скачайте файл** `docker-compose.yml` на компьютер
2. **Откройте терминал** в папке с файлом
3. **Запустите систему:**
    docker-compose up -d
5. Проверьте: http://localhost:8080/api/sushi
   
   Управление:
   
docker-compose up -d - запуск

docker-compose down - остановка

docker ps - статус контейнеров

docker logs sushi-app - логи приложения

Основные команды API:
Роллы:
GET /api/sushi - все роллы
GET /api/sushi/{id} - ролл по ID
Заказы:
POST /api/orders - создать заказ
GET /api/orders - все заказы
PUT /api/orders/{id}/status - изменить статус

Пример заказа:
curl -X POST http://localhost:8080/api/orders -H "Content-Type: application/json" -d '{
  "customerName": "Иван",
  "customerPhone": "+79123456789", 
  "deliveryAddress": "ул. Тестовая, 123",
  "items": [
    {"sushi": {"id": 1}, "quantity": 2},
    {"sushi": {"id": 3}, "quantity": 1}
  ]
}'


Меню (автозагрузка):
Филадельфия (450₽) - 15 мин
Калифорния (380₽) - 12 мин
Унаги (520₽) - 18 мин
Аляска (420₽) - 14 мин
Дракон (580₽) - 20 мин
