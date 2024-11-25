# Systemd

- Написать service, который будет раз в 30 секунд мониторить лог на предмет наличия ключевого слова (файл лога и ключевое слово должны задаваться в /etc/default).
  
- Установить spawn-fcgi и создать unit-файл (spawn-fcgi.sevice) с помощью переделки init-скрипта (https://gist.github.com/cea2k/1318020).
  
- Доработать unit-файл Nginx (nginx.service) для запуска нескольких инстансов сервера с разными конфигурационными файлами одновременно.

  

# Задание 1:

Все файлы в https://github.com/spbsupprt/Systemd watchlog* кладем в директорию templates и выполняем плейбук watchlog.yml.

Плейбук написан для одного хоста, который ссылается на inventory.ini vm1

vm1 прописан в .ssh/config

![image](https://github.com/user-attachments/assets/42802fef-c9a1-4c74-8b66-ad5b9498851f)

https://github.com/spbsupprt/Systemd/blob/main/watchlog.yml

ansible-playbook -i  inventory.ini watchlog.yml

![image](https://github.com/user-attachments/assets/0fd34447-d713-4076-9b90-57a418d7f1d7)

Делаем проверку сервисов и вывода на хосте:

![image](https://github.com/user-attachments/assets/8fb25ad4-06b1-4b1c-9ded-3be68d460989)
