# 说明
基于archer，调整部分自需功能，[查看开发计划](https://github.com/hhyo/archer/projects/1)  

## 系统体验
[在线体验](http://52.221.195.102) 
  
|  角色 | 账号 | 密码 |
| --- | --- | --- |
|  管理员| archer | archer |
|  工程师| engineer | archer |
|  DBA| dba | archer |


## 功能说明
1. 组管理  
   支持自定义组，组成员之间审批流程隔离、主库配置隔离
2. 审批流程改造  
   SQL上线审核、查询权限审核接入工作流，审批流程支持多级，自主配置
3. 跳过inception执行工单  
   对于inception不支持的语法，如子查询更新，DBA可以跳过inception直接执行，但无法生成回滚语句  
4. 快速上线其他实例  
   在工单详情可快速提交相同SQL内容到其他实例，可适用于test>beta>ga等多套环境维护的需求
5. 数据库会话管理  
   管理主库实例的连接会话，可以批量KIll PROCESS
6. 配置项动态化  
   除数据库依赖外大多数配置项都转移到数据库中，可动态变更，避免重启服务
7. SQL工单类型区分    
   自动判断DML&DDL  
7. SQL工单自动审批    
   支持正则判断工单是否需要人工审批 
8. 工单通知人  
   发起SQL上线时可以选择通知对象，将会在申请时邮件抄送给对方
9. 菜单栏调整  
   多级菜单展示  
   
## 部署
### 基础环境依赖
Python>=3.6  
Django==2.0.6  

### 安装
```bash
git clone https://github.com/hhyo/archer.git 
pip3 install -r requirements.txt -i https://mirrors.ustc.edu.cn/pypi/web/simple/ 
```
### [启动](https://github.com/hhyo/archer/tree/github#启动前准备)  

### 采取docker部署
archer镜像对应的是版本是:lihuanhuan
* inception镜像: https://dev.aliyun.com/detail.html?spm=5176.1972343.2.12.7b475aaaLiCfMf&repoId=142093
* archer镜像: https://dev.aliyun.com/detail.html?spm=5176.1972343.2.38.XtXtLh&repoId=142147    

