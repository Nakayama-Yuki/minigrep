# minigrep

テキストファイルから指定した文字列を含む行を検索するコマンドラインアプリです。

## 実行方法

Rust（rustup）をインストールし、このディレクトリで実行します。

```sh
cargo run -- nobody poem.txt
```

引数は「検索文字列」「ファイルのパス」の順です。通常は大文字と小文字を区別します。区別せず検索する場合は、環境変数 `IGNORE_CASE` を設定します。

```sh
IGNORE_CASE=1 cargo run -- NOBODY poem.txt
```

## テスト

```sh
cargo test
```

## Rustの更新

使用するRustのバージョンは `rust-toolchain.toml` で固定しています。Dependabotが月1回、新しいバージョンを確認し、更新があればPRを作成します。PRをマージすると更新が反映されます。Cargoの依存ライブラリも月1回確認します。
