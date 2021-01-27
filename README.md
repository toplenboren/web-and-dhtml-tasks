# Решения задач из курса «Веб и DHTML»

### Междоменное взаимодействие

Решение задачи находится в папке `crossdomain_integration`

1. Запускаем сервера на портах 3000 и 4200
2. Открываем `127.0.0.1:3000`
3. Если нажимать на кнопки, будут происходить междоменные запросы

---

### XSS атака

4200 — атакующий сервер

3000 — атакуемый сервер

Как происходит атака:

1. На страничке по адресу `[localhost:3000/form](http://localhost:3000/form)` заполняем форму, где в поле «ваше мнение» вводим атакующий скрипт и отправляем
2. Теперь как обычный пользователь заполняем форму
3. Просиходит переадресация и теперь мы видим данные, введенные ранее и мнения других пользователей, среди которых атакующий скрипт

Итог: атакующий скрипт выполняется и куки уходят

---