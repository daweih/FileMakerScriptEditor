# FileMakerScriptEditor
Writing script in FlileMaker solution and use these script to process data stored in FileMaker solution. 在 FileMaker 内编辑 perl, R, JavaScript 等脚本并使用这些脚本处理 FileMaker 内存储的数据。

本解决方案采用了内嵌 JavaScript 包代码的模式，可以保证结局方案内的 Web Viewer 更稳定。

采用 FileMaker 存储脚本的输入数据，进行脚本的编辑，调用脚本处理存储的数据。本解决方案可以作为小型生物信息/分子生物学实验室的脚本管理工具使用。

* 支持 FileMaker 13 及以后的版本（旧版本未进行测试）。

## Base64Decode 函数版本问题

由于 FileMaker 13 及之前的版本不支持 Base64Decode 结果直接保存到文本字段或从文本字段生成文件（细节请看[本文](http://daweih.github.io/2016/09/25/filemaker2/)），因此采用 ScriptMaster 提供的函数解决，也没有加载额外的包。

FileMaker 15 之后，Base64Decode 的功能强大很多，灵活性很高。可以参考示例文件 base64encode.container.fmp12。


