Конфигуратор
============

## Опции для настройки

| Опция             | Описание                                                          | Тип данных    | Стандартное значение                          |
|-------------------|-------------------------------------------------------------------|---------------|-----------------------------------------------|
|socialNetworks     |Массив с настройками драйверов социальных сетей                    |array          |-                                              |
|options            |HTML аттрибуты для ссылки                                          |array          |-                                              |
|enableSeoOptions   |Вкл/выкл добавление SEO аттрибутов для ссылки                      |bool           |true                                           |
|seoOptions         |SEO аттрибуты для ссылки                                           |array          |`['target' => '_blank', 'rel' => 'noopener']`  |
|enableDefaultIcons |Вкл/выкл использование иконок вместо текстовых лэйблов             |bool           |false                                          |
|icons              |Ассоциативный массив с именем класса драйвера и селектором иконки  |array          |Используется стандартный набор иконок          |

## Примеры конфигурации

### icons

```php
'icons' => [
    \ymaker\social\share\drivers\Twitter::class => 'icon-twitter', // CSS класс
    \ymaker\social\share\drivers\Facebook::class => 'icon-facebook',  // CSS класс
],
```

## Создание своего конфигуратора

Если вы хотите создать свой конфигуратор, вам нужно:

1. Создать класс и унаследовать его от `\yii\base\BaseObject` или `\yii\base\Component` 
2. Реализовать интерфейс [ConfiguratorInterface](https://github.com/yiimaker/yii2-social-share/blob/master/src/configurators/ConfiguratorInterface.php)
3. Реализовать методы этого интерфейса