# Sphere-Othello-Game
『**LLM で 100 万行のソフトウェア開発 III — オンライン対戦球面オセロを作る**』（3 巻）で作った、ネット対戦の球面オセロの設計書とコードです。
# 球面オセロを GitHub に載せるときの説明（Othello-Game・Donut-Othello-Game と同じ形）

## 1. リポジトリを作るフォーム（New repository）

| 欄 | 入れるもの |
|:---|:---|
| Owner | `skogita` |
| Repository name | `Sphere-Othello-Game` |
| Description | 下の英語の文（About に出ます） |
| 公開 / 非公開 | Public |
| Add a README file | オフ（README は下の 2 本を入れます） |
| Add .gitignore | なし |
| Choose a license | ほかの 2 つのリポジトリと同じにそろえる（決めるのは owner） |

**Description（英語）**

```
Spherical Othello: online two-player Othello on a sphere (hexagon cells, 12 pentagon corners that never flip). Python servers, Kotlin terminal for Windows and Android, and 120 design documents. Companion source for the book "Toward a Million Lines III".
```

**Description（日本語にするなら）**

```
球面オセロ：球の盤（六角形の升と、裏返らない 12 の五角形の隅）で、離れた 2 人が打つネット対戦のオセロ。Python のサーバ、Windows と Android の Kotlin の端末、設計書 120 本。書籍『LLM で 100 万行のソフトウェア開発 III』の付属ソース
```

**Topics（任意）**: `othello` `reversi` `kotlin` `compose-multiplatform` `python` `integration-testing` `llm`

## 2. リポジトリに入れるもの

`_配布用/sphere/` の中から、次だけを入れます。

- `docs/`（日本語の設計書 124 本）
- `src/`
- `README.md` と `README.ja.md`——**このフォルダ（`sphere_github/`）の 2 本**を使います（配布物の中の README ではありません。リポジトリには実行ファイルが無いので、ダウンロードは Releases へ案内する形にしてあります）

**入れないもの**: `prebuilt/`（EXE と APK。実行ファイルは 100MB を超え、履歴に残ると重くなります）、ZIP。

## 3. リリース（Releases → Draft a new release）

| 欄 | 入れるもの |
|:---|:---|
| Choose a tag | `v1.0`（★Donut-Othello-Game のタグは `V1.0` と大文字になっています。どちらかにそろえてください） |
| Release title | `Spherical Othello 1.0 (Windows / Android)` |
| Describe this release | 下の文 |
| Attach binaries | `_配布用/sphere_en.zip` と `_配布用/sphere.zip` の 2 本 |

**Describe this release**

```
Spherical Othello 1.0 — companion release for the book "Toward a Million Lines III — Building Spherical Othello for Online Play".

Downloads
- sphere_en.zip — English edition: English design documents and English screens. Windows app (prebuilt/windows/othello_sphere.exe) and Android APK (prebuilt/android/othello_sphere.apk).
- sphere.zip — Japanese edition (日本語版): 日本語の設計書と日本語の画面。中の並びは同じです。

Security warnings — the apps are not code-signed
- Windows: before extracting, right-click the ZIP → Properties → tick "Unblock" → OK. If "Windows protected your PC" appears, click "More info" → "Run anyway".
- Android: the APK is signed with the Android debug key. Allow "Install unknown apps" for the app you open it with.

The servers (web, engine, machine player, DB) are Python 3.11+ and are started from the command line. See README.md in the ZIP.

---

署名がないため、警告が出ることがあります。
- Windows: 展開する前に、ZIP を右クリック →「プロパティ」→「許可する」にチェック → OK。「Windows によって PC が保護されました」が出たら「詳細情報」→「実行」。
- Android: APK は debug の鍵で署名してあります。開くアプリに「提供元不明のアプリのインストール」を許してください。
```

## 4. 載せる ZIP（2026-09-23 に README を直して作り直したもの）

| ファイル | 大きさ | 中身 |
|:---|--:|:---|
| `sphere_en.zip` | 61,631,227 バイト | 484 項目・英語の設計書・英語の画面の EXE と APK |
| `sphere.zip` | 61,593,962 バイト | 484 項目・日本語の設計書・日本語の画面の EXE と APK |
