<h1 align="center"> Анализ логов </h1>


*Общая задача:* создать скрипт для формирования витрины на основе логов web-сайта.

*Структура проекта:*
<ul>
  <li>data/ - источник исходных данных</li>
  <li>data_marts/ - готовые витрины данных</li>
  <li>logs_analysis.ipynb - файл с исходным кодом проекта</li>
  <li>ER/ - ER диаграмма модели данных</li>
</ul>

____

## 1. Исходные данные

Данные представлены в 2-ух файлах

### access.log

*54.36.149.41 - - [22/Jan/2019:03:56:14 +0330] "GET /filter/27|13%20%D9%85%DA%AF%D8%A7%D9%BE%DB%8C%DA%A9%D8%B3%D9%84,27|%DA%A9%D9%85%D8%AA%D8%B1%20%D8%A7%D8%B2%205%20%D9%85%DA%AF%D8%A7%D9%BE%DB%8C%DA%A9%D8%B3%D9%84,p53 HTTP/1.1" 200 30577 "-" "Mozilla/5.0 (compatible; AhrefsBot/6.1; +http//ahrefs.com/robot)" "-"*

### client_hostname

client,hostname,alias_list,address_list
5.123.144.95,5.123.144.95,[Errno 1] Unknown host,
![image](https://user-images.githubusercontent.com/86725214/209540782-38e6cb77-f9dc-46ae-9111-28087ed6c085.png)


## *Задача*:

Разработать скрипт формирования витрины следующего содержания:
1.      Суррогатный ключ устройства

2.      Название устройства

3.      Количество пользователей

4.      Доля пользователей данного устройства от общего числа пользователей.

5.      Количество совершенных действий для данного устройства

6.      Доля совершенных действий с данного устройства, относительно других устройств

7.      Список из 5 самых популярных браузеров, используемых на данном устройстве различными пользователями, с указанием доли использования для данного браузера относительно остальных браузеров. 

8.      Количество ответов сервера отличных от 200 на данном устройстве

9.      Для каждого из ответов сервера, отличных от 200, сформировать поле, в котором будет содержаться количество ответов данного типа
