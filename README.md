# Geolonia Skill

Geolonia Maps を使った地図アプリ開発を支援する [Claude Code](https://docs.anthropic.com/en/docs/claude-code) プラグインです。

## 含まれるスキル

### maps

Geolonia Maps（MapLibre GL JS ベース）を使った地図アプリの開発を支援します。

- **Embed API**: HTML の `data-*` 属性による宣言的な地図埋め込み
- **JavaScript API**: `geolonia.Map` / `Marker` / `Popup` / `SimpleStyle` によるプログラマティックな操作
- **ジオコーディング**: Community Geocoder（住所→座標）、Reverse Geocoder（座標→住所）、住所正規化
- **マップスタイル**: 組み込みスタイル一覧とカスタマイズ方法

セットアップは CDN 埋め込みに統一しています。

## インストール

```
/plugin marketplace add geolonia/skill
/plugin install maps@geolonia
```

## ローカルでテストする

リポジトリをクローンして `--plugin-dir` フラグで直接読み込みます。

```bash
git clone git@github.com:geolonia/skill.git
```

任意のプロジェクトディレクトリで Claude Code を起動する際にプラグインを指定します:

```bash
claude --plugin-dir /path/to/skill
```

地図関連のリクエストをすると、自動的にスキルが有効化されます。`/geolonia:maps` で明示的に呼び出すことも可能です。

スキルファイルを編集した場合は、Claude Code を再起動すると変更が反映されます。
