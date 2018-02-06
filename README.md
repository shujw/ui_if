# ui_if
提供调用iAP后台功能的REST接口2

### 概要
对一部分iAP的标准系统功能画面进行解耦，提供可以通过REST方式调用相关后台功能的WebAPI接口。
主要考虑为通过前后台分离的形式重新订制开发可以完成iAP系统功能的前台画面（PC版和移动版）

### 提供资料内容
- 接口代码及一部分接口的调用示例代码。
- 接口使用说明文档。

### 使用前提
- 现阶段提供的接口是基于iAP 2017冬季版进行开发和测试的，
- 请尽量使用在较高版本的iAP上。
- **部分接口代码基于iAP的Terasoluna的Java框架进行开发。需要在安装iAP时选择【Terasoluna开发框架】相关模块。否则相关接口代码无法正常编译，相关接口也无法正常使用。**
- **如需使用【认证相关接口】，需要在安装iAP时选择【Session管理】相关模块。否则相关接口代码无法正常编译，相关接口也无法正常使用。**
- **如需使用【通知相关接口】，需要在安装iAP时选择【通知Notice】相关模块。否则相关接口代码无法正常编译，相关接口也无法正常使用。**

### 使用方法
1.通过eBuilder建立一个新的iAP工程。
2.将github的project/src/下内容复制到新的iAP工程的src目录下。
3.编译成功后启动该工程，即可调用相关接口。
> 如需部署到实际项目中的部署方法和一般标准iAP工程的部署方法相同。

> 调用各接口时，首先要进行Login认证。
> - 方法1：通过iAP标准画面进行登录后，再调用各种接口。
> - 方法2：客户端调用认证接口，传递iAP中登记的用户Cd和密码进行Login后，在同一Session中再调用其它接口。

### 关于接口的使用说明文档
- 保存在github上的文档<ndims_iap_ui_if.xsls>文件中描述了大部分接口的调用方法和示例以及相关接口源代码的详细信息。
同时，接口的完整参数说明提供在线的文档。
> 请参考：<a href="http://54.223.44.201/ui/if/doc" target="_new_">ui_if在线接口文档</a>
**关于接口的文档更新，以在线接口文档为优先。**

### 注意点
- 相关接口代码处于测试阶段，如需在实际项目中使用，建议对使用接口的相关功能进行完整测试后再上线。
- 接口代码可以参考后，自行进行修改和使用。
- 提供的接口代码并未进行专属权限的封装。但有些接口内部调用的系统功能会检查调用的用户是否具有相关权限。
如果权限不足时可能会发生调用错误。
> 例如，不具备工作流权限的用户Login后调用工作流相关接口可能会发生错误或不能正确获得调用结果。
- 提供的接口并不是iAP的产品标准功能，接口开发方不对接口造成的影响负责。
