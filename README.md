# LangChain×Streamlit×RAGによるチャットボットアプリ 🤖

このプロジェクトは、LangChainとStreamlitを使用して構築されたRAG（Retrieval-Augmented Generation）ベースのチャットボットアプリケーションです。PDFドキュメントをアップロードし、その内容について質問応答を行うことができます。

> [!NOTE]
> 解説記事をQiitaに投稿しています。
> [LangChain×Streamlit×RAGによるチャットボットアプリを開発してみた](https://qiita.com/so-engineer/items/588bd7ff0482ea3fe57f)

## 特徴

このアプリケーションは、以下の特徴を持つ対話型AIチャットボットです。

- PDFドキュメントのアップロード機能
- インタラクティブなチャットインターフェース
- 会話履歴の保持と表示
- カスタマイズ可能な設定
  - AIモデルの選択（GPT-3.5/GPT-4）
  - temperatureの調整
  - チャンクサイズの調整

## 技術スタック

- Python
- Streamlit
- LangChain
- OpenAI GPT
- ChromaDB（ベクトルデータベース）
- PyMuPDF（PDF解析）

## セットアップ

1. リポジトリのクローン
```bash
git clone https://github.com/so-engineer/lc_sl_chatbot.git
```

2. プロジェクトのルートディレクトリで以下のコマンドを実行
```bash
cd lc_sl_chatbot
docker compose up -d
```

## 使用方法

1. ブラウザで http://localhost:8501 にアクセス

2. OpenAI APIキーの準備

3. ブラウザで表示されるインターフェースで以下の操作を行う
   - OpenAI APIキーを入力
   - 使用するモデルとパラメータを選択
   - PDFファイルをアップロード
   - チャットインターフェースで質問を入力

## プロジェクト構造

```
.
├── app.py               # アプリケーションのメインコード
├── requirements.txt     # プロジェクトの依存関係
├── LICENSE              # MITライセンス
├── .gitignore           # Gitの除外設定
├── .data/               # ベクトルデータベースの保存ディレクトリ
├── Dockerfile           # Docker設定ファイル
└── compose.yaml         # Docker Compose設定ファイル
```

## その他

API利用料やセキュリティには十分注意してください。