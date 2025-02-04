# Задание 6. Настройка Rate Limiting

Дано: 

Доработать его таким образом, чтобы обеспечить ограничение количества отправляемых запросов. Должно быть не более 10 запросов в минуту:

```nginx
http {
   # Настройка upstream для балансировки нагрузки
   upstream backend_servers {
       server backend1.example.com;
       server backend2.example.com;
       server backend3.example.com;
   }

   server {
       listen 80;

       location / {
           proxy_pass http://backend_servers;
       }

   }
}
```

## Решение

[nginx.conf](./nginx.conf)