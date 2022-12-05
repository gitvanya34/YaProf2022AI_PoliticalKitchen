# YaProf2022AI_PoliticalKitchen 
> Задача предоставлена партнером олимпиады — Федеральным исследовательским центром \Информатика и управление\ РАН

- #### На некотором несуществующем интернет-ресурсе \Политическая кухня\ популярностью пользуются два вида видеороликов: про политику и про кулинарию. При этом под роликами про консервативную политику комментарии оставляют только консерваторы, про либеральную --- только либералы. Кулинарные видео комментируют только кулинары. Иногда на ресурсе \Политическая кухня\ происходит сбой, и комментарии перепутываются (кулинарный комментарий попадает под политическое видео, либеральный --- под консервативное видео и т.п.), тогда необходимо по комментарию определить, кто его оставил (консерватор, либерал или кулинар) и перенести в соответствующий раздел. Доступа к самим текстам комментариев у команды \Политической кухни\ нет, но все тексты прошли обработку лингвистическим анализатором и каждый представлен набором численных признаков.
    
    

> Перед вами стоит задача разработать алгоритм машинного обучения, предсказывающий кем был написан комментарий: консерватором, либералом или кулинаром.

### Формат ввода

[Набор данных](https://disk.yandex.ru/d/9XuZIF8IIAx2fw) (или в архиве)


Тренировочная выборка Train.csv представляет собой csv-таблицу со столбцами-признаками и столбцом целевой переменной target.

Описание признаков обучающих данных:

• ___comments_count___ – общее количество комментариев под видео, для которого создан комментарий,

• ___replies_count___ – общее количество ответов на комментарии под видео,

• ___both_count___ – общее количество сообщений под видео,

• ___sentence_count___ – общее количество предложений под видео,

• ___word_count___ – общее количество слов под видео,

• ___target___ – метка кем был оставлен комментарий (0 – либерал, 1 – кулинар, 2 – консерватор),

• ___остальные столбцы___ – признаки, полученные с помощью лингвистического анализатора.

Тестовая выборка Test.csv представляет собой csv-таблицу со столбцами-признаками --- данные, ответы на которые нужно послать в тестирующую систему.

### Формат вывода
В файле SampleSubmission.csv показан формат файла ответа, который нужно загружать в систему. В связи с особенностями работы скрипта подсчета метрики качества, необходимо сохранять порядок следования строк в выходном файле submission.csv.

> Примечания:
Используемая метрика --- многоклассовый F1-score с глобальным усреднением.

Ваш балл вычисляется по формуле 
f1⋅10, где f1 --- результат работы вашего алгоритма.
______
# [Решение ](politicalKitchen.ipynb)