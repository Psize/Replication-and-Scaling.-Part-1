# Домашнее задание к занятию «Репликация и масштабирование. Часть 1»
## Задание 1
В схеме master‑slave есть один ведущий узел (master), который принимает все операции записи, и один или несколько ведомых (slave), которые только читают данные и получают изменения от master. Это просто настраивается, не вызывает конфликтов записи, но при отказе master запись становится невозможной до ручного переключения. В схеме master‑master оба узла одновременно являются и master, и slave, то есть запись разрешена на любой из них, а изменения реплицируются в обе стороны. Это даёт более высокую доступность записи, но требует разрешения конфликтов (например, при одновременном обновлении одной строки или при автоинкременте) и усложняет настройку. Master‑slave обычно применяют для масштабирования чтения и резервного копирования, а master‑master – для географически распределённых систем или когда нужна запись на несколько узлов с приемлемой сложностью.

--- 

## Задание 2
master
<img width="875" height="80" alt="image" src="https://github.com/user-attachments/assets/0cee64e6-e216-4acd-b07f-1c6ac8f625cd" />

<img width="642" height="174" alt="image" src="https://github.com/user-attachments/assets/4ab3662c-e1b9-4dd4-bea1-4d528c12f7f2" />

<img width="265" height="191" alt="image" src="https://github.com/user-attachments/assets/df74a73c-226b-4e66-b257-1ff8b8cbf618" />


slave
<img width="825" height="89" alt="image" src="https://github.com/user-attachments/assets/dee1278e-159e-4a95-957a-146246db4a2a" />

<img width="760" height="967" alt="image" src="https://github.com/user-attachments/assets/b9e68cc6-f5ff-43ba-87f6-a0c035c9a03b" />

<img width="265" height="191" alt="image" src="https://github.com/user-attachments/assets/b02c4aed-59c2-48c8-8aa6-358238d895ad" />

