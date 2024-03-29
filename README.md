# HDR
# Алгоритм слияния экспозиций Мертенса

Этот проект реализует алгоритм слияния экспозиций, предложенный Томом Мертенсом и его коллегами. Цель алгоритма — объединить серию изображений с различной экспозицией в одно изображение, чтобы улучшить видимость как светлых, так и темных участков.

## Основы

Алгоритм использует три меры качества для оценки каждого пикселя на входных изображениях:

- Контрастность (C)
- Насыщенность (S)
- Хорошо экспонированные области (E)

Эти параметры комбинируются для создания весовых карт, которые затем используются для многоуровневого слияния с использованием пирамид Гаусса и Лапласа.

## Реализация

Код написан на Python и использует библиотеки OpenCV и NumPy для обработки изображений и Matplotlib для визуализации.

### Класс `exposureFusion`

Ключевой класс `exposureFusion` включает методы для создания весовых карт, построения гауссовых и лапласиановых пирамид и слияния изображений.

### Процесс

1. Инициализация объекта `exposureFusion` с заданными параметрами весов.
2. Загрузка исходных изображений.
3. Вычисление весовых карт для контрастности, насыщенности и хорошей экспонированности.
4. Слияние изображений на основе вычисленных весов.
5. Визуализация исходных и полученных изображений.

## Результаты

В репозитории представлены примеры исходных изображений и результаты слияния при различных наборах весов.

## Установка и Запуск

Для работы с проектом убедитесь, что установлены следующие библиотеки:

- NumPy
- OpenCV
- Matplotlib

Установите их с помощью команды `pip`:

```sh
pip install numpy opencv-python matplotlib


* [Ссылка на ноутбук](https://github.com/yuliats77/HDR/blob/main/julia_diploma/hdr.ipynb)

