# 更新日志
## V1.4.1 (2022-7-28)
### Features
- 【服务端】统一部署脚本，封装local、docker、docker-compose部署方式启动server&web&client   
- 【服务端】支持源码安装Redis与Nginx  
- 【服务端】macOS启动docker desktop  
- 【服务端】完善github action脚本  
- 【工具】更新工具列表

### Docs
- 上传新版本白皮书  
- 调整快速入门指引文档  



## V1.4.0 (2022-7-18)
### Features
- 【客户端】jenkins插件增加分析方案模版ID和分析方案名称参数
- 【服务端】增加扫描方案模板API  
- 【服务器】优化文件服务器鉴权交互  
- 【客户端】QuickScan支持指定分析方案模板进行扫描；支持从环境变量读取文件服务器url和token  
- 【Web端】升级moment依赖
### Docs
- 更新插件使用说明书和启动参数说明



## V1.3.3 (2022-6-29)
### Features
- 【服务端】支持团队、项目组禁用，支持代码库、分支项目删除
- 【服务端】扫描方案支持分支过滤
- 【Web端】支持禁用团队、项目，代码库登记支持ssh_url 
- 【Web端】支持分支过滤配置，修复代码统计文件选中效果，支持工具、依赖凭证移除
- 【工具】增加tca_ql工具
- 【客户端】节点模式不再由客户端加载编译工具的环境变量，避免覆盖机器原有环境变量
- 【客户端】QuickScan模式，异常时输出task.log方便排查问题
- 【客户端】.code.yml支持.yaml后缀
### Bugfixes
- 【客户端】tool_scheme和ini配置共用时，可能出现工具重复，需要对工具库去重后再拉取
### Docs
- 更新TCA Action相关文档
- 更新Jenkins插件文档；增加环境依赖说明
- 更新自定义工具文档，使用工具依赖
- 更新CLS readme



## V1.3.2 (2022-6-16)
### Features
- 【客户端】QuickScan根据语言执行不同的任务
### Docs
- docker-compose部署文档中数据库注意事项



## V1.3.1 (2022-6-14)
### Features
- 【客户端】新增merge quest分支增量扫描  
- 【客户端】新增Quickscan模式  
- 【客户端】localscan支持工具并发  
- 【工具】新增二进制文件依赖分析工具  
- 【服务端】server调整服务监控探测脚本：celery状态判断  
- 【服务端】增加子任务接口，完善部署脚本  
- 【服务端】更新CLS版本v20220613.1  
- 【服务端】基于 CentOS7.9.2009（已测）的运行环境一键安装脚本，并已安装及配置命令 gunicorn 和 celery  
- 【Web端】调整OAuth显示  



## V1.3.0 (2022-6-7)
### Features
- 【工具】新增独立工具Loong
- 【工具】新增Java、JS基础安全规则包
- 【工具】增加Go和Python技术安全规则包
- 【服务端】新增oauth授权及工具依赖管理
- 【服务端】docker-compose部署支持挂载本地日志目录
- 【客户端】支持工具依赖管理
- 【Web端】支持工具依赖管理设置和Git OAuth设置
- 【Web端】团队列表支持滚动加载 

### Bugfixes
- 【服务端】补充scmproxy缺失依赖
- 【服务端】修复issue入库忽略处理操作

### Docs
- 更新工具目录readme
- 更新client README.md



## V1.2.1 (2022-5-24)
### Features
- 【工具】新增Collie/Compass（测试版）工具
- 【工具】添加tscancode系列工具
- 【工具】工具区分编译型和非编译型
- 【客户端】更新cmdscm二进制文件，调整获取ssh端口号方式
- 【客户端】增加腾讯工蜂作为工具拉取源，支持选用
- 【服务端】调整工程配置和文档，支持https克隆
- 【Web端】前端页面优化

### Docs
- 添加集成工具说明文档
- readme增加微信公众号和腾讯开源摘星计划的说明及链接
- 修改帮助文档的脚本名称；修改工蜂镜像仓库链接位置
- 调整自定义规则文档
- 调整doc，优化部署、使用文档



## V1.2.0 (2022-4-27)
### Features
- 【Web端】增加工具管理
- 【工具】增加logback检查的安全规则
- 【服务端】增加TCA server&web 一键部署脚本
- 【服务端】删除main部分异步任务；调整server nginx启动位置
- 【服务端】增加server健康监测
### Docs
- 完善部署和Q&A文档
- 上传工具列表


## V1.1.3 (2022-4-18)
### Features
- 【工具】上传开源合规检查规则
- 【工具】新增PHP安全相关规则
- 【服务端】上线license鉴权
- 【客户端】支持对工具license校验
### Docs
- 更新文档内的工具默认路径
- 增加任务分布式执行能力操作文档
- 增加PR操作流程


## V1.1.2 (2022-4-2)
### Features
- 【服务端】优化部署构建脚本 
### Docs
- 简化前端部署脚本&文档 
- 优化指引文档


## V1.1.1 (2022-3-31)
### Features
- 【工具】增加0daychecker工具
- 【工具】增加Log4j、LogBack漏洞检查规则包

### Docs
- 完善部署文档说明，推荐使用Docker-Compose 2.3.3版本

## V1.1.0 (2022-3-29)
### Features
- 【客户端】client支持arm64架构执行环境
- 【客户端】client新增分布式节点模式
- 【客户端】修改参数isTotal(是否开启全量扫描)判断方式及参数startCommand（启动客户端命令）拼接方式
- 【服务端】支持任务分布式下发
- 【服务端】完善基于minio的文件存储配置
- 【Web端】调整文件资源引用地址
- 【Web端】web模块部署脚本问题修复及优化
- 【Web端】增加管理后台、增加在线分析
- 【Web端】调整前端部署脚本，支持传递nginx配置地址、前端资源部署地址
### Bugfixes
- Jenkins插件命令拼装逻辑修正
### Docs
- 调整pypi下载失败提示
- 调整前端部署文档及脚本
- 更新License



## V1.0.1 (2022-03-01)
### Features
- feat: 【服务端】调整代码库登记ssh url链接格式适配  
- feat: 【工具】上线支持PHP安全工具-Rips  
- feat: 【工具】调整androidlint部分规则描述  
- feat: 【客户端】上线Jenkins插件  
- feat: 【客户端】增加工具拉取可选配置项  
- feat: 【客户端】支持在命令行参数中输入团队编号和项目名称  
- feat: 【客户端】限制PYTHON_VERSION环境变量可选值  
- feat: 【客户端】增加在docker中快速使用client的方式  

### Bugfixes
- fix: 【服务端】补充缺失的依赖  
- fix: 【Web端】修复下载codedog.ini失败提示
 
### Docs
- doc: 上线部署文档Q&A  
- doc: 优化部署文档、帮助文档说明  
- doc: 增加产品白皮书  
- doc: 补充redis和nginx源码安装参考文档



## V1.0.0
初始发布