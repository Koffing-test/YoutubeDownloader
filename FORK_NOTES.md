# Состояние форка

Репозиторий: `https://github.com/Koffing-test/YoutubeDownloader`

Upstream: `https://github.com/Tyrrrz/YoutubeDownloader`, ветка `prime`.

## Цель

Поддерживать нейтральный форк приложения без политических условий
использования, политических уведомлений при запуске и связанных ссылок.

MIT-лицензия и исходный copyright сохраняются согласно требованиям лицензии.
Форк не обходит DRM, авторизацию, приватность контента или ограничения,
устанавливаемые YouTube.

## Выполнено 2026-09-01

- Создан форк в аккаунте `Koffing-test` и добавлен remote `upstream`.
- Удалены политические badges, блок `Terms of use` и связанные ссылки из
  `Readme.md`.
- Удален политический диалог при запуске, его настройка и строки из всех
  локализаций.
- Ссылки на релизы, CI, автообновления, проект и metadata загруженных файлов
  направлены на `Koffing-test/YoutubeDownloader`.
- Company metadata и macOS bundle identifier переведены на форк.
- GitHub `About` очищен от исходного описания: оставлены нейтральная подпись
  `Link to download` и ссылка на последний релиз форка.
- `Readme.md` сокращен до единственной нейтральной ссылки на последний релиз;
  удалены описание, badges, внешние ссылки, изображения и скриншоты.
- Поиск по исходникам не находит удаленные тексты или идентификаторы диалога.
- `git diff --check` проходит.
- Локальная сборка не запускалась: на Mac отсутствует .NET SDK.
- GitHub Actions успешно проверил форматирование и собрал приложение для
  Windows (`x86`, `x64`, `arm64`), Linux (`x64`, `arm64`) и macOS (`x64`,
  `arm64`): `https://github.com/Koffing-test/YoutubeDownloader/actions/runs/33527128420`.

## Обновление из upstream

После каждого merge/rebase из `upstream/prime` нужно проверить, что не
вернулись `UkraineSupport`, политический блок README и upstream-настройки
автообновления:

```sh
rg -n -i "UkraineSupport|tyrrrz.me/ukraine|fuck-russia|why-so-political" .
rg -n "Tyrrrz.*YoutubeDownloader" YoutubeDownloader/Services/UpdateService.cs
```

## Резервная копия

Копия `Program.cs` перед исправлением форматирования:

`/Users/koffing/Documents/cloud/YoutubeDownloader-backups/20260901-1845-format-fix/Program.cs`
