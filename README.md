# Лабораторная работа №12. Введение в Bootstrap
Цель работы:
- Познакомиться с CSS-фреймворком Bootstrap 5
- Освоить систему сеток (Grid System)
- Научиться использовать готовые компоненты Bootstrap

- Поспать
- Покушать
- [x]Сделать лабу по ИСРПО

## Что мы изучили?

### Подключение Bootstrap
Существует два основных способа подключения Bootstrap:
- Через CDN (Content Delivery Network) — быстрый способ
- Локальная установка через npm — для продакшн-проектов

```html
 <!-- Bootstrap CSS-->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-sRIl4kxILFvY47J16cr9ZwB07vP4J8+LH7qKQnuqkuIAvNWLzeN8tE5YBujZqJLB" crossorigin="anonymous" />
    <link rel="stylesheet" href="custom.css" />
```

```html
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js" integrity="sha384-
FKyoEForCGlyvwx9Hj09JcYn3nv7wiPVlz7YYwJrWVcXK/BmnVDxM+D2scQbITxI" crossorigin="anonymous">
</script>
```

**Важные моменты:**
- **Bootstrap CSS** подключается перед вашими стилями
- **Bootstrap JS** подключается в конце body для оптимизации загрузки
- *bootstrap.bundle.min.js* включает **Popper.js** для работы всплывающих элементов
- **integrity** - это механизм Subresource Integrity (SRI) или более простыми
словами хэш содержимого файла (Bootstrap JS). **Браузер:**
- скачивает файл с CDN,
- вычисляет его хэш,
- сравнивает с указанным в integrity.
- Если файл подменён или повреждён → скрипт не выполнится.
---
**crossorigin** - Разрешает браузеру:
- загружать ресурс с другого домена,
- не передавая cookies или данные авторизации.

### Система сеток Bootstrap (Grid System)
**Grid System** — это основа адаптивной верстки в **Bootstrap**. Она основана на **flexbox** и позволяет создавать адаптивные макеты с 12 колонками.
---
**Основные концепции:**
- Container — контейнер для содержимого (.container или .container-fluid)
- Row — строка, содержащая колонки (.row)
- Column — колонка (.col, .col-6, .col-md-4 и т.д.)
---
**Breakpoints (контрольные точки):**
| Класс| Размер экрана| Устройство|
|----|----|----|
|(none)|<576px|Extra small (телефоны)|
|sm|≥576px|Small (телефоны в ландшафте)|
|md|≥768px |Medium (планшеты)|
|lg|≥992px|Large (ноутбуки)|
|xl|≥1200px|Extra large (десктопы)|
|xxl |≥1400px|Extra extra large (большие мониторы)|
---
**Описание использованных Bootstrap-стилей:**
**Контейнер и заголовок**
- **.container** — центрированный контейнер с отступами
- **.mt-5** — большой верхний отступ
- **.mb-4** — средний нижний отступ
**Сетка (Grid System)**
- **.row** — строка для колонок
- **.col** — колонка с автоматической шириной
- **.col-[число]** — колонка с фиксированной шириной (из 12 частей)
- **.col-[breakpoint]-[число]** — адаптивная колонка (например, col-md-6)
**Цвета и фон**
- **.bg-*** — цвет фона (primary, secondary, success, danger, warning, info)
- **.text-white** / **.text-dark** — цвет текста
**Отступы и рамки**
- **.p-3** — средние внутренние отступы (padding)
- **.border** — тонкая рамка вокруг элемента
- **.mb-2** — маленький нижний отступ
**Адаптивные классы (Пример 3)**
- **col-12** — на мобильных: 100% ширины
- **col-md-6** — на планшетах: 50% ширины
- **col-lg-3** — на десктопах: 25% ширины
**Ключевые особенности:**
- **12-колоночная система** — вся ширина делится на 12 частей
- **Адаптивность** — классы работают от мобильных к десктопам
- **Готовые стили** — цвета, отступы, типографика
- **Flexbox-основа** — автоматическое выравнивание и распределение