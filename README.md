# Monento Locales

This repository contains localisation resources for [Monento](https://monento.com) – a cross-platform app for tracking personal finances with encrypted data syncing.

You are welcome to contribute a new translation and fix mistakes in existent messages. 

## File Structure

Locale files are located under `locales` directory, example:

```
.i18n-editor-metadata
locale--comments.json
locale-en.json
locale-ru.json
```

Where:

* `.i18n-editor-metadata` – a configuration file for [i18n-editor](https://github.com/jcbvm/i18n-editor).
* `locale--comments.json` – the file contains comments and context details for translation terms.
* `locale-*.json` – these files contain translated terms per a locale.

## Editing Files

Locale files are plain JSON files and can be edited directly by a text editor or Github's online editor for quick fixes (we are using 2-space formatting for JSON).

However it is more convenient to use [i18n-editor](https://github.com/jcbvm/i18n-editor) – it is a cross-platform GUI editor running on Java 8:

- Follow [instructions](https://github.com/jcbvm/i18n-editor#requirements) and install at least **2.0.0-beta.1** version from its [releases](https://github.com/jcbvm/i18n-editor/releases) page.
- Open the editor and import `locales` directory as a new project.

*Note*: Start the editor by `java -jar i18n-editor.jar` command in a terminal in case it cannot be launched by its binary files.

## Guidelines

### Messages

* Message identifiers must begin with `i18n.` prefix.
* Most of messages are single-line line string.
* Some messages can contain new lines or HTML tags. These cases should be marked by comments.

### Variables and pluralisation

[MessageFormat.js](https://messageformat.github.io/messageformat/) library is used to pass variables into messages and to make pluralised variations of numerical values. Please take a look to [Format Guide](https://messageformat.github.io/messageformat/page-guide).

*Note:* Currently, value formatters of MessageFormat are not supported including date, duration, time and number.

## Contributors

You can add yourself to `contrubutors.json` file while making changes. People from the file will be listed in the application in alphabetical order.

Fields:

* `name` – required field
* `email` – optional field
* `url` – optional field

