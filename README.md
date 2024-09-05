[合集 \- AIGC(27\)](https://github.com)[1\.轻松复现一张AI图片04\-22](https://github.com/flydean/p/18150293)[2\.Stable Diffusion中的常用术语解析04\-23](https://github.com/flydean/p/18152608)[3\.Stable diffusion中这些重要的参数你一定要会用04\-24](https://github.com/flydean/p/18155012)[4\.Stable Diffusion中的embedding04\-25](https://github.com/flydean/p/18158261)[5\.怎么使用Stable diffusion中的models05\-28](https://github.com/flydean/p/18218116)[6\.Stable Diffusion WebUI详细使用指南05\-29](https://github.com/flydean/p/18220340)[7\.Stable diffusion采样器详解06\-04](https://github.com/flydean/p/18230619)[8\.原来Stable Diffusion是这样工作的06\-06](https://github.com/flydean/p/18235713)[9\.MoneyPrinterPlus:AI自动短视频生成工具,赚钱从来没有这么容易过06\-12](https://github.com/flydean/p/18244029)[10\.MoneyPrinterPlus:AI自动短视频生成工具,详细使用教程06\-17](https://github.com/flydean/p/18252063)[11\.MoneyPrinterPlus:AI自动短视频生成工具\-阿里云配置详解06\-20](https://github.com/flydean/p/18259059)[12\.MoneyPrinterPlus:AI自动短视频生成工具\-腾讯云配置详解06\-25](https://github.com/flydean/p/18266262)[13\.MoneyPrinterPlus:AI自动短视频生成工具\-微软云配置详解06\-26](https://github.com/flydean/p/18269224)[14\.重磅!免费一键批量混剪工具它来了,一天上万短视频不是梦06\-28](https://github.com/flydean/p/18272631):[蓝猫机场](https://fenfang.org)[15\.hypernetwork在SD中是怎么工作的07\-01](https://github.com/flydean/p/18278161)[16\.SD中的VAE,你不能不懂07\-03](https://github.com/flydean/p/18281548)[17\.福利来了！MoneyPrinterPlus可以自动配置环境和自动运行了07\-04](https://github.com/flydean/p/18283130)[18\.手把手教你生成一幅好看的AI图片07\-05](https://github.com/flydean/p/18285702)[19\.什么?这动物图片可以上国家地理?07\-09](https://github.com/flydean/p/18291672)[20\.重磅来袭!MoneyPrinterPlus一键发布短视频到视频号,抖音,快手,小红书上线了07\-10](https://github.com/flydean/p/18293523)[21\.MoneyPrinterPlus全面支持本地Ollama大模型07\-15](https://github.com/flydean/p/18303300)[22\.在MoneyPrinterPlus中使用本地chatTTS语音模型07\-16](https://github.com/flydean/p/18304553)[23\.fasterWhisper和MoneyPrinterPlus无缝集成07\-24](https://github.com/flydean/p/18320436)[24\.再升级!MoneyPrinterPlus集成GPT\_SoVITS08\-14](https://github.com/flydean/p/18358780)[25\.AI图像放大工具,图片放大无所不能09\-03](https://github.com/flydean/p/18394859)[26\.LoRA大模型微调的利器09\-04](https://github.com/flydean/p/18395814)27\.在stable diffussion中控制生成图片的光线09\-05收起
在摄影中，光线起着至关重要的作用，它对图像的整体质量和氛围有着显著的影响。您可以使用光线来增强主题，创造深度和维度，传达情感，以及突出重要细节。


在这篇文章中，我会告诉你如何在stable diffussion中控制生成图片的光线。


## 软件


我们将使用 AUTOMATIC1111 Stable Diffusion GUI 来创建图像。


## 使用光线关键词


最简单的控制光线的方法就是在提示中添加**光线关键词**。


我将使用以下基础提示和负面提示来说明效果。


正向提示词：



```
masterpiece,best quality,masterpiece,best quality,official art,extremely detailed CG unity 8k wallpaper,a beautiful woman,

```

负向提示词：



```
lowers,monochrome,grayscales,skin spots,acnes,skin blemishes,age spot,6 more fingers on one hand,deformity,bad legs,error legs,bad feet,malformed limbs,extra limbs,

```

模型：majicmixRealistic\_v7


宽度：512


高度：768


CFG 刻度：7


下面是使用基础提示词生成的图片，他们看起来还不错，但是光线就不怎么样了。


![image-20240703143858781](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031439947.png)


**Volumetric lighting**是在图像上明显的光束。它在摄影中用于增加体积感。


在提示中添加关键词**Volumetric lighting**：


![image-20240703144120928](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031441856.png)


**rim lighting**为主题添加了明亮的轮廓。它可能会使主题变暗。您可以与其他光线术语结合使用以照亮主题。


在提示中添加关键词**rim lighting**：


![image-20240703144310934](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031443765.png)


**Sunlight**为图像添加了阳光。它倾向于呈现自然背景。


在提示中添加关键词**Sunlight**。


![image-20240703144429961](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031444968.png)


**Backlight**将光源置于主题之后。通过添加这个关键词，您可以产生一些时尚的效果。


在提示中添加**Backlight**。


![image-20240703144516763](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031445610.png)


众所周知，Stable Diffusion 在没有引导的情况下不会产生黑暗的图像。


解决这个问题的方法有很多，包括使用模型和 LoRA。但更简单的方法是添加一些昏暗的光线关键词。


在提示中添加**dimly lit**。


![image-20240703144626131](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031446658.png)


**Crepuscular rays**在云层中添加了光线穿透的光线。它可以创造出令人惊叹的视觉效果。


这个提示和肖像宽高比通常呈现全身图像，添加**Crepuscular rays**会放大。


![image-20240703144742215](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031447630.png)


技巧：


* 如果您没有看到效果，请增加关键词的权重。
* 这些光线关键词并不总是有效。一次生成几张图像进行测试。
* 在提示生成器中找到更多的光线关键词。


## 控制特定区域的光线


提示中的光线关键词适用于整个图像。这里我会告诉你如何控制特定区域的光线。


这里你需要安装一个插件叫做regional Prompter。


下载地址如下： [https://github.com/hako\-mikan/sd\-webui\-regional\-prompter.git](https://github.com)


安装好之后，可以在工作区的下方发现这个Regional Prompter的区域。


在这个例子中，我们将对图像的上部和下部应用不同的光线。


在**txt2img**页面上，展开**regional Prompter**部分。


![image-20240703150427848](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031504474.png)


按我上面的选择进行设置。


基本上含义就是把图片按2：3的比例分割成两部分，来分别进行promot设置。


regional Prompter是一个非常强大的工具，可以产出非常惊艳的效果。我会在后续的文章中详细介绍regional Prompter。


这里只是作为一个使用场景。


我们改下输入提示：


正向提示词：



```
masterpiece,best quality,masterpiece,best quality,official art,extremely detailed CG unity 8k wallpaper,a beautiful woman,
BREAK
( hard light:1.2),(volumetric:1.2),well-lit,
BREAK
(dimly lit:1.4),

```

负面提示词保持不变。


这样我们的到了一个上面光亮，下面昏暗的图片。


![image-20240703150710842](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031507318.png)


现在尝试交换光线分配。



```
masterpiece,best quality,masterpiece,best quality,official art,extremely detailed CG unity 8k wallpaper,a beautiful woman,
BREAK
(dimly lit:1.4),
BREAK
( hard light:1.2),(volumetric:1.2),well-lit,

```

![image-20240703150837199](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031508876.png)


光线相应地交换。


技巧：


* 如果您没有看到效果，请调整关键词的权重。
* 区域提示并不总是100%有效。可以多尝试一些图片看看效果。


## 使用 ControlNet 控制光线


除了上面的提示词和regional Prompter来控制光线之外。我们还可以使用controlNet来对图片的光线进行更加精确的控制。


controlNet是一个单独的插件，所以你需要先安装它。


### Txt2img 设置


安装好controlNet之后，在**txt2img**页面上，像平常一样生成图像。


![image-20240703151405473](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031514542.png)


点击发送到 **img2img**。


这个操作会把所有的提示，负面提示，图像大小和种子值拷贝到 img2img 页面。


### Img2img 设置


在**img2img**页面上，导航到 ControlNet 部分。


将您刚刚保存的图像上传到**ControlNet 单元 0**。


![image-20240703173952451](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031739886.png)


大家可以使用我的配置选项。


这里我们需要选择Depth模型，在preprocessor中选择depth\_zoe,model选择control\_xxxx\_depth。


向上滚动到**img2img 画布**。删除图像。


然后使用画图工具绘制一个黑白的模板图。


白色代表光线。


如下所示：


![image-20240703174500514](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031745372.png)


把这个图像上传到**img2img 画布**。


将**调整大小模式**设置为仅调整大小。


将**去噪强度**设置为 0\.9。


点击**生成**。


您应该得到带有横向光源的图像。


![image-20240703174546141](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031745055.png)


如果你不想创建自己的光源，那么可以baidu一下黑白光源图片：


![image-20240703174814660](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031748562.png)


比如第一张光源图片，我们可以得到下面的图片：


![image-20240703174921267](https://flydean-1301049335.cos.ap-guangzhou.myqcloud.com/img/202407031749325.png)


### 备注


不一定必须使用深度控制模型。其他模型，如 canny 和lineart模型，也可以工作。你可以尝试使用预处理器，看看哪一个适合你。


如果您看到不自然的颜色，请减少**Controlnet 权重**。


调整去噪强度并观察效果。
[点我查看更多精彩内容:www.flydean.com](https://github.com)


