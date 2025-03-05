ЛР №2 с использованием PyTorch.
Классификация изображений по цветам. Определение цвета на финальном изображении.
Код был собран самостоятельно из разных работ найденных в интернете. Т.к. изучаю питон, собрать в единое было не прям сложно.
Нейронная сеть принимает датасет (датасет включает в себя 2276 изображений с разной цветовой гаммой, поделены на папки Blue, Pink, Yellow и т.д. (всего 12шт))
НС сжимает изображения до размера 128х128, загружает изображения из папок. Данные разделяются на обучающую и тестовую выборки (80% на обучение и 20% на тестирование). Далее определяется архитектура НС, она состоит из 2ух сверточных слоев, 2ух полносвязанных слоев и 2ух слоев подвыборки. Далее происходит обучение модели 10 раз, вычисляются потери. После обучения модель оценивается на тестовом наборе данных. Вычисляется точность предсказаний. Состояние обученной модели сохраняется в файл `color_classifier.pth`. 
Точность предсказаний - 80.67% Связанно с тем, что во многих изображениях присутствует палитра из самых разных цветов.  
Далее на выбранном файле определяется цвет.
В качестве примера (Example.png) выбрано изображение с абстракцией, где Розовый цвет доминирует.
НС определяет цвет, и как видно из примера, предполагает что это цвет Pink.

Датасет взят из github - https://github.com/riyanswat/color-recognition-dataset.git

![Example](https://github.com/user-attachments/assets/d6d1f862-03c9-41bd-b24a-bcfadb40fd38)
