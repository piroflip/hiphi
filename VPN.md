Инструкция по созданию мобильного роутера дл яработы сервисов от HiPhi в машине

Основная концепция:
Нам необходимо получить ip адрес который бы проходил CloudWAF (облачный межсетевой экран от HumanHorizons)
Делать мы это будем на основе роутера ZTE MF90+ с поддержкой OpenVPN. Хотя можно любой другой, который поддерживает OpenVPN.
Просто роутер от ZTE, как оказалось, обкатан и может быть модифицирован без глубоких знаний.

Идем на Авито и покупаем роутер сразу разлоченый под всех операторов и все симки (это важно). Ну или в любом другом месте.
Покупаем симку с безлимитным интернетом. Проверяем, что интернет через роутер работает.
Идем на сайт https://90.vzte.ru/ Там есть видеоинструкция по установке клиента OpenVPN. Берем самую обычную версию. Это стоит еще рублей 590.

Далее следует купить сервер в Гонконге и установить туда OpenVPN сервер. Сразу отмечу, подходят не все. Я перепробовал штук 5,
многие попадают в блок CloudWAF. Я остановился на https://62yun.ru/ Там оплата по СБП и ip подходят нам.
Сразу предупрежу этот шаг наиболее технически сложен. Кто знает как это сделать, тот сможет установить сервер, а кто нет, может обратиться ко мне
и я могу организовать OpenVPN профиль.
Далее грузим этот профиль в роутер, ДНС пофиг, у меня использует гугловские, все равно работает

Важное отступление, для правильной работы роутера, необходимо сменить адрес сети с 192.168.0.1 на, например, 192.168.99.1. И диапазон выдачи DHCP
c 192.168.0.100-192.168.0.200 на 192.168.99.100-192.168.99.200