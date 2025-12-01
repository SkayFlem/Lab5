# Домашнее задание к работе 5
## Условие задачи
Написать программу вычисления значения функции двух переменных. Результат проверить на контрольном примере.

## 1. Алгоритм и блок-схема
### Алгоритм
1. **Начало**
2. ввод значений :
   - `x` = первое число.
   - `y` = второе число.

3. Объявить константы:
   - `E` = 2.718281828459045.
4. Счёт
   - `korenchislitel` =  1 + pow(cos(x),2).
   - `choslitel` =  2.33 * log( pow(korenchislitel, 0.5))
   - `znamenatel` = pow(E, y) + pow(sin(x), 2)
5. Выводим результаты расчетов:
   - `printf("F(%f, %f) = %f", x, y, rezult);`
6. **Конец**
   
### Блок-схема
<img width="122" height="421" alt="Диаграмма без названия drawio" src="https://raw.githubusercontent.com/wyrtwwr/email-assets/refs/heads/main/lab5_%D1%81%D1%85%D0%B5%D0%BC%D0%B0.jpg" />

## 2. Реализация программы
#define _CRT_SECURE_NO_WARNINGS
#define _USE_MATH_DEFINES
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <math.h>
int main() {
	setlocale(LC_ALL, "RUS");
	const double E = 2.718281828459045; 
	float x, y;
	printf("введите x:");
	scanf("%f", &x);
	printf("введите y:");
	scanf("%f", &y);
	printf("Введеные значения:");
	printf("x = %f, y = %f\n", x, y);
	float korenchislitel = 1 + pow(cos(x),2);
	float choslitel = 2.33 * log( pow(korenchislitel, 0.5) );
	float znamenatel = pow(E, y) + pow(sin(x), 2);
	float rezult = choslitel / znamenatel;
	printf("F(%f, %f) = %f", x, y, rezult);
	printf("\nКонтрольные примеры:\n");
	float x2 = 1.9;
	float y2 = -1.0;
	printf("x2 = %f ,y2 = %f\n", x2, y2);
	float korenchislitel2 = 1 + pow(cos(x2), 2);
	float chislitel2 = 2.33 * log(pow(korenchislitel2, 0.5));
	float znamenatel2 = pow(E, y2) + pow(sin(x2), 2);
	float rezult2 = chislitel2 / znamenatel2;
	printf("F(1.9, -1.0) = %f\n", rezult2);
	float x3 = 1.6;
	float y3 = -2.3 * pow(E,-6);
	printf("x3 = %f ,y3 = %f\n", x3, y3);
	float korenchislitel3 = 1 + pow(cos(x3), 2);
	float chislitel3 = 2.33 * log(pow(korenchislitel3, 0.5));
	float znamenatel3 = pow(E, y3) + pow(sin(x3), 2);
	float rezult3 = chislitel3 / znamenatel3;
	printf("F(1.9, -1.0) = %f\n", rezult3);
}

## 3. Результаты работы программы
=== СИСТЕМА КОНТРОЛЯ ДОСТУПА ЭНЕРГИИ===
введите x:1,2223
введите y:3,4343
Введеные значения:x = 1,222300, y = 3,434300
F(1,222300, 3,434300) = 0,004029
Контрольные примеры:
x2 = 1,900000 ,y2 = -1,000000
F(1.9, -1.0) = 0,091668
x3 = 1,600000 ,y3 = -0,005701
F(1.9, -1.0) = 0,000498

<img  src="https://raw.githubusercontent.com/wyrtwwr/email-assets/refs/heads/main/lab5_consl.jpg" width="981" height="266">
