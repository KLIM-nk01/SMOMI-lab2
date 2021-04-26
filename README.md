# Лабораторная работа 2.

**Цель лабораторной работы:** Обучить нейронную сеть с использованием техники
обучения Transfer Learning [1]

**Задачи:**

1. С использованием примера [2] обучить нейронную сеть EfficientNet-B0 [3,4,5]
(случайное начальное приближение) для решения задачи классификации
изображений Food-101 [6]
2. С использованием [2] и техники обучения Transfer Learning [7] обучить нейронную
сеть EfficientNet-B0 (предобученную на базе изображений imagenet) для решения
задачи классификации изображений Food-101


![image](https://user-images.githubusercontent.com/56519328/116051585-6b880380-a681-11eb-8f16-07aee4705635.png)

**Графики обучения нейронной сети EfficientNet-B0(случайное начальное приближение)**

***График метрики точности:***
![image](https://user-images.githubusercontent.com/56519328/116051765-9bcfa200-a681-11eb-851d-0e190f08f53c.png)
***График функции потерь:***
![image](https://user-images.githubusercontent.com/56519328/116051810-a7bb6400-a681-11eb-8290-a74a6c8011b0.png)


**Графики обучения нейронной сети EfficientNet-B0 c использованием техники обучения Transfer Learning**
![image](https://user-images.githubusercontent.com/56519328/116051962-dafdf300-a681-11eb-99fc-4b41a03eeb99.png)

  
***График метрики точности:***
![image](https://user-images.githubusercontent.com/56519328/116052097-f963ee80-a681-11eb-810f-4bac3fac901e.png)
***График функции потерь:***
![image](https://user-images.githubusercontent.com/56519328/116052147-05e84700-a682-11eb-964d-6deb4ca59856.png)

***Анализ полученных результатов***
В ходе выполнения первой задачи лабораторной работы: обучение нейронной сети EfficientNet-B0 (случайное начальное приближение), при обучении процесс прервался на 36 эпохе, однако, анализируя графики, могу сказать, что нейронная сеть обучается до 2-3 эпохи, что видно из графика метрики точности (после 2-3 эпохи показатель начал уменьшаться), и из графика метрики потерь(показатели начали возрастать). Максимальная точность для тренировочных данных составила 30%, а на валидационных 31%.
Во второй задаче использовали технику обучения Transfer Learning, предобученную на базе изображений imagenet. Анализируя графики, могу сказать, что была достигнута точность в 83% на тренировочных данных и 63% на валидационных, как видно, эти показатели гораздо выше, чем при обучении без техники Transfer Learning. Однако анализируя график функции потерь можно сказать, что нейронная сеть начала переобучаться после 4 эпохи(функция потерь для валидационных данных начала возрастать, для тренировочных - уменьшаться) и графика метрики точности для валидационных данных(на 4 эпохе точность составила 66% , далее начала снижаться и в итоге достигла показателя в 63%).
