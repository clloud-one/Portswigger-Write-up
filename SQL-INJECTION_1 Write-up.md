# SQL-INJECTION_1 Write-up

**SQL-инъекция (SQLi)** — это уязвимость веб-безопасности, которая позволяет злоумышленнику вмешиваться в запросы, которые приложение выполняет к своей базе данных.

**Task: To solve the lab, perform a SQL injection attack that causes the application to display one or more unreleased products.**

1. Для решения данной задачи мы должны использовать фильтры по гифтам, после чего в BurpSuite внедрить следующую инъекцию: ' OR 1=1--

' - закрывает строку

OR 1=1 - условие вегда true

-- - комментарий, все последующее будет игнорироваться

То есть, мы делаем запрос, который вернет все товары занесенные в category.

![](C:\Users\balam\AppData\Roaming\marktext\images\2025-05-19-16-40-55-image.png)

![](C:\Users\balam\AppData\Roaming\marktext\images\2025-05-19-16-37-10-image.png)



**Task: To solve the lab, perform a SQL injection attack that logs in to the application as the user. `administrator`**

Для ее решения, введем в поле логин administartor а после пропустим все остальные параметры '--

![](C:\Users\balam\AppData\Roaming\marktext\images\2025-05-19-16-45-04-image.png)

И, готово! Мы вошли под админом

![](C:\Users\balam\AppData\Roaming\marktext\images\2025-05-19-16-45-47-image.png)
