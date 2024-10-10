В ходе предыдущего задания был развернут статический сайт следующего вида
![1](https://github.com/user-attachments/assets/ecdb2616-1f28-4757-94d9-f2ca5ae7c8b3)

Стандартная информация MkDocs в данном сайте была заменена
![2](https://github.com/user-attachments/assets/11c1e828-28f2-4e8f-91d7-970218298e8c)


В качестве кастомной стилизации было выбрано решение подключить CSS файл со стилизацией
![8](https://github.com/user-attachments/assets/cf56db4f-e10c-4a34-bc35-1dbcdd24a616)
![9](https://github.com/user-attachments/assets/7cef0eca-6027-4a4b-b41c-35fc73dd8d29)


Кроме того были добавлены мета тег с именем автора, стилизованы заголовки и footer
![16](https://github.com/user-attachments/assets/e5744220-704b-4471-8e94-0c3f8f02d406)
![6](https://github.com/user-attachments/assets/58630be7-8402-46ca-b662-7b79133d52b1)
<img width="764" alt="image" src="https://github.com/user-attachments/assets/39510069-aaf1-41ce-a14f-fa1fa2ce1795">


На основе <a href = "https://github.com/nzhukov/deploy-ghactions/tree/main">репозитория</a>
быа создана цепочка пайплайнов для для тестирования и
сборки статики  — фронтэнда сайта, а затем построения собственно самого сайта
и деплоя его на GitHub Pages, при этом была предусмотрена возможность сборки с помощью PostCss.


Таким образом при отправке пул реквеста/вливании кода происходит установка зависимостей, сборка проекта,
обработка стилей с помощью PostCss, минификация HTML, CSS, JS, минимизация JS, тестирование, а также валидация HTML.


Можно описать каждую команду более подробно в виде таблицы:
| Команда                              | Описание                                                                 |
|--------------------------------------|--------------------------------------------------------------------------|
| `npm ci`                             | Устанавливает все зависимости проекта, определенные в `package.json`.   |
| `npm run build`                      | Запускает сборку проекта с помощью Webpack.                             |
| `npm run styles`                    | Обрабатывает CSS файлы с помощью PostCSS, импортирует и минимизирует.  |
| `npm run minify-html`               | Минимизирует HTML файлы в директории `dist`.                            |
| `npm run minify-css`                | Минимизирует основной CSS файл, создавая `style.min.css`.              |
| `npm run minify-js`                 | Минимизирует JavaScript файл, создавая `script.min.js`.                |
| `npm test`                          | Запускает тесты проекта с помощью Jest.                                 |
| `npm run validate-html`              | Проверяет HTML файл на соответствие стандартам.                         |


Сборка проекта была проверена локально, ошибок при сборке не возникло

![14](https://github.com/user-attachments/assets/a18ac42e-2819-4266-a7f0-13c401d0b5a5)

При размещении на Github ошибок также не возникло, этапы сборки соответствуют командам пайплайна
![17](https://github.com/user-attachments/assets/fb6afab2-76bb-4a20-a413-81bbeedc5ac4)
![18](https://github.com/user-attachments/assets/172339e4-8c2d-4ebe-812f-c6368fc143cc)


Собранный сайт размещен на Github pages, URL: <a href = "https://murzin66.github.io/Second_Practice/src/index"> https://murzin66.github.io/Second_Practice/src/index</a>
