# NOTICE — Kanseki Repository 底本に関する表示

本リポジトリのテキストデータは、Kanseki Repository（漢籍リポジトリ、Kanripo）が公開するデータを底本とする再加工物である。CC BY-SA 4.0の条件（帰属表示・改変明示・同一ライセンス継承）に基づき、以下の通り出典と加工内容を表示する。

## 1. 底本の出典と版本情報

| 項目 | 内容 |
|---|---|
| 底本 | Kanseki Repository（1文献1リポジトリ構成） |
| 配布元 | https://github.com/kanripo |
| 採用ブランチ | master（全件。ブランチ名と取得時コミットSHAは catalog.csv の witness・commit 列に記録） |
| 分類・書誌の典拠 | kanripo/KR-Catalog（コミット 781711923e2ce6f82f6dacfb8576cd80774b7ec0）の KR/KR3a.txt〜KR3l.txt |
| 取得日 | 2026-10-07 |
| 収録範囲 | KR3子部（儒家類・兵家類・法家類・農家類・醫家類・天文算法類・術數類・藝術類・譜錄類・雜家類・類書類・小說家類）の目録888件のうち、リポジトリのある867件 |

masterブランチの底本は、各本文ファイル冒頭のプロパティ（BASEEDITION）によれば、四庫全書文淵閣本（WYG）794件、四部叢刊（SBCK）71件、TZH 1件、CHANT 1件である（catalog.csv の baseedition 列参照）。KR-Catalog の版本欄が WYG であっても master の底本が SBCK である文献が57件あり、catalog.csv の review_flag 列に記した。上流のリポジトリの既定ブランチが master 以外になっている3件（KR3j0192・KR3k0032・KR3k0043）も、master ブランチを採った。

底本表示が CHANT または TZH の2件は次の通りである。ほかの865件（底本表示が WYG・SBCK のもの。無標点の本文）とは性質が異なる。

| ID | 題名（目録） | 底本表示 | 内容 |
|---|---|---|---|
| KR3j0192 | 新論 | CHANT | 現代の標点と見出しを含む本文（目録の版本欄は tls）。本文ファイルの SOURCE 欄に「全上古三代秦漢三國六朝文 93-95」とある |
| KR3f0057 | 佛國暦象編 | TZH | 無標点の本文。底本は上流の Readme の表示による（「円通著佛國暦象編 底本:(德風本)東叡大王府藏版」とある） |

この2件のリポジトリ（master ブランチのファイル、およびGitHub上のリポジトリのページ）には、個別のライセンス表示・権利表示は無かった（2026-10-07確認）。

## 2. 底本のライセンス

Kanseki Repositoryは、そのコンテンツを **CC BY-SA 4.0**（Creative Commons 表示–継承 4.0 国際）で公開している。典拠は以下の通り（2026-10-07確認）。

- GitHub組織プロフィール（https://github.com/kanripo ）:「Comprehensive collection of premodern Chinese texts. Licensed as CC BY SA 4.0.」

なお、収録テキストの原典（諸子・医書・類書・筆記など）は著作権保護期間を満了した公有文献であり、CC BY-SA 4.0が及ぶのはKanripoによる翻刻・校正・構造化等の作成部分である。

## 3. 本リポジトリでの加工内容

- mandoku形式のメタデータ行（行頭が「#」の行）・画像リンクの除去（プレーンテキスト化）
- 頁マーカー `<pb:...>` の【　】形式への変換・保持
- 原本行末記号「¶」の除去と物理行の連結
- 巻ファイルの作品単位への統合、書誌情報の catalog.csv への集約
- 本文の文字そのものには改変を加えていない（異体字・外字参照・上流に残る記法もそのまま）

## 4. 本リポジトリのライセンス

底本の条件を継承し、CC BY-SA 4.0 で公開する。ライセンス全文は同梱の `LICENSE` を参照。

- ライセンス正文: https://creativecommons.org/licenses/by-sa/4.0/legalcode
- Kanseki Repository: https://github.com/kanripo
