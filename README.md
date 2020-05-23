# Coreference_annotated_corpus
Coreference-annotated Corpus of ACL Anthology papers in CoNLL format
(coreference between head noun phrases)

This corpus is based on the data from (Schäfer et al. 2012):
Ulrich Schäfer; Christian Spurk; Jörg Steffen
"A Fully Coreference-annotated Corpus of Scholarly Papers from the ACL Anthology," Proceedings of COLING 2012, pp.1059-1070, 2012.

To convert the original corpus to a CoNLL formatted corpus, we modified the corpus as follows:

* Correction of sentence boundary errors (with the help of GENIA sentence splitter and section title detection by Poppler)
* POS tagging (using Stanford CoreNLP)
* parse tree annotation (using Stanford CoreNLP)
* NE annotation (using Stanford CoreNLP)

Many NLP tools (POS tagger, syntactic parser, etc.) are based on general domain and tend to produce more errors in scientific texts.
Therefore, it is difficult to correctly identify noun phrases (candidate mentions) and it makes learning coreference system harder.  To resolve this problem, we changed the annotated mention spans from maximal projection of noun phrases to minimal projection which contains the head noun (Head NP).

If you use this data, please cite (Schäfer et al. 2012).

- original_auto_conlls: The original corpus contains inconsistet annotation in citations, either the parentheses arround a citation are included in the mention or not.
- citation_reformatted: Modified all citation mentions so that parentheses are not included.
- head_auto_conll: Modified all mentions into the head NPs.

To find the detailed description of the conversion, please refer to the following article: 

Aya Iwamoto, Hiroshi Noji, Hiroyuki Shindo, and Yuji Matsumoto,
"<a href="https://github.com/YujiMatsu/Coreference_annotated_corpus/blob/master/SCIDOCA2016_iwamoto.pdf">Toward Coreference Resolution in Scientific Domain</a>,"
 In Proceedings of First International Workshop on ScIentific Document Analysis (SCIDOCA 2016), Keio University, Kanagawa, Japan, November 15, 2016.

---------- in Japanese ----------
このコーパスは(Schäfer et al. 2012)らのデータに基づいています：
Ulrich Schäfer; Christian Spurk; Jörg Steffen
"A Fully Coreference-annotated Corpus of Scholarly Papers from the ACL Anthology,"
Proceedings of COLING 2012, pp.1059-1070, 2012.

オリジナルのフォーマットからCoNLLフォーマットへ変換するために，以下のように修正を行いました
* 文分割の誤りの修正（Genia Sentence splitter + Popplerで抽出されたセクションタイトル）
* 品詞タグ付け（Stanford CoreNLP）
* 句構造木（同上）
* NER（同上）

多くのNLPツール（品詞解析, 句構造解析器など）は一般の分野に基づいていて，科学技術分野ではより誤りが多くなる傾向があります．
その為，正しく名詞句（候補となる言及）の範囲を同定することが難しく，これによって共参照解析器の学習がより難しくなっています．
この問題を解決するため，アノテーションされたメンションの範囲を名詞句の最大範囲からHeadとなる名詞を含む最小範囲（Head NP）へ変更しました．

このデータを用いる際には，Schäferら(2012)の論文の引用をお願いします．

- original_auto_conlls: オリジナルのコーパスを変換したもの（引用に関す売るアノテーション基準が統一されていません．引用の前後に括弧を含む場合と含まない場合が混在しています．）
- citation_reformatted: 上記を括弧を含まないように統一したもの．
- head_auto_conll:head NPへアノテーションを変更したもの

変換に関する詳しい説明は，以下の論文を参照してください．

Aya Iwamoto, Hiroshi Noji, Hiroyuki Shindo, and Yuji Matsumoto,
"Toward Coreference Resolution in Scientific Domain,"
 In Proceedings of First International Workshop on ScIentific Document Analysis (SCIDOCA 2016), Keio University, Kanagawa, Japan, November 15, 2016.

岩元文, 能地宏, 進藤裕之, 松本裕治：
"科学技術文献の共参照解析コーパスの整備",
言語処理学会第２３回年次大会発表論文集, 筑波大学, pp50-53, March 14, 2017.
