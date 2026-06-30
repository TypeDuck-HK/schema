# TypeDuck Schema / TypeDuck 方案

呢個 repo 係 TypeDuck 各平台共用嘅 RIME 方案同辭典資料，支援 [Windows](https://github.com/TypeDuck-HK/TypeDuck-Windows)、[Mac](https://github.com/TypeDuck-HK/TypeDuck-Mac)、[Android](https://github.com/TypeDuck-HK/TypeDuck-Android)、[iOS](https://github.com/TypeDuck-HK/TypeDuck-iOS) 同 [Web](https://github.com/TypeDuck-HK/TypeDuck-Web)。

This repo is the shared RIME schema and dictionary data behind TypeDuck on [Windows](https://github.com/TypeDuck-HK/TypeDuck-Windows), [Mac](https://github.com/TypeDuck-HK/TypeDuck-Mac), [Android](https://github.com/TypeDuck-HK/TypeDuck-Android), [iOS](https://github.com/TypeDuck-HK/TypeDuck-iOS), and [Web](https://github.com/TypeDuck-HK/TypeDuck-Web).

`jyut6ping3.dict.yaml` 同 `essay.txt` 存放候選詞同詞頻；[TypeDuck librime](https://github.com/TypeDuck-HK/librime) 會用佢哋建立輸入候選。

`jyut6ping3.dict.yaml` and `essay.txt` provide entries and frequencies used by [TypeDuck librime](https://github.com/TypeDuck-HK/librime) to build candidate lists.

主要 TypeDuck 辭典係 `jyut6ping3_scolar.dict.yaml`；[rime-dictionary-lookup-filter](https://github.com/TypeDuck-HK/rime-dictionary-lookup-filter) 會查呢個檔案，加入翻譯等更豐富嘅辭典資料。

The main TypeDuck dictionary is `jyut6ping3_scolar.dict.yaml`; [rime-dictionary-lookup-filter](https://github.com/TypeDuck-HK/rime-dictionary-lookup-filter) reads it to enrich candidates with extra dictionary data such as multilingual translations.

`jyut6ping3_mobile*` 同 `loengfan_longpress` 係流動裝置專用方案，桌面版同網頁版唔會包含。

`jyut6ping3_mobile*` and `loengfan_longpress` are mobile-only schemas and are not included in desktop or web builds.

## Reverse Lookup / 反查

唔識讀或者唔肯定粵拼時，可以用反查：輸入反引號開頭嘅碼，再用其他輸入法搵字學字。

Reverse lookup lets you find and learn a character or word through another input method when you do not know its Cantonese pronunciation or Jyutping spelling.

要開始反查，請輸入：

To call up reverse lookup, type:

| Prefix / 前綴 | Input Method / 輸入法 |
| --- | --- |
| `` `p `` | Mandarin Pinyin / 普通話拼音 |
| `` `l `` | Loengfan / 粵語兩分 |
| `` `b `` | Stroke / 筆畫 |
| `` `c `` | Cangjie / 倉頡 |
| `` `q `` | Quick / 速成 |

反查方案只係臨時輔助工具，唔屬於 TypeDuck 主詞庫。多謝以下項目提供反查資料；佢哋保留各自嘅授權。

The reverse lookup schemas are provisional helpers, not part of the TypeDuck lexicon. Thanks to the projects below for the lookup data; each keeps its own license.

| Files / 檔案 | Source / 來源 | License / 授權 |
| --- | --- | --- |
| `luna_pinyin.dict.yaml` | [rime/rime-luna-pinyin](https://github.com/rime/rime-luna-pinyin) | LGPL-3.0 |
| `loengfan.dict.yaml` | [CanCLID/rime-loengfan](https://github.com/CanCLID/rime-loengfan) | CC BY 4.0 |
| `stroke.dict.yaml` | [rime/rime-stroke](https://github.com/rime/rime-stroke) | LGPL-3.0 |
| `cangjie3.dict.yaml`[^cangjie3] | [Arthurmcarthur/Cangjie3-Plus](https://github.com/Arthurmcarthur/Cangjie3-Plus) | MIT |
| `cangjie5.dict.yaml`[^cangjie5] | [Jackchows/Cangjie5](https://github.com/Jackchows/Cangjie5) | MIT |

[^cangjie3]: Also referenced by `quick3.dict.yaml` / `quick3.dict.yaml` 亦參照此方案
[^cangjie5]: Also referenced by `quick5.dict.yaml` / `quick5.dict.yaml` 亦參照此方案

## License / 授權

除咗上面列明嘅反查資料之外，本 repo 採用 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)，涵蓋 TypeDuck 主辭典同 `jyut6ping3` 方案。

Except for the reverse lookup data listed above, this repo, including the main TypeDuck dictionary and the `jyut6ping3` schema, is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
