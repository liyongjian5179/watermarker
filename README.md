# marker.py

为图片添加文字水印
可设置文字**大小、颜色、旋转、间隔、透明度**

# usage

需要PIL库 `pip install pillow==6.2.0  -i https://mirrors.aliyun.com/pypi/simple/`

```
usage: marker.py [-h] [-f FILE] [-m MARK] [-o OUT] [-c COLOR] [-s SPACE]
                 [-a ANGEL] [--size SIZE] [--opacity OPACITY]

optional arguments:
  -h, --help            show this help message and exit
  -f FILE, --file FILE  image file path or directory
  -m MARK, --mark MARK  watermark content
  -o OUT, --out OUT     image output directory, default is ./output
  -c COLOR, --color COLOR
                        text color like '#000000', default is #8B8B1B
  -s SPACE, --space SPACE
                        space between watermarks, default is 75
  -a ANGEL, --angel ANGEL
                        rotate angel of watermarks, default is 30
  --size SIZE           font size of text, default is 50
  --opacity OPACITY     opacity of watermarks, default is 0.15
```
# 参考命令
```bash
python marker.py -f ./input -m 仅限XXX平台注册使用 -c "#232862" --opacity 0.3 --size 30
```

# 命令参数
```
-f 参数，指定打水印的文件，如果你想打印整个文件夹，则输入该文件夹路径即可。
-m 参数，指定水印内容。
-o 参数，指定输出水印文件的位置，默认为output文件夹。
-c 参数，指定水印的颜色，默认值为shi..啊不，黄色，#8B8B1B.
-s 参数，指定水印与水印之间的空隙，默认值为75.
-a 参数，指定水印的旋转角度，我们的例子中都是默认值30度。
--size参数，指定水印文本字体大小，默认值为50。
--opacity参数，指定透明度，默认为0.15，数值越小越透明。
```

# 原图
![身份证正面](https://github.com/liyongjian5179/watermarker/raw/master/input/idcard.png)
![身份证背面](https://github.com/liyongjian5179/watermarker/raw/master/input/idcard_back.png)
# 打码后
![身份证正面](https://github.com/liyongjian5179/watermarker/raw/master/output/idcard.png)
![身份证背面](https://github.com/liyongjian5179/watermarker/raw/master/output/idcard_back.png)

