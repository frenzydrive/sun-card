# Home assistant Sun card
Home assistant Sun card based on Google weather design

## Preview
![Light mode preview](https://github.com/frenzydrive/sun-card/blob/main/preview/light.png?raw=true)
![Dark mode preview](https://github.com/frenzydrive/sun-card/blob/main/preview/dark.png?raw=true)

## Requirements
- Для работы карточки необходима установленная [Sun integration](https://www.home-assistant.io/integrations/sun/)

## Установка
### Через HACS(БОЛЬШЕ НЕ РАБОТАЕТ)
Home assistant Sun card доступна основном репозитории HACS. Подробная информация [тут](https://hacs.xyz/).

### ВРУЧНУЮ
1. Скачать файл [home-assistant-sun-card.js](https://github.com/frenzydrive/sun-card/releases/tag/v0.1.4) и сохранить его в папку `configuration/www`.
1. В Home Assistant зайти в `Configuration > Lovelace dashboard > Resources` и нажать `Add resource`.
    1. Добавить `/local/community/home-assistant-sun-card.js` в URL.
    1. Выбрать `Javascript Module` в качестве "Resource type".

## Настойка
### Через UI
1. GЗайти в dashboard, включить "edit mode" и нажать `Add card`, найти в списке `Custom: Sun card`.
1. В UI редакторе можно настроить параметры карточки добавляя параметры, которые описаны ниже.

ВАЖНО: Если `Custom: Sun card` не появилась в списке карточек, необходимо почистить кэш браузера.

### Через YAML
1. Необходимо добавить новую карточку с параметром `type: 'custom:sun-card'`.

Важно: Если появляется ошибка `Custom element doesn't exist`, необходимо почистить кэш браузера.

## Config
| Название      | Принимаемое значение | Описание.                            | Параметр по умолчанию                                   |
|---------------|----------------------|--------------------------------------|---------------------------------------------------------|
| darkMode      | `boolean`            | Темный или светлый тип карточки.     | Использует параметры Home Assistant                     |
| language      | `string`<sup>1</sup> | Язык карточки                        | Языка Home assistant или english если не поддерживается |
| showAzimuth   | `boolean`            | Displays azimuth in the footer       | `false`                                                 |
| showElevation | `boolean`            | Displays elevation in the footer     | `false`                                                 |
| timeFormat    | `'12h'`/`'24h'`      | Displayed time format                | Locale based on Home assistant language                 |
| title         | `string`             | Card title                           | Doesn't display a title by default                      |

(<sup>1</sup>) Поддерживаемые языки: `da`, `de`, `en`, `es`, `et`, `fi`, `fr`, `hu`, `it`, `nl`, `pl`, `pt-BR`, `ru`, `sl`, `sv`
