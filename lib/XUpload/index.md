---
category: Components
type: Data Display
subtitle: 图片上传
cols: 1
title: XUpload
---

上传文件

## 何时使用

- 需要上传图片的页面

## API

### XUpload


| 参数      | 说明                                      | 类型         | 默认值 |
|----------|------------------------------------------|-------------|-------|
|accept	|接受上传的文件类型, 详见 input accept Attribute	|string	|无|
|action	|必选参数, 上传的地址	|string/(file) => Promise	|无|
|directory	|支持上传文件夹（caniuse）|	boolean	|fasle|
|beforeUpload|	上传文件之前的钩子，参数为上传的文件，若返回 false 则停止上传。支持返回一个 Promise 对象，Promise 对象 reject 时则停止上传，resolve 时开始上传。注意：IE9 不支持该方法。|	(file, fileList) => boolean / Promise	|无
|customRequest	|通过覆盖默认的上传行为，可以自定义自己的上传实现	|Function	|无|
|data	|上传所需参数或返回上传参数的方法	|object/(file) => object	|无|
|defaultFileList	|默认已经上传的文件列表	|object[]	|无|
|disabled|	是否禁用|	boolean	|false|
|fileList	|已经上传的文件列表（受控），使用此参数时，如果遇到 onChange 只调用一次的问题 |	object[]	|无|
|headers|	设置上传的请求头部，IE10 以上有效|	object|	无|
|listType	|上传列表的内建样式，支持三种基本样式 text, picture 和 picture-card	|string|	'text'|
|multiple	|是否支持多选文件，ie10+ 支持。开启后按住 ctrl 可选择多个文件。	|boolean	|false|
|name	|发到后台的文件参数名|	string	|'file'|
|showUploadList|	是否展示uploadList, 可设为一个对象，用于单独设定 showPreviewIcon 和 showRemoveIcon|	Boolean or { showPreviewIcon?: boolean, showRemoveIcon?: boolean }	|true|
|supportServerRender|	服务端渲染时需要打开这个|	boolean	|false|
|withCredentials|	上传请求时是否携带 cookie|	boolean	|false|
|onChange	|上传文件改变时的状态|	Function	|无|
|previewVisible|控制显示预览对话框|boolean|无|
|onPreview	|点击文件链接或预览图标时的回调|	Function(file)	|无|
|previewImage|点击生成预览的图片链接|string|无|
|onCancel|取消预览回调函数|Function|无|
|onRemove  	|点击移除文件时的回调，返回值为 false 时不移除。支持返回一个 Promise 对象，Promise 对象 resolve(false) 或 reject 时不移除。              	|Function(file): boolean/Promise |无 | 