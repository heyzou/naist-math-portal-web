# NAIST指定教科書（数学）解答集 販促ポータルサイト

このリポジトリは、NAIST（奈良先端科学技術大学院大学）の院試数学（線形代数・解析入門）の自作解答集を紹介・販売するためのポータルサイト一式です。

## 構成
- `index.html`: メインのランディングページ
- `styles.css`: アカデミック・ミニマルなデザインを定義するスタイルシート

## PDFサンプルの差し替え方法
1. `naist-math-web` ディレクトリ内に `samples` フォルダを作成します。
2. 作成したフォルダにサンプルPDF（例：`linear_algebra_sample.pdf`, `analysis_sample.pdf`）を配置します。
3. `index.html` 内の `<!-- Embed sample ... -->` とコメントされている箇所、または `pdf-preview` クラスの div 内を以下のように修正します。

```html
<div class="pdf-preview">
    <embed src="samples/linear_algebra_sample.pdf" type="application/pdf" width="100%" height="100%">
</div>
```

## GitHub Pagesへのデプロイ手順
1. この `naist-math-web` ディレクトリの内容を GitHub のリポジトリに push します。
2. GitHub リポジトリの **Settings** > **Pages** に移動します。
3. **Build and deployment** > **Branch** で `main` (または `master`) ブランチの `/ (root)` を選択し、**Save** をクリックします。
4. 数分後、`https://<YOUR_USERNAME>.github.io/<REPO_NAME>/` にてサイトが公開されます。

## 数式の記述（MathJax）
本サイトには MathJax が導入されています。`index.html` 内で以下のように記述することで数式をレンダリングできます。

- インライン表示: `$E = mc^2$`
- ブロック表示: `$$ \int_a^b f(x) dx $$`

## ライセンス
本サイトのコードおよびコンテンツの著作権は作成者に帰属します。
