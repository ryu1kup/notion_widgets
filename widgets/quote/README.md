# Quote Widget

毎日ひとつの名言を表示する Notion 埋め込み用ウィジェット。  
日付ベースで名言が決まり、毎日自動的に切り替わります。ダブルクリックで次の名言に進めます。

## URL パラメータ

| パラメータ | 説明 | デフォルト |
|-----------|------|-----------|
| `color`    | 文字色。HEX（`#` 不要）または CSS カラー名 | `#000000`（ダークモード時 `#eeeeee`）|
| `bg`       | 背景色。同上 | `transparent` |
| `font`     | フォントファミリー（CSS の `font-family` に渡す値）| `Georgia, 'Times New Roman', serif` |
| `fontsize` | 名言のフォントサイズ（CSS 値）。偉人名はその 75% に連動 | `clamp(0.95rem, 3vw, 1.4rem)` |
| `lang`     | 言語。`jp` を指定すると日本語訳で表示 | 英語 |

## URL の例

```
# シンプル（デフォルト）
https://ryu1kup.github.io/notion_widgets/widgets/quote/

# 日本語
https://ryu1kup.github.io/notion_widgets/widgets/quote/?lang=jp

# 文字色・背景色を指定
https://ryu1kup.github.io/notion_widgets/widgets/quote/?color=333333&bg=fffdf7

# フォント・サイズを指定
https://ryu1kup.github.io/notion_widgets/widgets/quote/?font=Arial&fontsize=20px

# すべて組み合わせる
https://ryu1kup.github.io/notion_widgets/widgets/quote/?lang=jp&color=222222&bg=fafafa&font=Hiragino+Sans&fontsize=1.2rem
```

## Notion への埋め込み方

1. `/embed` ブロックを挿入
2. ウィジェットの URL をパラメータ付きで貼り付ける

## 動作仕様

- **日次切り替え**: UTC 0:00（JST 9:00）に翌日の名言へ切り替わります
- **ダブルクリック**: 次の名言に手動で進めます
- **ダークモード**: `color` 未指定時、OS のダークモード設定に自動追従します
