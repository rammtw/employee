## Входные данные

CSV файл со структурой сотрудников компании со следующими полями:

- ФИО сотрудника
- ФИО руководителя

Иерархия сотрудников может быть многоуровневой, например:

Руководитель №1 → Подчинённый №11 → Подчинённый №111 → Подчинённый №1111

## Необходимо

- Реализовать форму загрузки файла
- Разработать структуру БД для хранения содержимого загруженного файла с сохранением связи “руководитель → подчинённый → подчинённый”
- При загрузке файла сохранить его содержимое в БД
- Реализовать страницу для отображения списка сотрудников. Как будет отображаться иерархия остаётся на выбор реализующего
- Реализовать на странице списка всех сотрудников возможность отображения подчинённых выбранного или введенного в форму фильтрации сотрудника (из примера выше, при поиске подчинённых для №11 должна быть получена иерархия из №111 и №1111)

## Инструменты и требования

- Docker
- Nginx
- PHP 8
- Postgres или MySQL
- Symfony Framework
- Symfony Forms (для реализации формы загрузки файла и формы-фильтра для списка сотрудников)
- Любая UI-библиотека для реализации отображения формы загрузки и списка сотрудников (Symfony UX, Admin LTE, Bootstrap, и т.д.)
- Приложение должно содержать Dockerfile и собираться в виде docker-образа
- Приложение и БД должны запускаться при помощи docker-compose
