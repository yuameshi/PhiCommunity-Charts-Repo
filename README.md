# 这里是哪里

这里是[PhiCommunity](https://github.com/HanHan233/PhiCommunity)的谱面仓库，用于储存谱面文件

点击[此处](https://github.com/HanHan233/PhiCommunity-Charts-Repo)前往PCCR的GitHub仓库

# 提交谱面

在一切的之前，您需要PhiEdit或Re:PhiEdit创建的PEC格式谱面或者官方的JSON格式谱面，没有就别说了（请注意，我们不提供PhiEdit和Re:PhiEdit的副本）

请注意：对于Re:PhiEdit导出的PEC谱面可能需要做一些特殊的修正，请参考[这份文档](https://ilovecpp-my.sharepoint.com/:b:/g/personal/admin_han-han_xyz/EU6w76wDBIxMr0hhdeYP650BVg-UzIrQG3VhYiiTUmPCtA?e=y0CBjB)，在按此说明导出合适的PEC谱面后，前往lchzh3473的模拟器测试是否能正常播放，再进行提交。

并且在提交前确保您已经获得曲师、谱师和曲绘画师的授权。

首先`Fork`这个仓库到你的账号，这一步需要一个GitHub账号。如果您没有，只需注册一个，然后 Fork。

首先创建一个具有正确名称的新文件夹，例如 `rrhar` 或 `rrharil` 指的是 `Rrhar'il`。（不要包含特殊字符，如 `' / \ ` 等，不能以`.`开头）

在其中创建或粘贴以下文件
```
meta.json          必须-元数据     (名称不可变更)
base.mp3           必选-音乐       (名称可变更)
chart.json         必须-铺面       (名称可变更)
line.json          可选-判定线贴图  (名称可变更)
illustration.jpg   必须-曲绘       (名称可变更)
```
> 音乐要求：MP3/OGG/WAV等常见格式(能正常兼容各个浏览器的AudioContext即可)，大小小于5MB(建议调整采样率为44100kHz，调整比特率108~128Kbps，声道双通道)

> 曲绘要求：JPG/PNG等常见格式(WebP没测试过)，大小小于0.5MB

在`meta.json`内填入歌曲元信息（见下），注意要删除注释，使用英文字符，且双引号需要添加`\`转译。
```javascript
{
	"name":"Rrhar'il",                             //曲名
	"codename":"rrharil",                          //代号(你的文件夹名称)
	"artist": "Team Grimoire",                     //曲师
	"musicFile":"music.ogg",                       //音乐文件名
	"ezRanking":7,                                 //EZ定数（若没有值可不填）
	"hdRanking":12,                                //HD定数（若没有值可不填）
	"inRanking":15,                                //IN定数（若没有值可不填）
	"atRanking":16,                                //AT定数（若没有值可不填）
	"lineTexture":"line.json",                     //可选-判定线贴图文件名
	"chartEZ":"Chart_EZ.json",                     //EZ谱面（若没有值可不填）
	"chartHD":"Chart_HD.json",                     //HD谱面（若没有值可不填）
	"chartIN":"Chart_IN.json",                     //IN谱面（若没有值可不填）
	"chartAT":"Chart_AT.json",                     //AT谱面（若没有值可不填）
	"illustration":"illustration.jpg",             //曲绘文件名
	"chartDesigner":"RDRT -p 19:08:31",            //谱师(当此属性存在时将忽略所有其他谱师设定)
	"ezChartDesigner":"RDRT -p 19:08:31",          //EZ谱师
	"hdChartDesigner":"RDRT -p 20:02:21",          //HD谱师
	"inChartDesigner":"RDRT -p 20:08:31",          //IN谱师
	"atChartDesigner":"RWND -p 16493:62786:92551", //AT谱师
	"illustrator":"犀牛沱动画工坊",                 //曲绘画师
	"sliceAudioStart":"84.5"                       //预览音频切片开始时间（秒），预览音频持续时间为15秒
}
```

完成后，将谱面文件夹（您之前创建的）上传到 *你的Git仓库*（您之前复刻的那个），然后打开一个新的 `Pull Request` 然后等待合并。

如果您觉得此操作实在无法理解，您可以提出[Issue](https://github.com/HanHan233/PhiCommunity-Charts-Repo/issues)，让我代为添加。

# 请最好一次Commit搞定(真的不想Git仓库体积爆炸)

# 搞错了什么的话就删掉仓库重新Fork一个
