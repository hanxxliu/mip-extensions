# mip-custom

## 文档信息

- 所属产品项目：定制化MIP
- 产品版本：v1.0.11
- 文档版本：v1.0.3

撰写人|修改日期|修改内容|更新版本
---|---|---|---
王培|2017-04-19|创建文档|v1.0.0
王培|2017-05-02|增加必要属性 title|v1.0.1
王培|2017-05-03|增加必要脚本说明|v1.0.2
王培|2017-06-06|修改文档示例|v1.0.3

## 说明

mip-custom 定制化 MIP 组件，想在页面中加入定制化内容，必须引入这个组件。MIP 页面改造参考官网文档：https://www.mipengine.org/doc/00-mip-101.html。

标题|内容
----|----
类型|通用
支持布局|responsive,fixed-height,fill,container,fixed
所需脚本|https://mipcache.bdstatic.com/static/v1/mip-custom/mip-custom.js<br/> https://mipcache.bdstatic.com/static/v1/mip-mustache/mip-mustache.js<br>https://mipcache.bdstatic.com/static/v1/mip-fixed/mip-fixed.js

## 示例

### 基本用法

```html
<mip-custom>
    <script type="application/json">
        {
            "accid": "e2217bab684fbb898dccf04b",
            "title": "%E8%BF%99%E9%87%8C%E6%98%AF%E6%A0%87%E9%A2%98"
        }
    </script>
</mip-custom>
```

### 完整版示例

```html
<!DOCTYPE html>
<html mip>
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,minimum-scale=1,initial-scale=1" />
    <title>title</title>
    <link rel="stylesheet" type="text/css" href="https://mipcache.bdstatic.com/static/v1/mip.css">
    <link rel="canonical" href="对应的 h5 页面 url">
    <style mip-custom>
    </style>
</head>
<body>
    <h2>定制化MIP示例页面</h2>
    <p>正文</p>
    <mip-custom>
       <script type="application/json">
            {
                "accid": "e2217bab684fbb898dccf04b",
                "title": "%E8%BF%99%E9%87%8C%E6%98%AF%E6%A0%87%E9%A2%98"
            }
        </script>
    </mip-custom>
    <script src="https://mipcache.bdstatic.com/static/v1/mip.js"></script>
    <script src="https://mipcache.bdstatic.com/static/v1/mip-mustache/mip-mustache.js"></script>
    <script src="https://mipcache.bdstatic.com/static/v1/mip-custom/mip-custom.js"></script>
</body>
</html>

```

## 属性

### accid

说明：分润平台帐号ID，暂时需要联系百度 PM 手工申请   
必选项：是   
类型：字符串  
取值范围：无  
单位：无   
默认值：无   
 
### title

说明：页面内容标题，需要对中文编码（encodeURIComponent）   
必选项：是   
类型：字符串   
取值范围：无   
单位：无   
默认值：无   

## 注意事项

- 每个 MIP 页面中的定制化模板，插入之前必须准备 **accid**，需要联系百度 PM 手工申请
- title 是页面中内容标题，**不是**`<title>`标签中的文本，同时需要对中文编码（encodeURIComponent） 

