# quadratic-equation-solver

Запуск приложения : docker-compose up (в корневой папке)

Для локального запуска нужно : 
1) Запустить soap приложение в докер контейнере : в корне soap проекта "mvn clean install", "docker build -t soap_web_app .", "docker run -p 8080:8080 soap_web_app"
2) Сгенерировать недостающие wsdl классы spring-boot приложения нажатием reload project (при этом должно быть запущено soap приложение в докер контейнере на localhost:8080)
3) Чтобы собрать spring-boot приложение в SoapClientConfig меняем soap.service.docker.url на soap.service.local.url и собираем mvn clean install
4) Запускаем spring-boot приложение из среды разработки

Пример запроса : http://localhost:8081/api/calc?a=3&b=5&c=2
