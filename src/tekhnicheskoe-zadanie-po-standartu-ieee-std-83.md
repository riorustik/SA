# Техническое задание по стандарту IEEE STD 830-1998   
Название проекта: "Виртуальная примерка одежды с использованием ИИ по фото"
   
# 1. ВВЕДЕНИЕ   
## 1.1  Назначение   
Сайт будет предоставлять пользователям возможность загружать свои фотографии и изображения одежды (или выбирать их из каталога) для виртуальной примерки, моделируя, как одежда будет выглядеть с учетом телосложения пользователей.   
## 1.2 Область действия   
Разрабатываемая программная система называется системой виртуальной примерки одежды с использованием искусственного интеллекта, по фото. Она предназначена для конечных пользователей - клиентов заинтересованных в формировании своего внешнего образа, а также визуального ознакомления перед покупкой одежды. Эта система будет служить инструментом для улучшения клиентского опыта при онлайн-покупках. Система будет находиться в свободном доступе, каждый пользователь сможет воспользоваться сервисом через браузер.    
Виртуальной примерки одежды позволит пользователям загружать фотографии своих тел и одежды, для создания виртуальных образов, которые можно сохранять в галерее пользователя, которая включает альбомы сгенерированных образов, личных фотографий и фотографий одежды. В случаи отсутствия фотографий пользователя, на платформе будут доступны несколько вариантов одежды как для мужчин, так и для женщин, подготовленных администрацией сайта. По мимо этого, люди разного телосложения смогут выбрать один из вариантов готовых пресетов, подходящих под их параметры.    
**Коммерческое использование**: Использование для коммерческих целей возможно только по договору или платной подписке.   
## 1.3  Определения, акронимы и сокращения   
- **ПО** — Программное обеспечение.   
- **ИИ** — Искусственный интеллект.   
- **API** — Интерфейс прикладного программирования (Application Programming Interface).   
- Галерея — Один из основных разделов сайта, для хранения альбомов   
- Альбом — Элемент раздела "Галерея", для хранения фотографий пользователя.   
- Образ — сгенерированное изображение, являющее результатом работы виртуальной примерке.   
   
## 1.4  Краткий обзор   
Документ описывает общие требования к проекту, включая описание функциональных и нефункциональных требований, интерфейсов и ограничений.   
# 2. Общее описание   
## 2.1  Взаимодействие продукта   
Сайт является независимым и полностью самодостаточным сервисом, на котором пользователи могут загружать как свои фотографии, так и изображения одежды для виртуальной примерки. ИИ будет автоматически анализировать фотографии и накладывать изображение одежды на фото пользователя, с учетом его формы тела и пропорций.   
## 2.2 Разделы сайта   
Система на стороне клиента имеет 3 основных раздела сайта.   
### 1 раздел - Генерация изображения   
Представляет из себя страничку генерации изображения и является главной страницей [4.1]. Здесь пользователь может выбрать изображение одежды и пресет соответствующий параметрам тела пользователя или же загрузить свои фотографии. После выбора или загрузки, пользователь нажимаю кнопку "Сгенерировать образ", начинает процесс виртуальной примерки, в котором ИИ совместит одежду на изображении выбранном или загруженном пользователем.   
### 2 раздел - Галерея пользователя   
Представляет из себя страничку состоящую из альбомов пользователя представленных в виде плиток [4.2]. Здесь пользователь может создавать новые альбомы, удалять уже имеющие. Выбирая альбом, пользователь попадает хранилище фотографий, которые также представлены в виде плиток, пользователю доступно скачивание изображений, удаление выбранных фотографий, а также загрузка фотографий в выбранный альбом.   
### 3 раздел - Личный кабинет пользователя   
Представляет из себя страничку с личной информацией пользователя, а также с информацией для входа. Тут же пользователю доступен функционал удаления аккаунта пользователя [4.1]. Пользователь может изменить свои данные и данные для входа. В случаи удаления аккаунта необходимо подтвердить свои действия.   
## 2.3  Функции продукта (краткое описание)
   
**Создание аккаунта пользователя **- функция позволяет новым пользователям зарегистрироваться на платформе, предоставляя им доступ к функционалу сервиса. Эта функция включает в себя сбор необходимых данных, проверку введенной информации и подтверждение успешной регистрации.   
**Удаление аккаунта пользователя **- функция позволяет пользователям полностью удалить свою учетную запись с сервиса виртуальной примерки. Это обеспечивает пользователей правом управлять своими данными и конфиденциальностью, предоставляя возможность прекращения использования сервиса.   
**Загрузка фотографий** - функция позволяет пользователям загружать свои фотографии и фотографии одежды в сервис виртуальной примерки. Это предоставит пользователям свободу в формировании образов.   
**Сохранение фотографий в галереи** - функция позволяет сохранять фотографий пользователя и одежды в альбомах пользователя для последующего использования в виртуальной примерке.   
**Генерация образа** - функция позволяет, комбинируя изображения загруженные пользователем и представленные в каталоге, создавать изображения с учетом анатомических особенностей, визуализируя, как выбранная одежда будет выглядеть на них без необходимости физически примерять её.   
**Сохранение образа в галереи** - функция позволяет пользователям сохранять результаты виртуальной примерки в альбомы. Это делает доступ к ранее созданным образам быстрым и удобным, позволяя пользователям легко просматривать и управлять своими образами.
   
**Скачивания образа** - функция позволяет пользователям скачивать изображения с результатами виртуальной примерки одежды. Это позволит пользователям удобно сохранять результаты для дальнейшего использования при планировании будущих покупок.   
**Управление альбомами** - функция позволяет пользователю создавать, редактировать и удалять альбомы для хранения и организации фотографий. Эта функция предоставляет пользователям гибкость в управлении и упрощает процесс выбора и доступа к образам.   
## 2.4  Характеристики пользователя   
Продукт предназначен для пользователей старше 16 лет.   
Учитывая широкий охват аудитории данного веб-сервиса, необходимо учитывать, уровень навыков работы за компьютером и в сети интернет. Для использования сервиса по виртуальная примерка одежды пользователю необходимо иметь базовые навыки:   
  Умение использовать компьютеры - навыки запуска устройства и необходимых программных продуктов, для выхода в сеть.   
  Навыки навигации по веб-сайтам и приложениям.   
## 2.5  Ограничения   
**Ограничения на количество сохранённых фотографий в галереи **- пользователь может хранить до 100 фотографий в своих альбомах. Превышение этого лимита приведёт к необходимости удаления старых образов для добавления новых, что обуславливается экономией места на сервере.   
**Ограничения по географическому расположению - с**истема может быть недоступна в определённых регионах или странах из-за ограничений по лицензированию ИИ-технологий или локальных законов о защите данных.   
**Ограничения по использованию данных - в**се данные пользователей (фото, персональные данные) хранятся в соответствии с Федеральный закон "О персональных данных" от 27.07.2006 N 152-ФЗ.
   
# 3 Детальные требования   
## 3.1  Функциональные требования   
### Функция виртуальной примерки одежды
   
Функция виртуальной примерки одежды в сервисе позволяет пользователям примерять одежду на собственные фотографии в реальном времени с применением искусственного интеллекта. Это улучшает пользовательский опыт, позволяя им визуализировать, как выбранная одежда будет выглядеть на них без необходимости физически примерять её.   
**Основные требования**   
- Пользователь должен иметь возможность загружать фотографию своего тела.   
- Пользователь должен иметь возможность загружать фотографию одежды без лишних элементов на изображении.   
- Пользователь может выбирать одежду из предварительно загруженного каталога.   
- Возможность фильтрации и сортировки одежды по категориям, размерам, стилям и цветам.   
- Виртуальная примерка должна иметь ограничение по времени генерации, не более 20 секунд.    
- Результат должен обеспечивать реалистичное отображение одежды на фотографии пользователя.   
   
**Ограничения:**   
- Виртуальная примерка поддерживает только два предмета одежды на одно генерируемое изображение.   
- Система может некорректно работать с одеждой, которая частично или полностью перекрыта другими предметами на изображении.   
- Для успешной работы системы пользователь должен загружать фотографии в фронтальной позе (лицом к камере), так как ИИ-модели оптимизированы для обработки именно таких изображений.   
- Изображения с профилями или в движении, а так же с множеством объектов на фотографиях могут приводить к ошибкам в работе системы или снижению качества генерируемого образа.   
- Минимальные разрешения: 800x600 пикселей - изображение с меньшим разрешением могут быть отклонены, так как они не обеспечивают достаточную чёткость для работы ИИ-алгоритмов.   
   
### Функция создания аккаунта пользователя   
Функция создания аккаунта позволяет новым пользователям зарегистрироваться на платформе, предоставляя им доступ к функционалу сервиса. Эта функция включает в себя сбор необходимых данных, проверку введенной информации и подтверждение успешной регистрации. Данная функция должна быть реализована с учетом всех стандартов безопасности и соответствовать GDPR для обработки личных данных пользователей.   
**Основные требования**   
1. **Сбор данных**   
    - Имя (обязательное поле)   
    - Фамилия (обязательное поле)   
    - Адрес электронной почты (обязательное поле, должен быть уникальным и валидным)   
    - Пароль (обязательное поле, должен соответствовать требованиям безопасности)   
    - Номер телефона (необязательное поле, должен быть уникальным при наличии)   
    - Дата рождения (необязательное поле, в формате ДД.ММ.ГГГГ)   
2. **Валидация данных **   
    - Электронная почта должна соответствовать формату и быть уникальной.   
    - Пароль должен содержать не менее 8 символов, включать заглавные и строчные буквы, цифры и специальные символы.   
    - Номер телефона должен соответствовать заданному формату (например, +7XXXXXXXXXX для России).   
    - Дата рождения должна быть в корректном формате и не превышать текущую дату.   
3. **Обработка ошибок**   
    - В случае возникновения ошибок при регистрации (например, уже зарегистрированный адрес электронной почты, невалидный формат ввода и т.д.), пользователю должны быть выданы соответствующие сообщения об ошибках с пояснениями.   
   
### Функция удаления аккаунта пользователя
   
Функция удаления аккаунта позволяет пользователям полностью удалить свою учетную запись в сервисе виртуальной примерки. Это обеспечивает пользователей правом управлять своими данными и конфиденциальностью, предоставляя возможность прекращения использования сервиса. Данная функция должна быть реализована с учетом всех стандартов безопасности и соответствовать GDPR для обработки личных данных пользователей.   
**Основные требования**   
- В случае возникновения ошибок при удалении пользователю должны быть выданы соответствующие сообщения об ошибках с пояснениями.   
- После успешного удаления аккаунта, пользователю отображается страница входа с сообщением о завершении процесса. Также предоставляется информация о том, что аккаунт и все связанные данные были полностью удалены.   
- При подтверждении удаления пользователю сообщается, что все данные, включая сохраненные образы и личные настройки, будут безвозвратно удалены, восстановление аккаунта будет невозможным после удаления.   
- Необходимо реализовать меры безопасности, чтобы предотвратить случайное или несанкционированное удаление аккаунта (например, необходимость подтверждения через электронную почту или SMS).   
- Пользователь может инициировать процесс удаления аккаунта через настройки профиля. Для этого требуется выбрать опцию «Удалить аккаунт».   
   
### Функция загрузки фотографий
   
Функция позволяет загружать фотографии непосредственно в процессе генерации образа (один из этапов) или же загружать фотографии в альбомы в разделе "Галерея" для хранения и последующего использования.   
**Основные требования**   
- Допустимые форматы изображений: JPEG, PNG, WEBP.   
- Загружать фотографии со своего устройства в альбом.   
- Реализовать механизм аутентификации пользователя при загрузке файлов, чтобы избежать несанкционированного доступа.   
- В случае ошибок загрузки (например, превышение размера файла, неверный формат, проблемы с сетью) пользователю должны быть предоставлены сообщения об ошибках.   
   
### Функция сохранения фотографий 
   
Функция позволяет пользователям сохранять загруженные и сгенерированные фотографии для последующего использования в виртуальной примерке.   
**Основные требования**   
- Сохранить фотографии в альбомы после генерации изображения.   
- Выбрать, в какой альбом галереи будет сохранен образ.   
- Сохранить загруженные фотографии в альбомы после генерации изображения.   
- Имя изображения генерируется в формате "ГГГГ-ММ-ДД ЧЧ-ММ-СС".   
- В случае возникновения ошибок (например, проблемы с загрузкой, недоступность сервера) пользователю должны отображаться соответствующие сообщения.   
   
### Функция скачивания изображений
   
Данная функция предоставляет пользователям возможность скачивать изображения с результатами виртуальной примерки одежды, а также изображения ранее загруженные пользователем.   
**Основные требования**   
1. **Выбор изображения для скачивания**   
    - После завершения виртуальной примерки у пользователя будет возможность скачать изображение.   
    - Пользователь может скачать изображение из альбома пользователя.   
2. **Форматы изображений**   
    - JPEG (JPG): Высококачественное сжатие, оптимально для веба и общего использования.   
    - PNG: Поддерживает прозрачность, идеально для наложения изображений.   
3. **Процесс скачивания**   
    - По нажатию кнопки «Скачать» изображение буде сохраняться на устройстве пользователя.   
    - Пользователь получит уведомление о завершении загрузки (например, всплывающее окно или сообщение на экране).   
    - Имя изображения генерируется в формате "ГГГГ-ММ-ДД ЧЧ-ММ-СС".   
   
### Функция управления альбомами
   
Функция позволяет пользователям создавать, редактировать и удалять альбомы для хранения и организации фотографий и сгенерированных образов.   
**Основные требования**   
- Создать новый альбом, выбрав опцию «Создать альбом» в разделе "Галерея". Для создания альбома необходимо указать название (обязательно).   
- Просматривать сохранённые фотографии в альбомах.   
- Редактировать название альбомов.   
- Удалить альбом с подтверждением, что все изображения и данные, связанные с ним, будут безвозвратно удалены.   
- Сохранять свои альбомы на устройство в формате ZIP.   
- Изменения порядка изображений в альбоме с помощью сортировки по дате создания.   
- Фотографии должны отображаться в альбоме в виде плиток.   
- Удалять отдельные изображения.   
   
## 3.2 Интерфейсы пользователя   
**Страница регистрации и входа**   
  **Функциональность **Пользователи могут зарегистрироваться, войти или восстановить пароль.   
  **Обязательные поля и элементы интерфейса **   
    - Для регистрации необходимы Имя (обязательное поле), Фамилия (обязательное поле), Адрес электронной почты (обязательное поле, должен быть уникальным и валидным), Пароль (обязательное поле, должен соответствовать требованиям безопасности), Подтверждение пароля (должен обязательно соответствовать уже указанному), Дата рождения (необязательное поле, в формате ДД.ММ.ГГГГ), Номер телефона (необязательное поле, должен быть уникальным при наличии).    
    - Для входа необходимы Электронная почта или Номер телефона, Пароль.    
    - Для восстановления пароля необходима Электронная почта.   
  **Элементы управления **Кнопки "Регистрация", "Войти", "Восстановить пароль".    
  **UI/UX **Простота и минимализм интерфейса. Поля должны быть валидированы и визуально выделены как при корректном вводе так и при возникновении ошибки в полях (корректность email, длина пароля).   
  **Уведомления **Сообщения об ошибках или успешных действиях (например, ошибка входа).   
**Интерфейс виртуальной примерки (главная страница)**   
  **Функциональность **Пользователи могут загружать или выбирать изображения для визуализации одежды. Для генерации необходимы две фотографии из каталога, загруженные пользователем или выбранные из альбома пользователя. Выбор пресетов из каталога должен быть визуально обозначен.   
  **Элементы управления **Кнопка "Сгенерировать образ".   
  **UI/UX **Простота и минимализм интерфейса. Каталог одежды и анатомических пресетов представлен в виде бокового меню. Основная часть окна должна содержать сгенерированный образ пользователя.   
  **Уведомления  **Сообщения об ошибках или успешных действиях (например, загрузки фотографий или генерации).   
**Интерфейс загрузки изображений**   
  **Функциональность **Пользователи могут загружать фото в альбомы или для непосредственной генерации (фото пользователя, фото одежды).   
  **Форматы **Поддержка JPG и PNG форматов.   
  **Элементы управления **Кнопка "загрузить фото", кнопка "загрузить одежду".   
  **UI/UX **Простота и минимализм интерфейса. При нажатии на кнопки загрузки  одежды и фото пользователя открывается стандартное диалоговое окно выбора изображений. Поддержка перетаскивания файлов (drag-and-drop).   
  **Уведомления **Сообщения об ошибках (например, превышение размера файла, неподдерживаемый формат).   
**Интерфейс личного кабинета пользователя**   
  **Функциональность **Пользователи могут просмотреть и изменить свои личные данные, а также данные входа или удалить свой аккаунт.   
  **Обязательные поля и элементы интерфейса **Поля -  Имя (обязательное поле), Фамилия (обязательное поле), Адрес электронной почты (обязательное поле, должен быть уникальным и валидным), Пароль (обязательное поле, должен соответствовать требованиям безопасности), Дата рождения (необязательное поле, в формате ДД.ММ.ГГГГ), Номер телефона (необязательное поле, должен быть уникальным при наличии).    
  **Элементы управления **Кнопки "Сохранить", кнопка "Удалить аккаунт"   
  **UI/UX **Простота и минимализм интерфейса. Поля должны быть валидированы и визуально выделены как при корректном вводе так и при возникновении ошибки в полях (корректность email, длина пароля, пустое поле).   
  **Уведомления **Сообщения об ошибках или успешных действиях.   
**Интерфейс галереи пользователя**   
  **Функциональность **Управление альбомами пользователя. Возможность добавления, удаления и редактирования альбомов. Возможность сортировки (по дате, названию, количеству изображений)   
  **Элементы управления **кнопка добавления нового альбома, меню редактирования альбома, выпадающий список сортировок    
  **UI/UX **простота и минимализм интерфейса. Альбомы представлены в виде сетки плиток.   
  **Уведомления **Сообщения об ошибках или успешных действиях (например, ошибка создания нового альбома).   
**Интерфейс альбома пользователя**   
  **Функциональность **Управление изображениями в альбомах пользователя. Пользователь может загружать, скачивать и удалять изображения. Для удаления пользователю необходимо нажать кнопку выбрать и отметить фотографий которые он хочет удалить, после чего нажать кнопку удаления.    
  **Элементы управления **кнопка "скачать",  выпадающий список сортировок изображений, кнопка загрузки изображений, кнопка удаления фотографий.   
  **UI/UX **простота и минимализм интерфейса. Фотографии могут быть представлены в виде плиток. Выбор конкретного изображения, должен визуально выделять. Если пользователь выбрал какое то фото, оно должно масштабироваться для более детального просмотра.    
  **Уведомления **сообщения об ошибках или успешных действиях (например, ошибка загрузки изображения).   
## 3.3  Требования к производительности   
- Максимальная нагрузка на серверы: 10,000 одновременных пользователей.   
- Обработка запросов должна поддерживать масштабирование для минимизации задержек при пиковых нагрузках [пункт 3.4.2].   
- Система должна эффективно использовать доступные серверные мощности (процессоры, оперативную память, графические процессоры) для обработки ИИ-алгоритмов и поддерживать возможность масштабирования через балансировку нагрузки.   
   
## 3.4  Нефункциональные требования   
### 3.4.1 Безопасность
   
- Все данные, передаваемые между клиентом и сервером, должны быть шифрованы.   
- Поддержка двухфакторной аутентификации для защиты аккаунтов.   
- Пароль должен храниться в зашифрованном виде.   
- Защиты от брутфорс-атак.   
- Предотвращение автоматической регистрации.   
   
### 3.4.2 Масштабируемость   
**Автоматическое масштабирование**   
  - **Требование**: Веб-сервис должен поддерживать автоматическое масштабирование серверов для обработки изображений и работы с данными в зависимости от нагрузки (например, увеличение числа активных пользователей).   
**Балансировка нагрузки**   
  - **Требование**: Система должна использовать балансировщики нагрузки для распределения запросов между несколькими серверами, чтобы избежать перегрузки одного узла.   
### 3.4.3 Отказоустойчивость   
**Отказ системы** — это ситуация, при которой сервис не может выполнять свои основные функции или работает с серьезными сбоями. Время безотказной работы должно составлять не менее 99,5%. Должны быть предусмотрены механизмы резервного копирования данных (изображений и метаданных) с возможностью их восстановления в случае отказа системы. Для веб-сервиса отказами будут считаться следующие случаи:
   
- **Критические отказы**   
    Полная недоступность сайта.   
    Ошибки авторизации, которые мешают всем пользователям войти в систему.   
    Ошибки работы ИИ или невозможность выполнить основную функцию виртуальной примерки.   
- **Средние отказы**   
    Частичная недоступность функций (например, сбой в загрузке изображений, но остальные функции работают).   
    Медленная работа сайта, которая сильно ухудшает пользовательский опыт, но не делает сайт полностью недоступным.   
- **Минорные отказы**   
    Небольшие визуальные ошибки или сбои, не мешающие выполнению основных функций.   
    Ошибки, связанные с отдельными пользователями или данными.   
   
## 3.5  Другие требования   
**Ограничение по поддерживаемым браузерам - с**истема оптимизирована для работы в последних версиях браузеров Google Chrome, Mozilla Firefox, Safari и Microsoft Edge. Работа в старых версиях браузеров или других менее популярных браузерах может сопровождаться ошибками отображения или некорректной работой функционала.
**Минимальная версия браузера для корректной работы** - Chrome 80+, Firefox 70+, Safari 13+, Edge 20+.   
- Веб-приложение должно быть адаптировано для работы на всех современных браузерах (Chrome, Firefox, Edge, Safari).   
- Обязательная поддержка мобильных устройств для отображения сайта на смартфонах и планшетах (адаптивный дизайн).   
   
# 4 Приложения   
## 4.1 Раздел "Генерация образа" (главная страница)   
![{ADBE2EC9-44D6-45B8-AB70-0AC06AB6EBAC}.png](files\adbe2ec9-44d6-45b8-ab70-0ac06ab6ebac.png)    
## 4.2 Раздел "Галерея"    
   
## 4.3 Раздел "Аккаунт"   
   