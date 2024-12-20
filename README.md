# Итоговое задание по курсу "Цифровые архивы" 2024 г.
## Общее описание
Данный репозиторий содержит коллекцию веб-архивов сайтов, созданных волонтерами археологических экспедиций, изучающих поселения эпохи викингов и Древней Руси на территории России.
В коллекцию вошли:
- Сайт Гнездовской археологической экспедиции: [gnezdovo.com](https://gnezdovo.com/)
- Сайт экспедиции в Шниткино (Раннесредневековая археологическая экспедиция): [rsae.ru](http://www.rsae.ru/)
- Сайт Новгородской археологической экспедиции: [archnov.com](http://archnov.com/)
## Цель создания
Представленные ресурсы - в большей степени волонтерские проекты сотрудников экспедиций. Нет данных, что их функционирование
обеспечено государственным или каким-либо иным финансированием. Несмотря на то, что в данный момент их существованию нет непостредственной угрозы, мы не можем предсказать срок их существования. При этом на этих ресурсах хранятся материалы, необходимые для изучения в будущем. Исследователи публикуют новости о находках, тематические списки литературы и 3D модели раскопов и находок, которые могут быть не опубликованы в академических изданиях. Кроме того, каждая из экспедиций славится своими традициями, «фольклором», мифологемами. На сайте Гнездовской экспедиции этому посвящен отдельный [раздел](https://gnezdovo.com/mifology/). Такие данные уже сейчас представляют научный интерес для антропологов, фольклористов, психологов, а в будущем – для историков.
## Методология веб-архивации и анализа
Коллекцию веб-архивов была собрана с помощью инструмента [wpull](https://github.com/ArchiveTeam/wpull/blob/develop/doc/usage.rst), описание метаданных подготовлена с помощью [metawarc](https://github.com/datacoon/metawarc), оценка готовности ресурсов к архивации приведена с помощью метода CLEAR, благодаря ресурсу [ArchiveReady](https://archiveready.com/)
## Структура репозитория 
Результаты архивирования для каждого их сайтов представлены в соответсвующих папках:
1. [gnezdovo.com](https://github.com/salmonbelomor/da_git/tree/main/gnezdovo.com)
2. [rsae.ru](https://github.com/salmonbelomor/da_git/tree/main/rsae.ru)
3. [archnov.com](https://github.com/salmonbelomor/da_git/tree/main/archnov.com)

Каждая папка (кроме gnezdovo.com) содержит результат работы wpull: CDX, LOG, WARC.GZ и DB файлы.
В папке gnezdovo.com не содержится WARC.GZ файл, так как его размер больше 2 ГБ. См. облачное хранилище в таблице wpull & metawarc ниже.
Дополнительные файлы включают:
- metawarc_analyse.txt (Результат анализа содержимого WARC.GZ)
- {domain}_pdf.jsonl (Метаданные pdf-файлов)
- {domain}_pdf.jsonl (Экспорт текстового (HTML) содержимого)

## Результаты
Архивация и анализ сайтов [Раннесредневековой археологической экспедиции](http://www.rsae.ru/) и [Новгородской археологической экспедиции](http://archnov.com/) выполнен успешно. Сайт [Сайт Гнездовской археологической экспедиции](https://gnezdovo.com/) архивирован лишь частично из-за ошибки инструмента wpull. Последующий анализ содержимого WARC.GZ файла с помощью инструмента metawarc также оказался невозможен из-за [ошибок](https://i.postimg.cc/J0ZFyW9S/erroe.jpg). 
### ArchiveReady
| CLEAR оценка/ресурс  | [Гнездовская археологическая экспедиция](http://archiveready.com/check?url=https://gnezdovo.com/) | [Раннесредневековая археологической экспедиции](http://archiveready.com/check?url=http://www.rsae.ru/) | [Новгородская археологическая экспедиция](http://archiveready.com/check?url=http://archnov.com/) |
| -------------------- | ---------------------------------------------- | ------------------------------------------ | ------------------------------------------ |
| Accessibility        | 74%                                            | 60%                                        | 60%                                        |
| Cohesion             | 75%                                            | 89%                                        | 89%                                        |
| Metadata             | 100%                                           | 75%                                        | 80%                                        |
| Standards Compliance | 90%                                            | 80%                                        | 87%                                        |
| **Overall Rating**       | **85%**                                            | **76%**                                        | **79%**                                        |

### wpull & metawarc
| Полное наименование                                                 | Url                                            | Домен                               | Тип ресурса                     | Причина                         | Стратегия                 | Инструмент | Формат  | Размер  | Дата       | Статус          | Ошибка                     | Cloud Url                                                                                               | Metawarc |
| ------------------------------------------------------------------- | ---------------------------------------------- | ----------------------------------- | ------------------------------- | ------------------------------- | ------------------------- | ---------- | ------- | ------- | ---------- | --------------- | -------------------------- | ------------------------------------------------------------------------------------------------------- | -------- |
| Сайт археологических экспедиций “Археологический комплекс Гнёздово” | [https://gnezdovo.com/](https://gnezdovo.com/) | [gnezdovo.com](http://gnezdovo.com) | Сайт археологической экспедиции | Сохранение культурного наследия | Стандартная веб архивация | wpull      | warc.gz | 13.0 ГБ | 07.12.2024 | Частичный успех | Бесконечная загрузка wpull | [Google Drive](https://drive.google.com/drive/folders/1QdzpsRafqxvmgYzi3lTt-p2jlpd6-MtQ?usp=drive_link) | Ошибка   |
| Раннесредневековая археологическая экспедиция                       | [http://www.rsae.ru/](http://www.rsae.ru/)     | [rsae.ru](http://rsae.ru)           | Сайт археологической экспедиции | Сохранение культурного наследия | Стандартная веб архивация | wpull      | warc.gz | 0,27 ГБ | 07.12.2024 | Успешно         |                            | [Google Drive](https://drive.google.com/drive/folders/15sC_tTDjH5EUN3bM4OuQHLQkYwsfY9QR?usp=drive_link) | Успешно  |
| Новгородская археологическая экспедиция                             | [http://archnov.com/](http://archnov.com/)     | [archnov.com](http://archnov.com)   | Сайт археологической экспедиции | Сохранение культурного наследия | Стандартная веб архивация | wpull      | warc.gz | 1,62 ГБ | 07.12.2024 | Успешно         |                            | [Google Drive](https://drive.google.com/drive/folders/1UVGeWjW2e_PmMhHnPum7CQq6XvLYBoyf?usp=drive_link) | Успешно  |

## Лицензия
Creative Commons Zero v1.0 Universal
