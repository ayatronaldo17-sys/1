# Custom Subtitles (Fabric, Minecraft 1.21.11)

Заменяет ванильные субтитры своими:
- цвет текста и цвет фона (hex), прозрачность фона, тень
- 8 позиций на экране + смещение X/Y
- список звуков, которые можно скрыть (или маска: `subtitles.entity.zombie.*`)
- макс. число строк, время показа

Настройки: ModMenu -> Custom Subtitles -> настроить. Файл: `config/customsubtitles.json`.
Субтитры должны быть включены в Настройки -> Звук.

## Сборка
Нужны JDK 21 и интернет.
1. Скачай шаблон на https://fabricmc.net/develop (MC 1.21.11, Mojang mappings), возьми оттуда gradlew + gradle/wrapper
   и актуальные версии loom/loader в gradle.properties, либо поставь Gradle 9.x и выполни `gradle wrapper`.
2. `./gradlew build`
3. Готовый мод: `build/libs/customsubtitles-1.0.0.jar` (не *-sources.jar)

## Сборка без установки (GitHub Actions)
Залей содержимое папки в новый репозиторий на GitHub -> вкладка Actions -> build -> Artifacts -> customsubtitles-jar.
(Если сборка упадёт на версиях loom/loader/Gradle, поправь их по fabricmc.net/develop.)
