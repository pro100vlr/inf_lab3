# Лабораторная работа 3

Для выполнения этой лабораторной работы я скачала UTM.Что такое UTM? UTM - это полнофункциональный эмулятор системы и хост виртуальной машины для iOS и macOS. Одним словом, он позволяет запускать Windows, Linux и многое другое на Mac, iPhone и iPad.

<img width="771" alt="Снимок экрана 2024-11-02 в 22 23 27" src="https://github.com/user-attachments/assets/06846b69-9136-47ef-92d9-8235a32efa22">

Открыла и установила 3 виртуальные машины. Я изменила названия машин:

Машина А - MashinaB, Машина Б - MashinaC, Машина В - MashinaE.

Вот так открывается виртуальная машина:

<img width="802" alt="Снимок экрана 2024-11-02 в 22 29 58" src="https://github.com/user-attachments/assets/087f9c79-aee0-492a-a790-c16662597bde">

<img width="1281" alt="Снимок экрана 2024-11-02 в 22 32 26" src="https://github.com/user-attachments/assets/092c7ba1-9f0f-4807-b77b-f6b154f40441">

<img width="1286" alt="Снимок экрана 2024-11-02 в 22 33 51" src="https://github.com/user-attachments/assets/e61d0706-5444-4de5-8a63-0263a587f17b">

И так работает 3 виртуальные машины.

Проверила, что виртуальная машина выходит в интернет:

<img width="650" alt="Снимок экрана 2024-11-02 в 22 38 18" src="https://github.com/user-attachments/assets/fa9b0850-5afd-4d57-8d5d-38d0d506facc">

ping используется для проверки соединения между компьютером и удаленным сервером или устройством.

Команда ping google.com используется для проверки соединения между компьютером и сервером Google.

Благодаря этой команде проверили на доступ в Интернет 3 машин.Все выполняется !

Для того чтобы организовать сетевой доступ нужно знать ip-адреса машин C и E. Адрес посмотрела в настройках.

ip-адпес C: 192.168.64.5
ip-адрес E: 192.168.64.8

По условию задачи, нужно предоставить доступ из B в C, из B в E, выполняю это условие с помощью ping:

<img width="615" alt="Снимок экрана 2024-11-02 в 23 18 08" src="https://github.com/user-attachments/assets/272c2f10-9691-4510-a13d-23d8087a831c">

Чтобы запретить доступ из машины С в машину E использовала команду:

sudo iptables -A INPUT -s <IP-адрес машины 2> -j DROP

Команда sudo iptables -A INPUT -s <IP-адрес машины 2> -j DROP добавляет новое правило в цепочку INPUT, которое блокирует входящий трафик с указанного IP-адреса. Это означает, что все пакеты, поступающие с этого IP-адреса, будут блокироваться и не будут передаваться дальше.

Команда iptables является мощным инструментом для управления сетевым доступом и фильтрации пакетов в операционных системах Linux. Она позволяет администраторам настроить сетевой доступ и обеспечить безопасность компьютера или сети.

<img width="688" alt="Снимок экрана 2024-11-02 в 23 26 34" src="https://github.com/user-attachments/assets/107c1d38-293f-4333-8053-b2657c806202">

Проверка на выполнения условия:

<img width="552" alt="Снимок экрана 2024-11-02 в 23 28 24" src="https://github.com/user-attachments/assets/62d4d81f-5c63-4b1e-bf4e-fee13f7dba88">

С помощью ping и ip-адреса обращаемся к машине E из машины С. Вижу, что при отправке пакетов от машины E не получила ответа, слеловательно условие задачи выполнено.

Общий скрин:

<img width="1166" alt="Снимок экрана 2024-11-02 в 23 37 21" src="https://github.com/user-attachments/assets/742eb84d-bd67-4c96-b8df-ba057738adac">

Вывод: в данной лабораторной работе научилась устанавливать виртуальные машины.Научилась предоставлять сетевой доступ, а также запрещать его.







