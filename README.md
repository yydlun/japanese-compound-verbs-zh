# The Japanese Compound Verbs deck

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT.md)

## 中文说明

本仓库基于 [moltinginstar/japanese-compound-verbs](https://github.com/moltinginstar/japanese-compound-verbs)（作者 moltinginstar）。在此基础上，`data/deck.csv` 新增了 `meaning_zh` 列，为全部 2,759 个复合动词提供了简体中文释义：每个义项与每条例句均有中译，HTML 结构与英文列 `meaning_en` 保持一致（英文含糊处对照日文列校订）。构建代码也已同步接入该列：`Record` 类型新增 `meaning_zh` 字段，Anki note model 新增 “Meaning (Chinese)” 字段并显示在卡片背面。本仓库遵循原项目的 GPL-3.0 许可证（见 LICENSE 文件）。

This repo contains the data and code to build the [Japanese Compound Verbs](https://ankiweb.net/shared/info/921752699) deck, a comprehensive list of over 2700 compound verbs in Japanese, complete with parallel definitions, usage notes, and example sentences in Japanese, English, and Korean.

## Contributing

If you find any mistakes that may have slipped through, or if you have any suggestions for improvements (such as new note types), you’re more than welcome to create an issue or—better yet—a pull request. If you choose to contribute, these will come in handy:

- <https://docs.ankiweb.net/getting-started.html>
- <https://github.com/kerrickstaley/genanki>

## Repository structure

```text
.
├── build/
│   └── [Japanese Compound Verbs.apkg] the final packaged deck
├── data/
│   └── data.csv                       the contents of the deck
└── japanese_compound_verbs/
    ├── datatypes/
    │   └── data_record.py             type hints for data.csv
    ├── notetypes/
    │   └── <notetype>/
    │       ├── cards/
    │       │   └── <template>.py      front and back templates for a card style
    │       ├── definition.py          notetype ID, name, and fields 
    │       └── utils.py               functions for creating a note, etc.
    └── main.py                        script for building the deck
```

## License

The contents of this repository (including the data) are licensed under the [GNU GPL v3](https://choosealicense.com/licenses/gpl-3.0/) license.

## Credit

National Institute for Japanese Language and Linguistics. (2015) *The Compound Verb Lexicon* [Original Data]. (<https://vvlexicon.ninjal.ac.jp/>)
