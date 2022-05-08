# gh-pages 

Устанавливаем `npm install gh-pages --save-dev`

Добавляем `"deploy": "gh-pages -d dist"` в `scripts` в `package.json`.

Если добавить еще `"predeploy": "npm run build"`, то командой `npm run deploy` можно обновлять gh-pages локально.

## CI

В github интерфейсе репозитория в Settings | Actions | General в блоке Workflow permissions надо включить `Read and write permissions`

Секрет `GITHUB_TOKEN` [создастся](https://docs.github.com/en/actions/security-guides/automatic-token-authentication) автоматиически.

Создаем папки `.github/workflows`, в ней файл `.github/workflows/gh-pages-workflow.yml`

Содержимое файла аналогичное в этой репе. После этого любой пуш в указанные ветки будет паблишить папку в gh-pages.
