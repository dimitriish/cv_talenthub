# cv_talenthub
 - Шопхоев Дмитрий Сергеевич
  - Обработка и генерация изображений
  - Мультиклассовая классификация на датасете CIFAR-10
  - Были дообучены и сравнены ResNet с 18, 34 и 50 слоями.

![image](https://github.com/dimitriish/cv_talenthub/assets/62793986/d084d3a3-ac0b-4a28-9f25-391d7c36e7ef)
![image](https://github.com/dimitriish/cv_talenthub/assets/62793986/c2e71e5e-8d77-4805-b5a1-ec4554b00d65)
![image](https://github.com/dimitriish/cv_talenthub/assets/62793986/9dd7c5ea-f4c2-4386-a807-113115dc3ed3)
![image](https://github.com/dimitriish/cv_talenthub/assets/62793986/24772548-ab20-460a-9024-14e999196dc7)
![image](https://github.com/dimitriish/cv_talenthub/assets/62793986/2c80053a-0e3c-433f-9e56-c9fa36cf4369)
![image](https://github.com/dimitriish/cv_talenthub/assets/62793986/f0c5922b-db87-4f44-ab7a-572522f27bda)
![image](https://github.com/dimitriish/cv_talenthub/assets/62793986/47963fe0-9108-4063-a58f-c54419c51aad)


## Выводы
По функции потерь и точности на трейне можно предположить, что resnet18 обучилась полностью, вышла на плато примерно на 12 эпохе, resnet34 на последней эпохе догнала более младшую модель и потенциально еще может дообучиться, а resnet50 обучилась плохо и нужно еще дообучать.

Однако функция потерь на валидации для двух младших моделей начала расти, что говорит о переобучении, для resnet50 делать выводы сложно - лосс нестабилен, как на трейне, так и на валидации

Однако на тестовой выборке resnet50 показала результаты лучше, а resnet18 и resnet34 показали почти идентичные результаты, можно предположить, что обе эти модели переобучились на трейне.
