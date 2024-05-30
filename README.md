**Задание 1.**

*Рассчитать количество хостов в сети 10.10.80.128/25.*

**Решение 1.**

- Адрес сети: 10.10.80.128

- Минимальный адрес хоста: 10.10.80.129
  
- Максимальный адрес хоста: 10.10.80.254
 
- Широковещательный адрес: 10.10.80.255
  
- Количество адресов: 126.


**Задание 2.**

*Рассчитать количество подсетей с префиксом /28 в сети 192.168.0.0/23.*


**Решение 2**

Для того чтобы рассчитать количество подсетей с префиксом /28 в сети 192.168.0.0/23, необходимо выполнить следующие шаги:

Сначала определим количество доступных адресов в сети /23. Для префикса /23 у нас есть 2^9 = 512 адресов, включая сетевой адрес и широковещательный адрес.

Подсеть с префиксом /28 имеет 2^4 = 16 адресов, но из них 2 адреса будут зарезервированы для сетевого адреса и широковещательного адреса, поэтому у нас остается 14 адресов для узлов.

Для того чтобы узнать, сколько подсетей с префиксом /28 мы можем получить из сети /23, нужно разделить общее количество адресов в сети /23 на количество адресов в каждой подсети /28:

(512 адресов в /23) / (14 адресов в /28)  округляем до до целого числа, получаем 36.

Получается, что мы можем получить 36 целых подсетей с префиксом /28 из сети 192.168.0.0/23. То есть в данной сети можно создать 36 подсетей с префиксом /28.



**Задание 3.**

Какой IP адрес не входит в диапазон сети 172.16.30.128/25?

а) 172.16.30.254

б) 172.16.30.199

в) 172.16.30.1


**Решение 3.**

Диапазон IP адресов в сети 172.16.30.128/25 будет следующий:

- Начальный IP адрес: 172.16.30.128
 
- Конечный IP адрес: 172.16.30.255
  
- Диапазон доступных IP адресов: от 172.16.30.129 до 172.16.30.254

Теперь оценим каждый предложенный IP адрес:

а) 172.16.30.254: Этот IP адрес входит в диапазон сети 172.16.30.128/25.

б) 172.16.30.199: Этот IP адрес также входит в указанный диапазон.

в) 172.16.30.1: Этот IP адрес не входит в диапазон, так как он находится перед начальным адресом 172.16.30.128.


Таким образом, IP адрес "172.16.30.1" не входит в диапазон сети 172.16.30.128/25.

Способ расчета заключается в определении начального и конечного IP адресов по маске подсети (в данном случае /25, что означает 25 бит подсети), а затем выделении диапазона доступных IP адресов от начального до конечного, и проверке входит ли конкретный IP адрес в этот диапазон.



**Задание 4.**

*Необходимо выделить подсети из диапазона 192.168.255.0/24 для 2-х групп пользователей по 70 хостов.*



**Решение 4.**

Для выделения подсетей из диапазона 192.168.255.0/24 для 2-х групп пользователей по 70 хостов каждая, нужно сначала определить количество бит, необходимых для хостов в каждой подсети.

Для 70 хостов понадобится 7 бит (2^7 - 2 = 126 - 2 = 124 хоста) или 8 для обеспечения достаточного количества IP-адресов.

Учитывая, что у нас имеется диапазон 192.168.255.0/24, который имеет 24 бита для сети и 8 бит для хостов, мы можем использовать первые 3 бита из 24 в качестве дополнительных битов сети для новых подсетей.

Рассмотрим следующие диапазоны:

1. Первая подсеть для первой группы пользователей:
- Сеть: 192.168.255.0/27
  
- Адрес шлюза: 192.168.255.1
  
- Broadcast адрес: 192.168.255.31

2. Вторая подсеть для второй группы пользователей:
   
- Сеть: 192.168.255.32/27
  
- Адрес шлюза: 192.168.255.33
  
- Broadcast адрес: 192.168.255.63

Таким образом, мы выделили 2 подсети для 2-х групп пользователей. В каждой подсети есть 32 IP-адреса, из которых 30 можно использовать для устройств, а 2 IP-адреса зарезервированы для шлюза и broadcast адреса.

Остались свободные подсети в диапазоне 192.168.255.0/24, так как мы использовали только 2 из 256 возможных подсетей. Мы можем продолжать выделять новые подсети для других групп пользователей, используя оставшиеся биты сети.

Таким образом, мы смогли выделить подсети для 2-х групп пользователей, оставив возможность для выделения дополнительных подсетей в данном диапазоне IP-адресов.



**Задание 5.**

*Необходимо выделить подсети из диапазона 172.16.0.0/22 для 2-х групп по 100 хостов и 2-х групп по 50 хостов.*





**Решение 5.**

Для разделения диапазона 172.16.0.0/22 на подсети для 2-х групп по 100 хостов и 2-х групп по 50 хостов, мы можем использовать следующий метод:

Сначала определим количество битов, необходимых для хостов в каждой группе:

- Для группы из 100 хостов нам потребуется минимум 7 бит для хостов (2^7 - 2 = 126 хостов, так как 2 адреса резервируются для адреса сети и broadcast адреса).
  
- Для группы из 50 хостов нам потребуется минимум 6 бит для хостов (2^6 - 2 = 62 хоста).
  

Далее мы можем создать следующие подсети:

1. Для группы из 100 хостов:
   
- Адрес сети: 172.16.0.0/25
  
- Адрес шлюза: 172.16.0.1
  
- Broadcast адрес: 172.16.0.127

2. Для группы из 100 хостов:
   
- Адрес сети: 172.16.0.128/25
  
- Адрес шлюза: 172.16.0.129
  
- Broadcast адрес: 172.16.0.255

3. Для группы из 50 хостов:

- Адрес сети: 172.16.1.0/26
  
- Адрес шлюза: 172.16.1.1
  
- Broadcast адрес: 172.16.1.63

4. Для группы из 50 хостов:
   
- Адрес сети: 172.16.1.64/26
  
- Адрес шлюза: 172.16.1.65
  
- Broadcast адрес: 172.16.1.127

Количество свободных подсетей после выделения этих 4 подсетей можно вычислить следующим образом:

- У нас был диапазон 172.16.0.0/22, что означает 2^10 = 1024 адреса внутри этого диапазона.
  
- Мы выделили 4 подсети суммарным количеством хостов 100+100+50+50 = 300.
  
- Таким образом, осталось 1024 - 300 = 724 свободных хоста.
  
  
  
- Чтобы найти количество свободных подсетей, мы должны ответить на вопрос, какие подсети мы можем выделить с новым префиксом. Поскольку у нас есть 724 свободных хоста, это означает, что мы можем создать подсеть с префиксом /23 для 512 хостов или две подсети с префиксом /24 для 256 хостов каждая.

Таким образом, после выделения 4 подсетей из диапазона 172.16.0.0/22 для 2-х групп по 100 хостов и 2-х групп по 50 хостов, у нас осталось 724 свободных хоста, которые могут быть использованы для создания подсети с префиксом /23 или двух подсетей с префиксом /24.

