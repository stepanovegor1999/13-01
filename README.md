Домашнее задание к занятию «Уязвимости и атаки на информационные системы»
Задание 1
Скачайте и установите виртуальную машину Metasploitable: https://sourceforge.net/projects/metasploitable/.

Это типовая ОС для экспериментов в области информационной безопасности, с которой следует начать при анализе уязвимостей.

Просканируйте эту виртуальную машину, используя nmap.

Попробуйте найти уязвимости, которым подвержена эта виртуальная машина.

Сами уязвимости можно поискать на сайте https://www.exploit-db.com/.

Для этого нужно в поиске ввести название сетевой службы, обнаруженной на атакуемой машине, и выбрать подходящие по версии уязвимости.

Ответьте на следующие вопросы:

Какие сетевые службы в ней разрешены?
<img width="1718" height="1048" alt="Ubuntu 1-2025-07-18-16-57-39" src="https://github.com/user-attachments/assets/9516ce60-3ffb-4de2-b3c4-a66a0fd07f78" />

Какие уязвимости были вами обнаружены? (список со ссылками: достаточно трёх уязвимостей)
<img width="1718" height="1048" alt="Ubuntu 1-2025-07-18-17-00-59" src="https://github.com/user-attachments/assets/e6c65730-eab2-4417-83f0-15910d794724" />
<img width="1718" height="1048" alt="Ubuntu 1-2025-07-18-17-00-49" src="https://github.com/user-attachments/assets/d7fff602-b26f-4737-866a-9e5acbd0a921" />


Задание 2
Проведите сканирование Metasploitable в режимах SYN, FIN, Xmas, UDP.

Запишите сеансы сканирования в Wireshark.

Ответьте на следующие вопросы:

Чем отличаются эти режимы сканирования с точки зрения сетевого трафика?
Как отвечает сервер?
Приведите ответ в свободной форме.
SYN сканирование <img width="1718" height="1048" alt="Ubuntu 1-2025-07-18-17-10-02" src="https://github.com/user-attachments/assets/3cffdfa9-92bd-4897-ad6d-0869c5c6b5a6" />
Fin <img width="1718" height="1048" alt="Ubuntu 1-2025-07-18-17-11-12" src="https://github.com/user-attachments/assets/250dd9f2-bd05-4831-bead-8fb73dd1a783" />
Xmas <img width="1718" height="1048" alt="Ubuntu 1-2025-07-18-17-11-59" src="https://github.com/user-attachments/assets/0555dd0c-a904-4ad7-8a66-95047dc05198" />
UDP <img width="1718" height="1048" alt="Ubuntu 1-2025-07-18-17-12-57" src="https://github.com/user-attachments/assets/141cd43f-eb37-401d-ad51-516c5b56b369" />

SYN сканирование протокол TCP	Отправляется SYN	Ответ: SYN-ACK (если порт открыт), RST (если закрыт)
FIN сканирование протокол	TCP	Отправляется FIN	Открытый порт — игнорирует, закрытый — RST
Xmas сканирование протокол	TCP если порт закрытый — RST
UDP сканирование протокол UDP	если порт закрытый — "Port Unreachable"
