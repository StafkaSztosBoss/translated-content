---
title: Hash function (ハッシュ関数)
slug: Glossary/Hash_function
l10n:
  sourceCommit: 7159a4c0a2f1e886c09268c41c103c4ac7100d63
---

{{GlossarySidebar}}

ハッシュ関数は、可変長の入力を受けて固定長の出力を生成する関数であり、「ダイジェスト」（または単に「ハッシュ」）とも呼ばれます。ハッシュ関数は素早く計算されるべきであり、入力が異なる場合は可能な限り異なる出力を生成すべきです（これは衝突耐性と呼ばれます）。

ハッシュ関数には{{glossary("cryptography", "暗号学的")}}な用途と非暗号学的な用途があります。ハッシュ関数の暗号以外の用途としては、例えばマップや辞書などの連想配列のキーを生成するというものがあります。

{{domxref("SubtleCrypto.digest()", "digest()")}} は {{domxref("SubtleCrypto")}} インターフェイスの関数で、ウェブアプリケーションで利用可能な様々なハッシュを作成します。

## 暗号学的ハッシュ関数

暗号学的なハッシュ関数は、{{Glossary("digital signature", "デジタル署名")}}や{{Glossary("HMAC", "メッセージ認証コード")}}などの用途があります。

すべてのハッシュ関数が暗号に適しているわけではありません。暗号に使用するためには、ハッシュ関数は以下の性質を持っていなければなりません。

- 計算が速い
- 一方向性: 出力が与えられれば、元の入力を再生することは現実的でないか、不可能であるはずである
- 改竄耐性：入力を変更すると出力が変わる
- 衝突耐性: 同じ出力を生み出す 2 つの異なる入力を見つけることは現実的ではないはずだ

暗号学的に使用される最も一般的なハッシュ関数は _SHA-2_ (Secure Hash Algorithm 2) ファミリーであり、その名前は `"SHA-"` に続いて出力するダイジェストのビット数を示します。例えば `"SHA-256"` や `"SHA-512"` です。

SHA-2 は、もはや安全とはみなされないため、暗号化には使うべきではない SHA-1 アルゴリズムの後継です。なお、 MD5 アルゴリズムも安全でないと考えられています。

## 関連情報

- {{domxref("SubtleCrypto.digest()")}}
- [ハッシュ関数](https://ja.wikipedia.org/wiki/ハッシュ関数)（ウィキペディア）
- [暗号学的ハッシュ関数](https://ja.wikipedia.org/wiki/暗号学的ハッシュ関数)（ウィキペディア）
- 関連用語:
  - {{Glossary("Symmetric-key cryptography", "共通鍵暗号")}}
