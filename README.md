# cppHusky 的 Rime 自用方案

該方案由 *cppHusky* 基於 [Rime](https://github.com/rime/home) 輸入引擎製作而成。支持以下輸入法：

+ **全拼（基于 朙月拼音·简化字）**
+ **五笔86（基于 [networm的86五笔单字方案](https://github.com/networm/Rime)）**
+ **大千注音（基於 注音·臺灣正體）**
+ **倉頡五代（基於 [Jackchows的倉頡五代補完計劃](https://github.com/Jackchows/Cangjie5)）**

下面陳述各輸入法之特性，以供參閱。

## 全局設定（可以有例外）

全角模式的標點配置相對詳細；半角模式的標點配置比較簡潔。參見默認配置文件 [default.custom.yaml](https://github.com/cppHusky/Rime/blob/main/default.custom.yaml) 。

只能用 `Ctrl`+`` ` `` 喚起方案選單。可以用 `shift` 快捷鍵切換中英文輸入。

翻下頁可以用 `]`；翻上頁可以用 `[`。

所有輸入法均默認使用英文模式。

（另：這些方案無一例外，均不允許混合輸入。如，Rime原本的倉頡輸入法允許混輸拼音，本方案已將該功能取消）

## 全拼（基于 朙月拼音·简化字）

每页5个候选项。

包含 [Rime扩充词库](https://github.com/rime-aca/dictionaries)。

支持词组输入和动态调整词频。

敲击 `` ` `` 可以通过笔画反查拼音，笔画的规则是：`h` 横 `s` 竖 `p` 撇 `n` 捺 `z` 折。

## 五笔86（基于 networm的86五笔单字方案）

每页3个候选项。（就本人的使用经验来说，几乎没有三个以上的同码字；即便有，那也是很生僻的字）

该输入法的词库只含单字。（三万余汉字，含简体字和繁体字，简体字优先）

不支持词组输入和动态调整词频。（这样能做到最好的“盲打”效果）

四码唯一自动上屏；敲击第五码可以顶字上屏。（部分标点符号也有顶字上屏作用）

敲击 `` ` `` 可以通过全拼反查五笔编码。

支持 [仓颉五代符号表](https://zh.wikibooks.org/zh-cn/%E5%80%89%E9%A0%A1%E8%BC%B8%E5%85%A5%E6%B3%95/%E9%80%B2%E9%9A%8E%E7%9F%A5%E8%AD%98#%E4%BA%94%E4%BB%A3%E5%80%89%E9%A0%A1%E7%AC%A6%E8%99%9F%E8%A1%A8) 中的部分 `yyy` 开头符号，以 `zy`
代替 `yyy` 使用。

## 大千注音 （基於 注音·臺灣正體）

每頁5個候選項。

尚未配置額外詞庫。

支持詞組輸入和動態調整詞頻。

有獨特的標點符號配置方案，詳見 [bopomofo_tw.custom.yaml](https://github.com/cppHusky/Rime/blob/main/bopomofo_tw.custom.yaml)。

敲擊 `` ` `` 可以通過筆畫反查注音，筆畫的規則是：`h` 橫 `s` 豎 `p` 撇 `n` 捺 `z` 折。

## 倉頡五代 （基於 Jackchows的倉頡五代補完計劃）

每頁3個候選項。

該輸入法的詞庫只含單字。（至少九萬餘漢字，含繁體字和簡化字，繁體字通常優先）

不支持詞組輸入和動態調整詞頻。（這樣能做到最好的「盲打」效果）

五碼唯一自動上屏；敲擊第六碼可以頂字上屏。（部分標點符號也有頂字上屏作用）

敲擊 `` ` `` 可以通過全拼反查倉頡碼。

支授 [五代倉頡符號表](https://zh.wikibooks.org/zh-tw/%E5%80%89%E9%A0%A1%E8%BC%B8%E5%85%A5%E6%B3%95/%E9%80%B2%E9%9A%8E%E7%9F%A5%E8%AD%98#%E4%BA%94%E4%BB%A3%E5%80%89%E9%A0%A1%E7%AC%A6%E8%99%9F%E8%A1%A8)。

碼表中刪去 `重` 碼，改為 `片` 碼。

+ 敲繫 `片戈*` 可以輸入 [表意文字描述字元](https://zh.wikipedia.org/wiki/%E8%A1%A8%E6%84%8F%E6%96%87%E5%AD%97%E6%8F%8F%E8%BF%B0%E5%AD%97%E7%AC%A6)，如 `片戈田一中` 得 `⿸`；
+ 敲繫 `片弓*` 可以輸入計數符號（即畫「正」字），如 `片弓一卜` 得 `𝍴`；
+ 敲繫 `片口*` 可以輸入部首字元，如 `片口弓中` 得 `⻏` 與 `⻖`。
+ 敲繫 `片尸*` 可以輸入筆畫字元，如 `片尸女中` 得 `㇟`。
