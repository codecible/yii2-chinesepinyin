# yii2-chinesepinyin
yii2版, 可以把汉子转为拼音

# 安装方法

1.命令安装
``` php
php composer.phar require diszz/yii2-chinesepinyin
或
composer require diszz/yii2-chinesepinyin
```


# 代码中使用

``` php
$Pinyin = new ChinesePinyin();
$str = '带声调的汉语拼音';
$ret = $Pinyin->TransformWithTone($str);
var_dump($ret);

echo '<br/>';
$str = '无声调的汉语拼音,凡芃团队';
$ret = $Pinyin->TransformWithoutTone($str);
var_dump($ret);

echo '<br/>';
$str = '首字母只包括汉字BuHanPinYin';
$ret = $Pinyin->TransformUcwordsOnlyChar($str);
var_dump($ret);

echo '<br/>';
$str = '首字母和其他字符如B区32号';
$ret = $Pinyin->TransformUcwords($str);
var_dump($ret);


string(40) "dài shēng diào de hàn yǔ pīn yīn "
string(38) "wushengdiaodehanyupinyinfanpengtuandui"
string(8) "SZMZBKHZ"
string(14) "szmhqtzfrBq32h" 

```


