autokana
========

Library for automatically rendering Furigana for inputed Japanese Text.

日本語入力に対するフリガナを自動的に別フィールドに記入するJQueryプラグイン。

Requires
-------------------------------------------------

* Jquery

Description
-------------------------------------------------

Attaches a keydown listener to the first defined element, and transfers the inputted kana characters to the second element.
This allows Japanese users to automatically input the furigana for their name without needing to input data twice. Because the furigana box is filled out in real time, corrections can be made by the user afterwards.

Based on Rubricks' autoRuby.js prototype project: http://d.hatena.ne.jp/rubricks/20080702/1215003705

第一変数のJqueryセレクターにキーダウンリスナーをバインドして、入力された文字をフリガナとして第２変数のJqueryセレクターに自動的に入力する。

RubricksのautoRuby.jsをベースにしました。Prototype版が必要でありましたら、そちらへご参考：
http://d.hatena.ne.jp/rubricks/20080702/1215003705


Usage
-------------------------------------------------

* Pass the NAME element and the FURIGANA input elements to the Plugin
* $.fn.autoKana('#UserName', '#UserFurigana');
* Optionally, pass the katakana:true option to automatically convert the furigana to full-width katakana
* $.fn.autoKana('#UserName', '#UserFurigana', {katakana:true});

* 名前とフリガナのフィールドエレメントをプラグインに定義：
* $.fn.autoKana('#UserName', '#UserFurigana');
* katakana:trueのオプションを定義する場合、フリガナがカタカナに変換されませす。
* $.fn.autoKana('#UserName', '#UserFurigana', {katakana:true});

Issues
-------------------------------------------------

* Kana will be removed from the furigana field if deleted from the original input field, but kanji that are deleted from the input field will not be reflected in the furigana field
* For obvious reasons, getting the Furigana of copy/pasted text is not supported
* English characters are not currently supported

* 第一フィールドから削除されたカナがフリガナのフィールドにも反映しますが、削除された漢字が反映されない。なので、hiddenフィールドを避けることがお勧め
* keydownを利用しているので、コピペされたテキストは非対応
* ローマ字は非対応

Example Site
-------------------------------------------------

Made for Kurokabe Square's online reservation system:
http://kurokabe.jp/

長浜黒壁スクエアのクラス吹き体験教室システム
http://kurokabe.jp/