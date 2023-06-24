# Домашнее задание №2

## Данные:
    * Гистоновая метка: H3K4me1
    * Клеточная линия: K562
    * Реплика 1: ENCLB497KKU
    * Реплика 2: ENCLB060JFJ
    * Контроль: ENCFF000VEK 

Ссылка на тетрадку: https://colab.research.google.com/drive/1OT6iWlQWoBWUgF2p0lcDzlcx1gItRXm4?usp=sharing

## Анализ FastQC
### ENCFF000VDV (Table 1)
До подрезания             |  После
:-------------------------:|:-------------------------:
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/b829c309-4139-4766-9481-08373af5310a) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/b9211976-257e-43c2-94be-2ee9120c2f4b)
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/1e4f067a-49aa-43b0-9277-b551cdfc687f) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/cea9ff3c-17d3-49b1-8c3b-0c69e66ea645)
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/5ecf20fe-e502-4577-a0b6-759d54ce7661) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/c498adf4-4509-4113-b848-f589cb94b5fe)
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/dd1f82dd-eeb3-420a-94fa-7d96433853f1) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/aab9a36c-ab18-418d-ad55-2e2a829da14f)
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/d412145b-1bad-40a1-8b51-70433bb607f4) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/32a29cce-b115-4a67-a51e-68bc27c2d59a)
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/a52bf68c-d5bb-46e3-b907-f61c67138d4d) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/051a0303-5bf2-4d8a-a82c-3ad32dfb9faf)

Выводы: как можем видеть на графике Per base sequence quality, чтение не прошло проверку качества и, следовательно, необходимо его подрезать (я воспользовалась trimmomatic). После подрезания картина заметно улучшилась: графики качества либо изменили показатели к лучшему, либо остались на прежнем (хорошем) уровне.   

### ENCFF000VDU (Table 2)
До подрезания             |  После
:-------------------------:|:-------------------------:
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/d38ebccd-e8ce-47fa-a7b9-81dd6bbe3eee) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/e9f296a8-3850-4d01-a879-1cc9a9fc892f)
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/224d95b5-a3ba-4d0b-866a-103e84a08ffb) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/50aebfc8-96f6-4967-be93-a3b7c858182e)
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/3c4f38f1-a86c-42b0-a7b6-8dc1be121271) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/55a4ce60-c189-4b94-aac8-8de9a4e502e1) 
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/6e7c89ff-8fb1-4d4e-9b45-776da06449aa) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/dbfa5c7f-d9cf-4305-90a5-b173e4027247)
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/c690b467-6c8e-4188-bf2d-870bb6377c38) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/75f242f1-943c-455a-8b90-2db7e034514c)

Выводы: Ситуация похожа на то, что мы видели в первой реплике, однако показатели на графике Per base sequence quality намного хуже. Подрезание (я воспользовалась trimmomatic) несколько улучшает картину, но проверку качества (для данной метрики) чтение все равно не проходит.

### ENCFF000VEK
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/7ce0ceb6-f247-4f5b-8839-81776b02fcd3) 

![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/99d85491-4b9f-4ecb-9ff4-b4cbb3994e96) 

![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/b28eff5a-628c-4805-a7db-19d0c656582a)

![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/238177bf-c72b-4038-90d5-d6a9fd593818) 

![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/e09fbd98-1e02-4068-b0d1-cc706c5e9057)

Выводы: как видно из саммари и последующих графиков, чтение контрольной последовательности проходит проверку качества по всем метрикам и, следовательно, в подрезании не нуждается   

## Выравнивание на 7-ую хромосому: статистика

ChIP-seq	| Total number of reads |	Unique reads number |	Common reads number |	No Alignment
:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:
ENCFF000VDV	| 13962988 |	754540 (5.40%)	 | 3095936 (22.17%) |	10112512 (72.42%)
ENCFF000VDU	| 36240958 |	1973592 (5.45%) |	5392765 (14.88%) |	28874601 (79.67%)
ENCFF000VEK	| 36418708 |	2626947 (7.21%) |	5271026 (14.47%) |	28520735 (78.31%)

Комментарий: поскольку мы выравнивали чтение всего на одну хромосому, количество выравниваний получилось небольшим, что было ожидаемо. Количество уникальных выравниваний не слишком высоко, но лежит в пределах нормы. 

## Диаграммы Венна
X > Y             |  Y > X
:-------------------------:|:-------------------------:
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/1dadc810-2f52-49d6-b39a-0604f2718ec0) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/1688b3ff-d370-4732-9a2b-f44198685957)

![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/f58b7f56-a9ab-4bd9-9150-ca1e4b532188) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/91fca8fa-0205-45e6-99ba-bc5580d241e7)

Комментарий: Аглоритм, на котором строятся данные диаграммы работает таким образом, что пики первого чтения ищутся во втором чтении. Если некторые пики, первого чтения меньше (нет совпадения в размере пиков), то алгоритм выдаст совпадение при сравнении превого со вторым, но не даст его при сравнении второго с первым (поскольку большие пики содержат меньшие, но не наоборот).Отсюда и разница в цифрах и графиках. Про само количество пересечений можно сказать, что оно относительно небольшое (ожидаемо), опять же, потому что выпавнивание происходило на всего одну хромосому.

## Бонусная часть:
### ENCFF825PKH

Типичное             |  Эксперементальное
:-------------------------:|:-------------------------:
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/1cc272a4-e544-4ee1-a7a5-4a233e8f5501) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/9afab55a-aff5-43ea-9630-54818d4e8a2e)

Выводы:

### ENCFF196QGZ

Типичное             |  Эксперементальное
:-------------------------:|:-------------------------:
![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/349810c7-d103-42de-9e40-770e83ebde56) | ![image](https://github.com/mylifeclosetwice/hse_hw2_chip/assets/71773580/072cedf1-766e-4354-9280-dbb9539f1027)

Выводы:















