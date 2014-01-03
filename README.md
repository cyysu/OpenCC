# Open Chinese Convert 開放中文轉換

## Introduction 介紹

Open Chinese Convert (OpenCC, 開放中文轉換) is an opensource project for conversion between Traditional Chinese and Simplified Chinese, supporting character-level conversion, phrase-level conversion, variant conversion and regional idioms among Mainland China, Taiwan and Hong kong.

中文簡繁轉換開源項目，支持詞彙級別的轉換、異體字轉換和地區習慣用詞轉換（中國大陸、臺灣、香港）。

### Features 特點

* 嚴格區分「一簡對多繁」和「一簡對多異」。
* 完全兼容異體字，可以實現動態替換。
* 嚴格審校一簡對多繁詞條，原則爲「能分則不合」。
* 支持中國大陸、臺灣、香港異體字和地區習慣用詞轉換，如「裏」「裡」、「鼠標」「滑鼠」。
* 詞庫和函數庫完全分離，可以自由修改、導入、擴展。
* 支持C、C++、Python、PHP、Java、Ruby、Node.js。
* 兼容Windows、Linux、Mac平臺。

### Links 相關鏈接

* Introduction 詳細介紹 https://code.google.com/p/opencc/wiki/Introduction
* Development Documentation 開發文檔 http://byvoid.github.io/OpenCC/
* OpenCC Online (在線轉換) http://opencc.byvoid.com/
* 現代漢語常用簡繁一對多字義辨析表 http://ytenx.org/byohlyuk/KienxPyan

## Installation 安裝

* [Debian](http://packages.qa.debian.org/o/opencc.html)
* [Ubuntu](https://launchpad.net/ubuntu/+source/opencc)
* [Fedora](https://admin.fedoraproject.org/pkgdb/acls/name/opencc)
* [Arch Linux](https://www.archlinux.org/packages/community/x86_64/opencc/)
* [Mac OS](https://github.com/mxcl/homebrew/blob/master/Library/Formula/opencc.rb)
* [Node.js](https://npmjs.org/package/opencc)

## Usage 使用

### Command Line 命令行

`opencc --help`

### Configurations 配置文件

#### 預設配置文件

* `s2t.json` Simplified Chinese to Traditional Chinese 簡體到繁體
* `t2s.json` Traditional Chinese to Simplified Chinese 繁體到簡體
* `s2tw.json` Simplified Chinese to Traditional Chinese (Taiwan Standard) 簡體到繁體（臺灣正體標準）
* `tw2s.json` Traditional Chinese (Taiwan Standard) to Simplified Chinese 繁體（臺灣正體標準）到簡體
* `s2twp.json` Simplified Chinese to Traditional Chinese (Taiwan Standard) with Taiwanese idiom 簡體到繁體（臺灣正體標準）並轉換爲臺灣常用詞彙
* `tw2sp.json` Traditional Chinese (Taiwan Standard) to Simplified Chinese with Mainland Chinese idiom 繁體（臺灣正體標準）到簡體並轉換爲中國大陸常用詞彙

## Build 編譯

[![Build Status](https://travis-ci.org/BYVoid/OpenCC.png?branch=master)](https://travis-ci.org/BYVoid/OpenCC)

### Build with CMake

```
mkdir build
cd build
cmake -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release -D ENABLE_GETTEXT:BOOL=ON ..
make
sudo make install
```

Windows MSYS:

```
cmake .. -G "MSYS Makefiles" -DCMAKE_INSTALL_PREFIX="" -DCMAKE_BUILD_TYPE=Release -DENABLE_GETTEXT:BOOL=OFF
make
```

Windows Visual Studio (2013 or higher required):

```
cmake .. -G "Visual Studio 12" -DCMAKE_INSTALL_PREFIX="" -DCMAKE_BUILD_TYPE=Release -DENABLE_GETTEXT:BOOL=OFF
make
```

## Screenshot 截圖

![OpenCC Mac](http://opencc.googlecode.com/files/screenshot-gui-mac.png)

![OpenCC Windows](http://opencc.googlecode.com/files/screenshot-gui.png)

![OpenCC Ubuntu](http://opencc.googlecode.com/files/screenshot-gui-ubuntu.png)

### Projects using Opencc 使用OpenCC的項目

* [ibus-pinyin](http://code.google.com/p/ibus/)
* [fcitx](http://code.google.com/p/fcitx/)
* [rimeime](http://code.google.com/p/rimeime/)
* [libgooglepinyin](http://code.google.com/p/libgooglepinyin/)
* [ibus-libpinyin](https://github.com/libpinyin/ibus-libpinyin)
* [BYVBlog](https://github.com/byvoid/byvblog)
* [豆瓣同城微信](http://weixinqiao.com/douban-event/)

## Contributors 貢獻者

* [BYVoid](http://www.byvoid.com/)
* [佛振](https://github.com/lotem)
* [Peng Huang](https://github.com/phuang)
* [LI Daobing](https://github.com/lidaobing)
