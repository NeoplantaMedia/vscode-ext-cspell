# vscode-ext-cspell

Custom dictionaries settings for [_Code Spell Checker_](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) extension for _VSCode_ editor.

<br>

## Instructions

Inside an empty _.vscode_ directory, which is placed in a project root directory, run the following on a command line:

    git clone --depth 1 https://github.com/NeoplantaMedia/vscode-ext-cspell.git . && rm -rf .git && rm .gitignore LICENSE README.md

Inside the _.vscode_ directory, in the _cspell_dictionaries_ directory, add new words to the already defined dictionaries or [add a new dictionary](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker#project-workspace-dictionary-using-cspell.json) and then register it under _dictionaryDefinitions_ entry, in the _cspell.json_ file.

Defined dictionaries from the _cspell_dictionaries_ directory, can be then added to the [already assigned dictionaries](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker#dictionaries) of a programming language, in the _cspell.json_ file, under _languageSettings_ entry. A dictionary can be also added to the list under _dictionaries_ entry, which means that it will be used for every file type.

File types that are being spell checked are listed in the _cspell.json_ file, under _enableFiletypes_ entry. The process of adding or removing a file type is described [here](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker#enable-disable-file-types).

<br>

## Other Settings

Words that should always be considered correct but are specific only to a _workspace_, can be added to the _VSCode's_ workspace _settings.json_ file, in the _.vscode_ directory, under _cSpell.words_ entry:

```
{
  "cSpell.words": ["word1", "word2"]
}
```

Global words that should always be considered correct in every project, can be added to the _VSCode's_ user _settings.json_ file, under _cSpell.userWords_ entry:

```
{
  "cSpell.userWords": ["word1", "word2"]
}
```

Change the way spelling errors are reported, choosing between _error_, _warning_, _information_ and _hing_, in the _VSCode's_ user _settings.json_ file, under _cSpell.diagnosticLevel_ entry:

```
{
  "cSpell.diagnosticLevel": "Error"
}
```

Directories and files that should not be spell checked can be added to the _VSCode's_ user _settings.json_ file, under _cSpell.ignorePaths_ entry:

```
{
  "cSpell.ignorePaths": ["**/build/", "**/package.json"]
}
```

About these and other settings, read [on the extension page](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) or search for the _cspell_ in the _VSCode_ _Settings_ search bar.
