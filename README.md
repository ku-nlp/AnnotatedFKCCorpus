# Annotated FKC Corpus

## Overview

This is a Japanese text corpus that consists of Fuman (complaints) documents with various linguistic annotations. FKC stands for Fuman Kaitori Center, which is a Japanese consumer opinion data collection and analysis service. This corpus contains complaint documents with various genres, such as consumer electronics, hospital, information technology (IT), supermarket, trip, and traffic. It comprises 654 documents, which correspond to 1,282 sentences.

The linguistic annotations consist of annotations of morphology, named entities, dependencies, predicate-argument structures including zero anaphora, and coreferences. All the annotations were given by manually modifying automatic analyses of the morphological analyzer Juman++ and the dependency, case structure and anaphora analyzer.

## Notes on annotation guidelines

The annotation guidelines for this corpus are written in the manuals found in the "doc" directory. The guidelines for morphology and dependencies are described in syn_guideline.pdf, those for predicate-argument structures and coreferences are described in rel_guideline.pdf. The guidelines for named entities are available at the IREX web site (<http://nlp.cs.nyu.edu/irex/>).

## Distributed files

* knp/ : the corpus annotated with morphology, named entities, dependencies, predicate-argument structures, and coreferences
* org/ : the raw corpus
* doc/ : annotation guidelines
* id/ : document id files providing train/test split

## Format of the corpus annotated with annotations of morphology, named entities, dependencies, predicate-argument structures, and coreferences

Annotations of this corpus are given in the following format.

```text
# S-ID:fuman-trip-0000000001-1
* 2D
+ 3D
太郎 たろう 太郎 名詞 6 人名 5 * 0 * 0
は は は 助詞 9 副助詞 2 * 0 * 0
* 2D
+ 2D
京都 きょうと 京都 名詞 6 地名 4 * 0 * 0
+ 3D <NE:ORGANIZATION:京都大学>
大学 だいがく 大学 名詞 6 普通名詞 1 * 0 * 0
に に に 助詞 9 格助詞 1 * 0 * 0
* -1D
+ -1D <rel type="ガ" target="太郎" sid="fuman-trip-0000000001-1" id="0"/><rel type="ニ" target="大学" sid="fuman-trip-0000000001-1" id="2"/>
行った いった 行く 動詞 2 * 0 子音動詞カ行促音便形 3 タ形 10
EOS
```

A description of this format can be found in [the documentation of KWDLC](https://github.com/ku-nlp/KWDLC#format-of-the-corpus-annotated-with-annotations-of-morphology-named-entities-dependencies-predicate-argument-structures-and-coreferences).

## References

* 萩行正嗣, 河原大輔, 黒橋禎夫. 多様な文書の書き始めに対する意味関係タグ付きコーパスの構築とその分析, 自然言語処理, Vol.21, No.2, pp.213-248, 2014.
<https://doi.org/10.5715/jnlp.21.213>

## Acknowledgment

The creation of this corpus was supported by Insight Tech Inc. We deeply appreciate their support.

## Contact

If you have any questions or problems about this corpus, please send an email to nl-resource at nlp.ist.i.kyoto-u.ac.jp.

## Copyright

The copyright of the complaint documents belongs to Insight Tech Inc.
The copyright of the annotation information belongs to Kurohashi Lab, Kyoto University.

## License

The license for this corpus is subject to CC BY-NC-SA 4.0.
<https://creativecommons.org/licenses/by-nc-sa/4.0/>
The purpose of using this corpus is limited to academic research.
