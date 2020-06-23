# car-plate-numbers-ocr
Baseline for MADE kaggle competition

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/alexyar88/car-plate-numbers-ocr/blob/master/car-plates-ocr.ipynb)

- Используется MaskRCNN. Предсказываем не только bounding box (детекция), но и маску для номера (сегментация).
- По маске делаем 4-угольный полигон, который разворачиваем в прямоугольник. Используем для предсказания и bounding box, и маску.
- Для OCR используется CRNN из лекции. 
- Для того, чтобы понять, действительно ли на картинке номер, используется не только score из детектора, но и норма argmax логитов каждого символа из OCR модели. 
