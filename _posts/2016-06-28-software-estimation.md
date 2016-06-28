---
layout: post
title:  "Оцениваем трудозатраты на разработку правильно"
date:   2016-06-28 21:00:00 +0300
permalink: /software-estimation/
tags: [software estimation, software development]
keywords: [estimation, software]
author: nikolay-sapunov
---
Оценка проектов в&nbsp;IT&nbsp;&mdash; больная тема. Кто не&nbsp;давал невыполнимых обещаний, а&nbsp;потом не&nbsp;сидел овертайм чтобы уложиться в&nbsp;тот срок, что сам и&nbsp;озвучил?

В&nbsp;начале пути, когда давал оценку будучи разработчиком, я&nbsp;постоянно недооценивал. Каждый раз выявлялась работа, которую я&nbsp;не&nbsp;учел. Коллеги советовали умножать оценки на&nbsp;2, на&nbsp;3, на&nbsp;число&nbsp;ПИ, но&nbsp;это не&nbsp;помогало улучшить точность оценок, а&nbsp;только добавляло других проблем, например, когда нужно было объяснить, откуда взялась высокая оценка.

С&nbsp;того времени прошло 10&nbsp;лет. За&nbsp;это время я&nbsp;участвовал в&nbsp;оценке более 200&nbsp;проектов, набил много шишек и&nbsp;я&nbsp;хочу поделиться с&nbsp;вами мыслями на&nbsp;тему оценки проектов.

Надеюсь статья поможет вам улучшить качество оценок, которые вы&nbsp;даете

<!--more-->

#Зачем давать оценки?
Процент &laquo;успешных&raquo; проектов не&nbsp;превышает 29% (Исследование The Standish Group за&nbsp;2015&nbsp;год). Остальные&nbsp;71% либо провальные, либо вышли за&nbsp;рамки тройного ограничения (сроки, функционал, бюджет).

Из&nbsp;этой статистики делаем вывод, что оценка проектов часто не&nbsp;соответствует действительности. Значит&nbsp;ли это, что оценку давать нет смысла? На&nbsp;просторах интернета даже появилось движение за&nbsp;то, чтобы не&nbsp;давать никаких оценок, а&nbsp;просто писать код&nbsp;&mdash; и&nbsp;будь, что будет. Что успеем, то&nbsp;успеем (поищите по&nbsp;тегу #noestimates).

Не&nbsp;давать никаких оценок&nbsp;&mdash; звучит заманчиво, но&nbsp;давайте отвлечемся и&nbsp;представим, что вы&nbsp;заказываете такси. Вы&nbsp;спрашиваете водителя: &laquo;сколько стоит доехать до&nbsp;такой-то улицы&raquo;, а&nbsp;он&nbsp;отвечает: &laquo;не&nbsp;знаю, садись в&nbsp;машину, доедем&nbsp;&mdash; скажу, сколько заплатить по&nbsp;приезду&raquo;.

Или, например, вариант в&nbsp;стиле Agile: &laquo;Ну, мы&nbsp;будем ехать, а&nbsp;ты&nbsp;будешь платить мне каждые 10&nbsp;минут в&nbsp;дороге&nbsp;&mdash; и&nbsp;так пока не&nbsp;кончатся деньги) Как кончатся&nbsp;&mdash; высажу, но, возможно, мы&nbsp;доедем, или будем уже рядом. Ну, а&nbsp;если не&nbsp;рядом, то&nbsp;это твои проблемы&nbsp;&mdash; не&nbsp;повезло.&raquo;

Примерно так ощущают себя заказчики в&nbsp;ИТ, когда им&nbsp;предлагают начать работы без каких-либо оценок. 

В&nbsp;примере выше в&nbsp;идеале мы&nbsp;хотим получить от&nbsp;водителя точную цену, за&nbsp;которую он&nbsp;нас довезет. В&nbsp;крайнем случае, неплохо&nbsp;бы получить диапазон цен. Так мы&nbsp;сможем прикинуть&nbsp;&mdash; брать такси, ехать общественным транспортом, идти пешком или вообще никуда не&nbsp;ехать и&nbsp;остаться дома.

Лезть в&nbsp;машину, совсем не&nbsp;понимая, чего ожидать&nbsp;&mdash; не&nbsp;то&nbsp;решение, которое принимают в&nbsp;здравом уме.

Надеюсь, мне удалось убедить вас, что оценка&nbsp;&mdash; это важная составляющая для принятия решений на&nbsp;проекте. Она может быть близкой к&nbsp;реальности, а&nbsp;может быть не&nbsp;очень, но&nbsp;она нужна.

#Причина недооценивания
Давайте представим, что менеджер спрашивает разработчика, за&nbsp;сколько он&nbsp;сделает задачу. Разработчик уже делал подобное ранее и&nbsp;дает &laquo;наиболее вероятную&raquo; оценку. Пусть это будет 10&nbsp;дней.
Есть, конечно, вероятность, что задача займет 12&nbsp;дней, но&nbsp;эта вероятность ниже, чем вероятность того, что задача займет 10&nbsp;дней. Так&nbsp;же есть вероятность, что задача займет 8&nbsp;дней, но&nbsp;и&nbsp;эта вероятность будет меньше.

Часто предполагается, что оценки на&nbsp;задачу/проект распределяются по&nbsp;нормальному закону распределения (подробнее о&nbsp;нормальном распределении). И, если изобразить распределение оценок и&nbsp;их&nbsp;вероятностей в&nbsp;виде графика, то&nbsp;мы&nbsp;получим следующую картину:![](http://forasoft.github.io/assets/posts/software-estimation/Theory01.png)
Ось Х&nbsp;соответствует оценке, а&nbsp;ось Y -вероятности того, что эта оценка окажется верной, и&nbsp;задача займет именно этот срок (ни&nbsp;больше, ни&nbsp;меньше). В&nbsp;центре, как вы&nbsp;видите,&nbsp;&mdash; точка с&nbsp;наибольшей вероятностью или наиболее вероятная оценка. Эта вероятность соответствует нашей оценке в&nbsp;10&nbsp;дней.

Площадь под кривой дает суммарную вероятность в&nbsp;100%. Получается, что если мы&nbsp;дадим наиболее вероятную оценку, то&nbsp;мы&nbsp;завершим проект/задачу в&nbsp;срок или ранее с&nbsp;вероятностью в&nbsp;50% (площадь под графиком до&nbsp;оценки 10&nbsp;часов&nbsp;&mdash; это половина площади фигуры, и&nbsp;равна 50%).
Т.е., руководствуясь данным принципом и&nbsp;давая наиболее вероятную оценку мы&nbsp;должны срывать примерно&nbsp;50% сроков.

И&nbsp;это при условии, что распределение вероятности действительно соответствует нормальному распределению. При нормальном распределении вероятность закончить раньше наиболее вероятной оценки равна вероятности закончить позже нее. Но, если задуматься, на&nbsp;практике вероятность того, что что-то пойдёт не&nbsp;так, гораздо выше того, что случится чудо, и&nbsp;мы&nbsp;закончим раньше. Другими словами, суммарное значение всех негативных рисков всегда больше, чем &laquo;рисков&raquo; позитивных (возможностей).

Если учесть данное предположение, то&nbsp;получим следующее распределение:![](http://forasoft.github.io/assets/posts/software-estimation/Theory02.png)
Чтобы было нагляднее, давайте представим эту же информацию в виде кумулятивного графика, в котором будет указана вероятность завершения проекта в указанный срок или ранее:![](http://forasoft.github.io/assets/posts/software-estimation/Theory03.png)
Получается, что если взять &laquo;наиболее вероятную&raquo; оценку в&nbsp;10&nbsp;дней, то&nbsp;вероятность того, что задача будет готова в&nbsp;этот срок или раньше&nbsp;&mdash; меньше 50%. 

Итак, основная причина недооценивания&nbsp;&mdash; это неопределенность и&nbsp;игнорирование теории вероятности. Оценка, которая является &laquo;наиболее вероятной&raquo;, будет превышена с&nbsp;вероятностью более&nbsp;50%.

#Что считать хорошей оценкой?
Есть много версий ответа на&nbsp;этот вопрос, но&nbsp;на&nbsp;практике, если оценка отклоняется от&nbsp;цели проекта более чем на&nbsp;20%, то&nbsp;у&nbsp;руководителя проекта нет пространства для маневра. Если оценка колеблется в&nbsp;пределах&nbsp;20%, то&nbsp;проект можно завершить успешно за&nbsp;счет управления функциональностью, сроками, размером команды и&nbsp;другими параметрами. Это звучит достаточно разумно, поэтому давайте для примера остановимся на&nbsp;этом определении хорошей оценки (это решение должно быть принято на&nbsp;уровне организации&nbsp;&mdash; кто-то рискует, и&nbsp;их&nbsp;устраивает отклонение в&nbsp;40-50%, а&nbsp;кому-то и&nbsp;10% много). 

Итак для нас хорошей оценкой будет считаться&nbsp;та, что отличается от&nbsp;фактического результата не&nbsp;более чем на&nbsp;20%.

#Зависимость точности оценки от стадии проекта
В&nbsp;процессе работы над задачей/проектом мы&nbsp;постоянно узнаем новую информацию. Мы&nbsp;получаем фидбек от&nbsp;заказчика, менеджера, тестировщика, дизайнера и&nbsp;других участников команды. И&nbsp;все эти знания постоянно дополняются. В&nbsp;самом начале проекта/задачи нам, как правило, мало что о&nbsp;нем/ней известно. Но&nbsp;по&nbsp;ходу выполнения проекта требования все больше проясняются, и&nbsp;по&nbsp;окончании проекта мы&nbsp;уже точно знаем, что именно нужно было сделать, и&nbsp;можем точно сказать, сколько это заняло времени.
![](http://forasoft.github.io/assets/posts/software-estimation/Theory04.png)
Знания, которыми мы&nbsp;обладаем, напрямую влияют на&nbsp;точность оценки. 

Исследования Луиса Ларанхейра также показывают, что точность оценки программного проекта зависит от&nbsp;степени проясненности требований (Luiz Laranjeira 1990). Чем более прояснены требования, тем точнее оценка. Оценка не&nbsp;точна, прежде всего, потому, что неопределенность заложена в&nbsp;самом проекте/задаче. Единственным способом сокращения неопределенности в&nbsp;оценке является сокращение ее&nbsp;в&nbsp;проекте/задаче.

В&nbsp;соответствии с&nbsp;этим исследованием и&nbsp;здравым смыслом, если мы&nbsp;будем сокращать неопределенность на&nbsp;проекте/задаче, будет увеличиваться и&nbsp;точность оценки.![](http://forasoft.github.io/assets/posts/software-estimation/Theory05.png)
Данный график приведен для наглядности, и&nbsp;в&nbsp;реальности наиболее вероятная оценка может изменяться в&nbsp;процессе сокращения неопределенности.

Луис Ларанхейр в&nbsp;своем исследовании пошел дальше и&nbsp;выявил численную зависимость того, как разброс оценки зависит от&nbsp;стадии проекта (уровня неопределенности). 

Если взять оптимистичную, пессимистичную и&nbsp;наиболее вероятную оценки (оптимистичная оценка&nbsp;&mdash; это самый ранний срок сдачи из&nbsp;всех возможных, пессимистичная&nbsp;&mdash; самый поздний) и&nbsp;показать, как отношение между ними меняется со&nbsp;временем, от&nbsp;начала проекта до&nbsp;его завершения, то&nbsp;получится следующая картина:![](http://forasoft.github.io/assets/posts/software-estimation/Theory06.png)
Эта фигура называется конусом неопределенности. Горизонтальная ось соответствует времени от&nbsp;начала работы над проектом до&nbsp;его завершения. На&nbsp;ней отмечены основные этапы проекта.
На&nbsp;вертикальной оси отмечается относительная величина ошибки в&nbsp;оценке.

Так, на&nbsp;стадии исходной концепции наиболее вероятная оценка может отличаться от&nbsp;оптимистической в&nbsp;4&nbsp;раза. На&nbsp;стадии готового&nbsp;UI разброс оценки уже варьируется от&nbsp;0,8 до&nbsp;1,25 относительно наиболее вероятной оценки.

Очень важная деталь&nbsp;&mdash; конус не&nbsp;сужается автоматически с&nbsp;течением времени. Для того, чтобы он&nbsp;сужался, нужно действительно управлять проектом и&nbsp;предпринимать конкретные действия, направленные на&nbsp;снижение неопределенности. Если вы&nbsp;целенаправленно не&nbsp;снижаете неопределенность по&nbsp;ходу выполнения проекта, то&nbsp;ваши дела будут выглядеть примерно так:![](http://forasoft.github.io/assets/posts/software-estimation/Theory07.png)
Область выделенная голубым называется облаком неопределенности. На&nbsp;протяжении всего проекта оценка подвержена большим отклонениям вплоть до&nbsp;самого завершения работ. 

Чтобы продвинуться по&nbsp;конусу в&nbsp;самую правую точку, где нет неопределенности, нам нужно создать готовый продукт :) Получается, пока продукт не&nbsp;готов, неопределенность есть всегда, и&nbsp;оценка не&nbsp;может быть точной на&nbsp;100%. Но&nbsp;на&nbsp;точность оценки можно повлиять, снижая неопределенность. При этом, **любое действие, направленное на&nbsp;снижение неопределенности, снижает разброс оценки**.

Данную модель используют во&nbsp;многих компаниях, в&nbsp;том числе и&nbsp;в&nbsp;NASA. Некоторые адаптируют&nbsp;ее, чтобы учитывать нестабильность требований. Более детально об&nbsp;этом можно прочитать в&nbsp;&laquo;Software Estimation: Demystifying the Black Art&raquo;.
#Практика. Оцениваем проект на разных стадиях
Давайте представим, что к&nbsp;вам пришел менеджер проекта и&nbsp;попросил оценить какую-то функцию или проект. 

Первым делом нужно изучить доступные требования и&nbsp;понять, на&nbsp;каком этапе жизненного цикла находится описание задачи или проекта (Исходная концепция, Согласованное определение, Завершенные требования, Готов UI, Спроектирована архитектура).

Дальнейшие действия зависят от&nbsp;того, на&nbsp;каком этапе мы&nbsp;находимся:

##Стадия 1. Исходная концепция
Если к&nbsp;вам приходит менеджер или клиент и&nbsp;спрашивает: &laquo;Сколько времени займет сделать приложение, где доктора будут консультировать пациентов?&raquo;, то&nbsp;вы&nbsp;точно на&nbsp;этапе &laquo;Исходная концепция&raquo;.
###Когда имеет смысл давать оценку на данном этапе?
На&nbsp;стадии предпродажи. Когда ну&nbsp;очень нужно определить, стоит&nbsp;ли обсуждать проект далее. Вообще-то, оценок на&nbsp;этом этапе лучше избегать и&nbsp;сначала стараться снизить неопределенность, чтобы перейти на&nbsp;следующий этап жизненного цикла проекта.

###Что нужно, чтобы дать оценку на данном этапе?
Нужно иметь данные фактических трудозатрат по&nbsp;похожему завершенному проекту.

###Какие инструменты больше всего подходят на данном этапе?
* Оценка по&nbsp;аналогии

###Алгоритм оценки
На&nbsp;самом деле, дать оценку на&nbsp;сам проект на&nbsp;данном этапе не&nbsp;получится. Можно только сказать, сколько времени ушло на&nbsp;другой похожий проект.

Например, оценку можно озвучить как &laquo;Я&nbsp;не&nbsp;знаю сколько времени займет этот проект, так как данных недостаточно, но&nbsp;чем-то похожий на&nbsp;него проект&nbsp;Х занял&nbsp;Y времени. Чтобы дать хотя&nbsp;бы примерную оценку по&nbsp;данному проекту, нужно прояснить требования.&raquo;

Если данных по&nbsp;похожим завершенным проектам нет, то&nbsp;единственный возможный вариант дать оценку&nbsp;&mdash; снижать неопределенность и&nbsp;переходить на&nbsp;следующий этап.
###Как перейти на следующий этап?
Для этого нужно прояснить требования, чтобы было понятно, зачем нужно приложение и&nbsp;какие функции оно будет выполнять. 

В&nbsp;идеале нужно иметь навыки сбора и&nbsp;анализа требований.

Для того, чтобы повысить свои навыки в&nbsp;сборе и&nbsp;анализе требований, неплохо&nbsp;бы прочитать &laquo;Разработка требований к&nbsp;программному обеспечению&raquo; Карл И. Вигерс, Джой Битти

Для сбора первичных требований вы&nbsp;можете воспользоваться следующим опросником:

* Для чего нужно приложение? Какие проблемы оно будет решать?
* Какие типы пользователей будут пользоваться приложением? (для задачи, озвученной выше&nbsp;&mdash; это, скорее всего, Врач, Пациент, Администратор)
* Какие проблемы каждый тип пользователей сможет решать в&nbsp;приложении?
* На&nbsp;каких платформах будет работать приложение?

После выяснения этих деталей у&nbsp;вас должна сформироваться картина приложения, какие проблемы оно должно решать, и&nbsp;каким образом. Это будет означать, что переход на&nbsp;следующий этап состоялся.
##Стадия 2. Согласованное определение продукта
На&nbsp;данном этапе уже есть понимание, что приложение будет делать и&nbsp;что не&nbsp;будет. Хотя и&nbsp;без подробных деталей.

###Когда имеет смысл давать оценку на данном этапе?
Опять&nbsp;же, на&nbsp;стадии предпродажи. Когда нужно принять решение о&nbsp;том, имеет&nbsp;ли смысл вообще делать этот проект/задачу, хватает&nbsp;ли денег на&nbsp;него, приемлемы&nbsp;ли сроки реализации. 
Стоит&nbsp;ли та&nbsp;ценность, которую принесет проект, тех ресурсов, которые нужно будет вложить.

###Что нужно, чтобы дать оценку на данном этапе?
Нужно иметь историю завершенных проектов с&nbsp;оценкой, либо богатый опыт разработки в&nbsp;той сфере, к&nbsp;которой относится оцениваемый проект. А&nbsp;лучше&nbsp;&mdash; и&nbsp;то, и&nbsp;другое вместе.

###Какие инструменты больше всего подходят на данном этапе?

* Оценка по&nbsp;аналогии
* Оценка сверху вниз

###Алгоритм оценки
Если такой&nbsp;же проект уже делали, то&nbsp;можно сразу озвучить в&nbsp;качестве примерной оценки то&nbsp;время, которое ушло на&nbsp;тот проект.

Если данных по&nbsp;такому проекту нет, то&nbsp;нужно разбить проект на&nbsp;основные функциональные блоки, а&nbsp;затем каждый блок оценить по&nbsp;методу аналогии с&nbsp;блоками, которые делались на&nbsp;других проектах.

Так, например, в&nbsp;случае с&nbsp;приложением &laquo;где доктора будут консультировать пациентов&raquo; у&nbsp;нас могло&nbsp;бы получиться следующее:

* Регистрация
* Система записи на&nbsp;прием
* Система уведомлений
* Видео консультации
* Система отзывов
* Система оплаты

И&nbsp;для оценки блока &laquo;Регистрация&raquo; можно взять оценку с&nbsp;одного проекта, а&nbsp;для оценки блока &laquo;Система отзывов&raquo;&nbsp;&mdash; с&nbsp;другого.

Если есть блоки, которые никогда не&nbsp;делались, либо данных по&nbsp;ним нет, можно либо оценить трудозатраты на&nbsp;них относительно других блоков, либо снизить неопределенность и&nbsp;использовать метод оценки со&nbsp;следующего этапа.

Так, например, модуль &laquo;Система отзывов&raquo; может нам показаться в&nbsp;2&nbsp;раза сложнее модуля &laquo;Регистрация&raquo;. Соответственно, для этого модуля мы&nbsp;можем взять оценку, в&nbsp;2&nbsp;раза превышающую оценку на&nbsp;модуль &laquo;Регистрация&raquo;.

Этот метод (оценка одного блока относительно другого блока) очень не&nbsp;точный, и&nbsp;его лучше использовать, только если количество блоков, которые никогда не&nbsp;делались, не&nbsp;превышает&nbsp;20% от&nbsp;блоков, по&nbsp;которым есть исторические данные. В&nbsp;противном случае, это будет гадание на&nbsp;кофейной гуще.

После этой процедуры оценку по&nbsp;всем блокам нужно сложить, и&nbsp;это будет наиболее вероятная оценка. Пессимистичную и&nbsp;оптимистичную оценки можно рассчитать, используя коэффициенты, которые соответствуют текущему этапу&nbsp;&mdash; х0,5 и&nbsp;х2 (см. таблицу коэффициентов).

В&nbsp;идеале, это уже можно озвучить менеджеру, он&nbsp;должен разобраться, что с&nbsp;этим делать.

Если&nbsp;же так случилось, что разобраться менеджер не&nbsp;может и&nbsp;просит одно число&nbsp;&mdash; есть способы дать и&nbsp;одно.

Как из&nbsp;3-х оценок (пессимистичная, оптимистичная и&nbsp;наиболее вероятная) сделать одну, я&nbsp;расскажу позже в&nbsp;разделе &laquo;Как из&nbsp;3-х оценок получить одну?&raquo;.
###Как перейти на следующий этап?
Чтобы перейти на&nbsp;следующий этап, нужно подготовить полный список требований. Есть много разных способов документирования, но&nbsp;мы&nbsp;рассмотрим распространенный вариант с&nbsp;User Story.

Для каждого блока нужно определить, кто им&nbsp;будет пользоваться и&nbsp;что конкретно будет делать там.

Так, например, для блока &laquo;Система отзывов&raquo; после сбора и&nbsp;анализа требований мы&nbsp;могли&nbsp;бы получить следующее:

* Пациент может просмотреть все отзывы о&nbsp;выбранном докторе
* Пациент может оставить отзыв доктору после видео консультации с&nbsp;ним
* Доктор может видеть список отзывов, которые ему оставили пациенты
* Доктор может написать комментарий к&nbsp;отзыву на&nbsp;свою консультацию
* Администратор может видеть список всех отзывов на&nbsp;сайте
* Администратор может редактировать выбранный отзыв на&nbsp;сайте
* Администратор может удалять выбранный отзыв на&nbsp;сайте

Также нужно собрать и&nbsp;записать все не&nbsp;функциональные требования к&nbsp;проекту. Чтобы собрать&nbsp;их, можно воспользоваться следующим чек-листом:

* На&nbsp;каких платформах должно работать?
* Какие операционные системы нужно поддерживать?
* С&nbsp;чем нужно интегрироваться?
* Как быстро должно работать?
* Сколько пользователей должно поддерживать одновременно?

Прояснение этого будет означать переход на&nbsp;следующий этап.
##Стадия 3. Требования собраны и проанализированы
На&nbsp;данном этапе есть полный список того, что может делать каждый пользователь в&nbsp;системе, а&nbsp;также есть список не&nbsp;функциональных требований.

###Когда имеет смысл давать оценку на данном этапе?

Когда нужно дать примерную оценку на&nbsp;проект перед стартом работы по&nbsp;модели T&amp;M. Оценки задач с&nbsp;данного этапа могут быть использованы для приоритизации конкретных задач на&nbsp;проекте, для планирования даты релиза и&nbsp;бюджета всего проекта.
Также их&nbsp;можно использовать для контроля производительности команды на&nbsp;проекте и&nbsp;оценке ее&nbsp;эффективности.

###Что нужно, чтобы дать оценку на данном этапе?

* Список функциональных требований
* Список не&nbsp;функциональных требований

###Какие инструменты больше всего подходят на данном этапе?

* Оценка снизу вверх
* Оценка по&nbsp;аналогии

###Алгоритм оценки
Нужно разбить каждую задачу на&nbsp;составляющие (провести декомпозицию). При этом, чем мельче вы&nbsp;разобьете, тем более точную оценку вы&nbsp;получите. 

Чтобы сделать это наилучшим образом, нужно представить все, что нужно сделать для реализации данной задачи. Можно мысленно, но&nbsp;лучше на&nbsp;бумажке.

Например, для нашей User Story &laquo;Пациент может просмотреть все отзывы о&nbsp;выбранном докторе&raquo; могла&nbsp;бы получиться следующая картина (иллюстрации ниже специально сделаны от&nbsp;руки, чтобы показать, как процесс оценки может выглядеть на&nbsp;практике):

![](http://forasoft.github.io/assets/posts/software-estimation/Practice01.png)

Тут мы&nbsp;разделили задачу на&nbsp;3&nbsp;составляющие:

* Создать инфраструктуру в&nbsp;базе данных
* Сделать уровень DAL, для выборки данных
* Сделать&nbsp;UI, где будут выводится сами отзывы

Если есть возможность, для задач, которые включают в&nbsp;себя интерфейс пользователя, можно прикинуть интерфейс функционала от&nbsp;руки и&nbsp;согласовать его с&nbsp;тем, кто просит оценку. Это сразу отбросит множество вопросов, повысит точность оценки и&nbsp;облегчит вам жизнь в&nbsp;будущем.

Если вы&nbsp;хотите повысить свои навыки в&nbsp;проектировании интерфейсов, неплохо&nbsp;бы прочитать &laquo;Интерфейс&raquo; Джеф Раскин и&nbsp;&laquo;Об&nbsp;интерфейсе. Основы проектирования взаимодействия&raquo; Алан Купер.

Далее нужно представить, что именно будет делаться для каждой задачи и&nbsp;оценить, сколько времени это займет. На&nbsp;этом этапе нужно именно подсчитать время, а&nbsp;не&nbsp;угадать. Вы&nbsp;должны представлять себе, что вы будете делать для реализации каждой подзадачи. 

![](http://forasoft.github.io/assets/posts/software-estimation/Practice02.png)

Если есть задачи, которые занимают более 8&nbsp;часов, их&nbsp;нужно разбить на&nbsp;подзадачи.

Оценку, которую вы&nbsp;получили после описанной процедуры, можно считать оптимистической, так как, скорее всего, она учитывает кратчайший путь из&nbsp;точки&nbsp;А в&nbsp;точку&nbsp;Б (при условии, что вы&nbsp;ничего не&nbsp;забыли). 

Теперь самое время подумать о&nbsp;тех вещах, которые&nbsp;вы, возможно, пропустили, и&nbsp;скорректировать свою оценку. В&nbsp;таких случаях, как правило, помогает чек-лист. Вот пример такого листа:

* Тестирование
* Дизайн
* Создание тестовых данных
* Поддержка разных разрешений экрана
* ...


После прохода по&nbsp;этому списку нужно дополнить список задач тем, что, возможно было пропущено:
![](http://forasoft.github.io/assets/posts/software-estimation/Practice03.png)

После этого нужно пройтись по&nbsp;каждой задаче и&nbsp;подзадаче и&nbsp;подумать, что могло&nbsp;бы пойти не&nbsp;так, какие ошибки могут возникнуть, что мы&nbsp;пропустили. Как правило, в&nbsp;процессе данного анализа выявляются, в&nbsp;том числе, и&nbsp;вещи, без которых и&nbsp;наилучший случай (оптимистическая оценка) невозможен. Их&nbsp;нужно добавить к&nbsp;вашей оценке.
![](http://forasoft.github.io/assets/posts/software-estimation/Practice04.png)

После того, как вы&nbsp;и&nbsp;это подсчитаете&nbsp;&mdash; ваша оценка, скорее всего, будет все ещё ближе к&nbsp;оптимистичной, чем к&nbsp;наиболее вероятной. Если посмотреть на&nbsp;конус, то&nbsp;эта оценка будет ближе к&nbsp;нижней его грани. 

![](http://forasoft.github.io/assets/posts/software-estimation/Theory08.png)

Исключение может быть в&nbsp;том случае, если вы&nbsp;уже делали подобную задачу ранее и&nbsp;можете точно утверждать, что знаете, как ее&nbsp;делать, и&nbsp;сколько времени она занимала ранее. В&nbsp;этом случае ваша оценка могла&nbsp;бы называться &laquo;наиболее вероятной&raquo; и&nbsp;соответствовала&nbsp;бы прямой 1х&nbsp;на&nbsp;конусе. В&nbsp;противном случае ваша оценка&nbsp;&mdash; оптимистичная.

Оставшиеся две оценки можно рассчитать, используя коэффициенты, которые соответствуют текущему этапу&nbsp;&mdash; х0,67 и&nbsp;х1,5 (см. таблицу коэффициентов).

Если подсчитать оценку и&nbsp;приведенного выше примера, мы&nbsp;получим следующее:

* Оптимистическая оценка&nbsp;&mdash; 14&nbsp;часов
* Наиболее вероятная&nbsp;&mdash; 20&nbsp;часов
* Пессимистическая&nbsp;&mdash; 31&nbsp;час

###Как перейти на следующий этап?

Чтобы перейти на&nbsp;следующий этап, нужно спроектировать интерфейс пользователя. Лучшим способом сделать это будет создание wireframes.

Для этого есть множество программ, но&nbsp;я&nbsp;бы порекомендовал обратить внимание на&nbsp;Balsamiq и&nbsp;Axure RP.

Прототипирование&nbsp;&mdash; это отдельная обширная тема, которая выходит за&nbsp;рамки данной статьи.

Наличие wireframe будет означать переход на&nbsp;следующий этап.

##Стадия 4. Интерфейс спроектирован
На&nbsp;данном этапе есть wireframe и&nbsp;полный список того, что может делать каждый пользователь в&nbsp;системе, а&nbsp;также есть список не&nbsp;функциональных требований.

###Когда имеет смысл давать оценку на данном этапе?
Для подготовки точной оценки по&nbsp;модели Fixed Price, но&nbsp;также можно и&nbsp;для всего того, что было перечислено на&nbsp;прошлом этапе.

###Что нужно, чтобы дать оценку на данном этапе?

* Готовые wireframes
* Список функциональных требований
* Список не&nbsp;функциональных требований

###Какие инструменты больше всего подходят на данном этапе?

* Оценка снизу вверх
* Оценка по&nbsp;аналогии

###Алгоритм оценки

Такой&nbsp;же, как и&nbsp;на&nbsp;предыдущем этапе. Разница состоит в&nbsp;точности. Имея спланированный интерфейс, вам гораздо меньше придётся додумывать, и&nbsp;вероятность что-то не&nbsp;учесть будет гораздо меньше.

###Как перейти на следующий этап?
Спроектировать всю архитектуру приложения и&nbsp;детально продумать будущую реализацию. Этот вариант мы&nbsp;рассматривать не&nbsp;будем, так как он&nbsp;довольно редко используется на&nbsp;практике. При этом алгоритм оценки после продумывания архитектуры не&nbsp;будет отличаться от&nbsp;алгоритма текущего этапа. Разница, опять&nbsp;же, будет в&nbsp;повышении точности.
##Получаем из диапазона оценок одну
Если у&nbsp;вас уже есть наиболее вероятная, пессимистическая и&nbsp;оптимистическая оценки, то&nbsp;для того, чтобы получить одну оценку, можно использовать наработки Тома ДеМарко, который в&nbsp;своей книге &laquo;Вальсируя с&nbsp;медведями&raquo; поднял идею, что абсолютная вероятность может быть вычислена путём интегрирования площади под кривой (того самого графика асимметричного распределения вероятностей, что мы&nbsp;рисовали ранее). Оригинальный шаблон для подсчета можно скачать тут (также доступен без регистрации тут). В&nbsp;шаблон нужно просто подставить 3&nbsp;числа и&nbsp;получить результат в&nbsp;виде списка оценок с&nbsp;соответствующими им&nbsp;вероятностями. 

Например, для оценок 14, 20&nbsp;и&nbsp;31&nbsp;мы получим следующий результат (скрин с&nbsp;шаблона excel):

![](http://forasoft.github.io/assets/posts/software-estimation/Screen01.png)

Вы&nbsp;можете выбрать любую вероятность, которую посчитаете приемлемой для своей организации, но&nbsp;я&nbsp;хотел&nbsp;бы вспомнить про пример, который приводит Вильям Дункан (основной автор базовых версий PMBoK), когда рассказывает про риски:

&laquo;Предположим, вы&nbsp;решили сыграть в&nbsp;русскую рулетку. Вы&nbsp;берете револьвер, закладываете один патрон, проворачиваете барабан, приставляете револьвер к&nbsp;виску и&nbsp;нажимаете на&nbsp;спусковой крючок... Какова вероятность выжить при игре в&nbsp;русскую рулетку? 5/6, или (грубо) 83&nbsp;%... &raquo;. 

Учитывая этот пример, я&nbsp;бы советовал брать 85%&nbsp;&mdash; одного патрона более чем достаточно).
#Не знаем как оценить - говорим
Если вы&nbsp;не&nbsp;знаете, что от&nbsp;вас хотят, либо не&nbsp;знаете, как именно реализовывать функционал, который вас просят оценить&nbsp;&mdash; то&nbsp;в&nbsp;этом случае лучше честно сказать об&nbsp;этом менеджеру, дать ему примерную оценку (если вообще возможно) и&nbsp;предложить ему конкретные действия, чтобы эту оценку уточнить. 

Например, если вы&nbsp;не&nbsp;знаете, подходит&nbsp;ли технология для реализации задачи&nbsp;&mdash; попросите время на&nbsp;то, чтобы сделать прототип, который либо подтвердит вашу оценку, либо покажет, что вы&nbsp;что-то упустили. Если вы&nbsp;не&nbsp;уверены, что задачу вообще можно решить&nbsp;&mdash; скажите об&nbsp;этом сразу. Такие вещи лучше проверять до&nbsp;того, как вы&nbsp;взяли на&nbsp;себя обязательства.

Очень важно давать менеджеру эту информацию, иначе он&nbsp;может взять вашу оценку на&nbsp;веру, и&nbsp;даже не&nbsp;подозревать, что есть вероятность сорвать срок в&nbsp;5&nbsp;раз или вообще не&nbsp;сделать продукт на&nbsp;данной технологии&nbsp;/ с&nbsp;данными требованиями.

Хороший менеджер всегда на&nbsp;вашей стороне, ведь вы&nbsp;в&nbsp;одной лодке, и&nbsp;его карьера зависит от&nbsp;того, уложитесь&nbsp;ли вы&nbsp;в&nbsp;срок, зачастую сильнее, чем ваша.

#Сомневаемся - не обещаем
Многие организации и&nbsp;разработчики сами способствуют срыву собственных проектов только за&nbsp;счет того, что принимают на&nbsp;себя обязательства в&nbsp;слишком ранней точке конуса неопределенности. На&nbsp;ранней стадии, где возможный результат колеблется от&nbsp;100% до&nbsp;1600%, принимать решения и&nbsp;фиксировать сроки очень рискованно. 

Эффективные организации и&nbsp;разработчики откладывают принятие на&nbsp;себя обязательств до&nbsp;того момента, как будет выполнена работа по&nbsp;сужению конуса.

Как правило, это характерно для организаций, находящихся на&nbsp;более зрелом уровне модели CMM, в&nbsp;которых процедуры сужения конуса явно описаны и&nbsp;соблюдаются.

Ниже приводится иллюстрация улучшения качества оценок в&nbsp;проектах ВВС США при переходе на&nbsp;более зрелый уровень CMM (Lawlis, Flowe and Thodahl,1995).![](http://forasoft.github.io/assets/posts/software-estimation/Theory09.png)
Думаю, тут есть о&nbsp;чем задуматься. Статистика по&nbsp;другим компаниям подтверждает эту корреляцию.

При этом, точность оценки не&nbsp;достигается одними только методами оценки, она неразрывно связана с&nbsp;эффективностью управления проектами и&nbsp;зависит не&nbsp;только от&nbsp;разработчиков, но&nbsp;и&nbsp;от&nbsp;менеджеров проекта и&nbsp;высшего руководства компании.

#Выводы

* Дать оценку, которая совпадет с&nbsp;действительностью практически невозможно, но&nbsp;в&nbsp;ваших силах повлиять на&nbsp;диапазон, в&nbsp;котором она будет колебаться. Для этого нужно снижать неопределенность на&nbsp;проекте.
* Дробление задач на&nbsp;составляющие поможет повысить точность вашей оценки. В&nbsp;процессе декомпозиции вы&nbsp;более детально продумаете, что будете делать и&nbsp;как.
* Используйте чек листы, чтобы снизить вероятность что-нибудь пропустить при оценке.
* Используйте конус неопределенности для того чтобы понять в&nbsp;каком диапазоне вероятнее всего будет колебаться ваша оценка 
* И&nbsp;напоследок&nbsp;&mdash; постоянно сравнивайте ту&nbsp;оценку, которую вы&nbsp;дали, со&nbsp;временем, которое реально ушло на&nbsp;задачу. Это поможет вам прокачать свой навык оценки, понять, что вы&nbsp;упустили, и&nbsp;использовать это в&nbsp;последующих оценках.

#Полезные книги
На&nbsp;тему оценки трудозатрат очень много литературы, но&nbsp;я&nbsp;приведу 2&nbsp;книги, которые просто обязаны быть прочитаны:

* &laquo;Вальсируя с&nbsp;Медведями: управление рисками в&nbsp;проектах по&nbsp;разработке программного обеспечения&raquo; Том деМарко и&nbsp;Тимоти Листер
* &laquo;Software Estimation: Demystifying the Black Art&raquo; Steve McConnell