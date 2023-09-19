README_RUS

TimeApp - это простое веб-приложение, полностью настроенное для разработки в режиме DEV с поддержкой Hot Reload на бэкенде.

Описание

Это приложение позволяет пользователям просматривать текущее время и сохранять его для последующего доступа. Основные функции приложения включают:

- Отображение текущего времени в режиме прямого эфира на веб-сайте через Frontend.
- Возможность сохранить текущее время с помощью кнопки "Сохранить время".
- Визуальное подтверждение сохранения времени на экране.
- Хранение сохраненного времени в базе данных.

Использование

1. Откройте веб-приложение TimeApp в браузере.
2. На главной странице вы увидите текущее время в режиме прямого эфира.
3. Нажмите кнопку "Сохранить время", чтобы сохранить текущее время.
4. Сохраненное время будет отображаться на экране визуально для подтверждения.
5. Сохраненное время также будет доступно в базе данных.

Обратите внимание: Hot Reload на бэкенде включен, что позволяет вносить изменения и видеть их без необходимости пересборки контейнера. Однако на Frontend Hot Reload отключен, и для применения изменений через локальные файлы потребуется пересборка контейнера.
 Docker Setup

Для удобства развертывания приложения включены Docker-файлы и Docker Compose файлы. База данных также настроена через Docker Compose.

Запуск приложения с использованием Docker Compose

Чтобы запустить приложение в среде Docker, выполните следующие шаги:

1. Установите Docker и Docker Compose, если они не установлены.
2. Перейдите в корневую папку проекта.
3. Запустите приложение с помощью следующей команды:
4. docker-compose up


Приложение будет доступно по адресу http://localhost:3000, где "3000" - порт, указанный в Docker Compose файле.

### Доступ к базе данных

Доступ к базе данных MySQL осуществляется через [Adminer](https://www.adminer.org/), который также интегрирован в Docker Compose.

1. Для доступа к Adminer, перейдите по адресу http://localhost:8888, где "8888" - порт Adminer.
2. Используйте учетные данные, указанные в Docker Compose файле, для входа в Adminer и управления базой данных MySQL.

 Управление временем в базе данных

Вся сохраненная информация о времени будет доступна для управления через бэкэнд, который также включает базу данных. Вы можете выполнять следующие действия:

- Сохранять новое время, нажимая кнопку "Сохранить время" на Frontend (Обратите внимание, что Hot Reload на Frontend отключен и для внесения изменений нужно будет перезагрузить страницу).
- Удалять сохраненное время, если это необходимо.
- Просматривать все сохраненные временные записи в SQL-таблице для пользователей, которые нажали кнопку "Сохранить время".


README_ENG


 TimeApp

TimeApp is a simple web application, fully configured for development in DEV mode with Hot Reload support on the backend.

 Description

This application enables users to view the current time and save it for later access. The core features of the application include:

- Displaying real-time current time on the website through Frontend.
- The ability to save the current time using the "Save Time" button.
- Visual confirmation of time-saving displayed on the screen.
- Storing the saved time in a database.

 Usage

1. Open the TimeApp web application in your browser.
2. On the main page, you will see the current time in real-time.
3. Click the "Save Time" button to save the current time.
4. The saved time will be visually displayed on the screen for confirmation.
5. The saved time will also be accessible in the database.

Please note: Hot Reload on the backend is enabled, allowing you to make changes and see them without the need to rebuild the container. However, Hot Reload is disabled on the Frontend, and changes made through local files will require a container rebuild to take effect.

## Docker Setup

For easy deployment, Docker files and Docker Compose files are included. The database is also set up through Docker Compose.

### Running the Application Using Docker Compose

To run the application within a Docker environment, follow these steps:

1. Install Docker and Docker Compose if not already installed.
2.Navigate to the root folder of the project.
3. Start the application using the following command:


docker-compose up


The application will be available at http://localhost:3000, where "3000" is the port specified in the Docker Compose file.

Database Access

Access to the MySQL database is facilitated through [Adminer](https://www.adminer.org/), also integrated into Docker Compose.

1. To access Adminer, go to http://localhost:8888, where "8888" is the Adminer port.
2. Use the credentials provided in the Docker Compose file to log in to Adminer and manage the MySQL database.

Managing Time in the Database
  
All saved time information is accessible for management through the backend, which also includes the database. You can perform the following actions:

- Save new time by clicking the "Save Time" button on the Frontend (Note that Hot Reload on the Frontend is disabled, and you will need to refresh the page to see changes).
- Delete saved time when necessary.
- View all saved time records in an SQL table for users who pressed the "Save Time" button.
