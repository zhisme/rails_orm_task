## Установка
У вас должен быть установлен либо докер, либо руби локально.
```
bundle install
```

## Задача
Необходимо реализовать аналог рельсового ORM с помощью чистого руби. Посмотрите сразу на тесты для понимания что должны возвращать объекты, чтобы придумать архитектуру.  
Есть класс `User` и для него базовый класс `ApplicationRecord`. Внутри него замокан вызов в БД под методом `self.execute_sql`. Представим, что возвращаемое значение пришло нам из базы уже в виде хеша. Дальше мы должны определить свои методы `where`, `order`, которые будут работать с полученными данными.
Необязательно делать как в rails, можно продумать свое решение. Главное, чтобы все тесты были зелеными.

## Тесты
Все тесты `user_spec.rb' должны проходить.

## Запуск
Для нативного использования 
`bundle exec rspec user_spec.rb`

Для запуска через докер
`docker run -it $(docker build -q .)`
