# node_1
# Typescript-Intro

## Wofür ist Typescript da?

Typescript ist eine Programmiersprache. Sie erweitert Javascript und eine Vielzahl von Funktionalitäten. Es handelt sich um ein sogenanntes "Superset"; das bedeutet, dass JS-Code auch gülter TS-Code ist.
Browser können nativ nicht mit TS arbeiten. Daher muss TS in einem Zwischenschritt zu JS umgewandelt werden (das geschieht mittels eines Compilers).

Typescript bringe einige Vorteile mit sich:

- striktere Typisierung als JS
- unterstützt moderne JS Featrues, die noch nicht von allen Browsern unterstützt werden müssen
- bringt eigene Features mit sich (Generics, Types, etc.)

## Installation

Um Typescript nutzen zu können, empfiehlt es sich [Node.js](https://nodejs.org/en) herunterzuladen, um damit auf dem Node-Package-Manager (npm) zugreifen zu können.
Nach vollständiger Installaltion von Node.js und npm kann Typescripüt global auf unserem Computer mittels `npm i -g typescript` installiert werden. (Achtung! Dieser Weg KANN in ferner Zukunft zu Problemen führen. Behalte im Kopf, dass wir Typescript global installiert haben!)

Weiterhin benötigen wir Visual Studio Code und eine Erweiterung namens "Live Server" von Ritwick Dey.

Es kann vorkommen, dass Powershell uns nicht erlaubt, Skripte auszuführen. In diesem Fall müssen wir die Ausführung von Skripten erlauben. Das machen wir mittels `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned`.

## Entwicklung

Wenn wir den TS-Compiler anweisen wollen, die TS-Dateien in JS-Dateien umzuwandeln, machen wir das mittels `tsc DATEINAME`. Der Befehl `tsc DATEINAME -w` werden Änderungen live compiled.

## tsconfig.json

In der tsconfig.json können wir die Einstellungen für den TS-Compiler festlegen. So können wir beispielsweise den Output-Ordner festlegen, den Target, den Module, etc.
Die tsconfig.json kann mittels `tsc --init` erstellt werden.

In den meisten Fällen reicht es aus, die Einstellungen `target`, `module`, `outDir`, `rootDir` und `strict` zu setzen. Als zusätzliche Einstellung empfiehlt es sich die Eigenschaft `include` zu setzen, um den TS-Compiler anzuweisen, welche Dateien er kompilieren soll.

Für `target` empfiehlt sich `es6`, für `module` empfiehlt sich `es2015`, für `outDir` empfiehlt sich `./dist`, für `rootDir` empfiehlt sich `./src` und für `strict` empfiehlt sich `true`. `include` sollte auf `["src/**/*"]` gesetzt werden.

## Module

In Typescript können wir Module verwenden. Ein Modul ist eine Sammlung von Funktionen, Klassen, etc., die wir in anderen Dateien verwenden können. Ein Modul kann exportiert und importiert werden.

Ein Modul wird mittels `export` exportiert und mittels `import` importiert.

Wenn wir Module in unserer html-Datei verwenden wollen, müssen wir die JS-Dateien in die html-Datei einbinden. Das machen wir mittels `<script type="module" src="DATEI.js"></script>`.

## Dateistruktur

Es empfiehlt sich, die Dateien in einem bestimmten Ordner zu strukturieren. In einem Ordner `src` können wir unsere TS-Dateien ablegen. In einem Ordner `dist` können wir unsere JS-Dateien ablegen. In einem Ordner `public` können wir unsere html-Dateien ablegen.