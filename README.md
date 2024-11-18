# - Sort data
В проекте сделана сортировка и отображение списка товаров. Ниже описаны основные изменения:

1. Общие утилиты

	•	Созданы универсальные функции:
	•	parseNumber(value) — преобразует строку в число, удаляя все нечисловые символы.
	•	getPrice(item) — извлекает цену товара из строки или объекта с учётом разных форматов хранения данных.

2. Отделение логики отображения

	•	Добавлена функция renderList(items), которая генерирует HTML-код для списка товаров и вставляет его в контейнер .result.
	•	Использован метод map для формирования списка, что делает код более лаконичным.

3. Универсальная функция сортировки

	•	Реализована функция sortAndDisplay(arr, comparator), объединяющая логику сортировки и вывода. В неё передаётся массив данных и функция-компаратор.

4. Компактные функции сортировки

	•	sortByFeedbacks(arr) — сортирует товары по количеству отзывов в порядке убывания.
	•	sortByPrice(arr) — сортирует товары по цене в порядке возрастания.

5. Слушатели событий

	•	Добавлены обработчики событий для кнопок сортировки:
	•	Сортировка по цене (.price).
	•	Сортировка по отзывам (.feed).