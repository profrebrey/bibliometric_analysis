# bibliometric_analysis
Bibliometric analysis of academic journal
Цель проекта: провести библиометрический анализ международного научного журнала Feminist Economics с целью выявления основных тенденций развития научного направления Феминистская экономика (Экономика гендера). 

Описание данных: 
Спарсила с сайта редакции всю информацию о статьях и авторах. 
'Volume' Том (сквозная нумерация)
'Issue' Выпуск
'Issue_title' Название выпуска - есть в специальных выпусках
'Year' Год выпуска - с 1995 до 2022 
'Article_number' номер статьи - особенно важно, какая тема будет под номером один
'Title' - заглавие статьи - тоже полезно для определния тем
'Author1' -ФИО первого автора
'Author1_Info' - инфо о первом авторе. Из инфо можно извлечь страну, город, университет, факультет, номер ORCID  
'Author1_Contacts'- город и университет для авторов - так как для первых выпусков не было info
'Pages' номера страниц журнала - можно вычислить продолжительность статьи - но это будет не очень точно. Лучше количество знаков или слов. А на количество страниц могут влиять таблицы и рисунки и прочие приложения
'Date_published' дата онлайн публикации статьи
'DOI' номер DOI
'Abstract' - текст аннотации статьи 
'Highlights' -  основные тезисы статьи. Есть только в последней трети статей. Наверное легче удалить
'Keywords' - ключевые слова
'JEL codes' - посмотреть какие области экономических наук покрывает направление feminist economics 
'Views' - количество просмотров статьи на сайте - выделить самые популярные темы
'CrossRef'- количество ссылок на эту статью в научной литературе
'Almetric' -  колчисевто ссылок на эту статью в сми и соцсетях
'References' - список цитируемой литературы
'Citations' - список статей, процитировавших эту статью 
'WOS' - число цитат в базе данных Web of Science 
'Scopus' число цитат в Скопусе 
'Open_access' - 1 означает, что статья бесплатная, 0 - платная 
'lemmatized_text' - лемматизированный текст
'lemmatized_tokens лемматизированные токены 


Задачи и методы проекта: 

1. Выявить основные темы статей журнала на основе анализа аннотаций всех выпусков статьей (28 лет, 4 выпуска в год. После парсинга данных в табличке стало 925 строчек)
Методы: были испробованы методы кластеризации, LDA, но они не показали хороших и интерпретируемых результатов. Самой удачной вышла модель TF IDF 
TF-IDF (term frequency - inverse document frequency) — статистическая мера, используемая для оценки важности слова в контексте документа, являющегося частью коллекции документов или корпуса. Вес некоторого слова пропорционален частоте употребления этого слова в документе и обратно пропорционален частоте употребления слова во всех документах коллекции.

Мера TF-IDF часто используется в задачах анализа текстов и информационного поиска, например, как один из критериев релевантности документа поисковому запросу, при расчёте меры близости документов при кластеризации.

IDF не показала интересных результатов при использовании с одним словом. Поэтому попробовала посмотреть со словосочетаниями. 

Основные темы также можно посмотреть по ключевым словам и также посмотреть как они менялись по годам и сравнить с результатами анализа аннотаций 
Посмотреть темы по заглавиям статей 

2. Посмотреть, как менялись словосочетания по годам 
Сгруппировать таблицу по годам, объединить аннотации и посмотреть tf idf
Сделано 

3. Посмотреть контекст использования основных терминов, определяющих темы, таких как 
feminist / feminism, gender, 

Не сделано 

4. Посмотреть как связаны темы и авторы, особенно страны проживания и университеты, где работают авторы.  

5. Ключевые слова. Классифицировать ключевые слова и выделить оттуда названия стран, методы анализа и темы - сделано 

6. Посмотреть какие темы опубликуются в первой статье каждого выпуска журнала как самые главные с точки зрения редакции 

