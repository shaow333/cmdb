1.项目分析：
   1).用户管理
   
         *.个人中心
		 
		        * 显示个人信息，以及可以，修改个人信息，及用户密码
			
         *. 用户列表
		 
		        * 显示所有已添加用户信息，可以对用户进行，增加，删除，修改
		
   2).资产管理	
   
         *.机房管理
		 
		        * 显示已添加机房信息，可以对机房信息，进行，增加，删除，修改
		 
         *.机柜管理
		 
		        * 显示已添加机柜列表，可以对机柜，进行，增加，删除，修改
			 
         *.服务器管理
		 
		        * 显示已添加主机列表，可以对主机，进行，增加，删除，修改				 
  3).工单系统
            
         *.工单申请
			
		        * 提交新工单
			
         *.申请列表
			
		        * 显示已提交，未完成工单,可对工单状态，工单信息进行修改
				
         *.历史工单
			
		        * 可以看到，已提交所有工单，可以查看工单详情
			
  4).第三方接口

         *.批量执行命令
		 
		        * 调用 ansible接口，远程执行命令

		 
  5).日志可视化
  
         *.网站浏览状态分析  
		 
		        *.查库获取状态码统计数据,返回前端，进行渲染	
				
          *.网站访问IP来源
               			  
		        *.查库获取各省访问ip统计信息，格式化输出，前端渲染          
2.项目功能分析:
   1).用户管理
   
       *.用户登录/退出 
	   
	        函数文件: login.py 
		   
		          login()            获取前端输入账号密码，进行判断是否正确,用户是否锁定
		          loginout()         用户退出
                  
       *.个人中心
	   
	        函数文件:  user.py
		   
		          userinfo()           用户个人中心，显示已登录用户个人信息
		          updatepwd()     修改个人密码
		          userupdate() 修改个人资料
		   
	   *. 用户列表
	       
	        函数文件： userlist.py
			
		          listupdate()         用户列表，显示已添加用户列表
		          update()           更新用户信息
		          reg()              添加新用户
		          dlt()           删除用户
		
   2).资产管理

         *.机房管理
		     
	        函数文件：idc.py
			      
		          idclist()             显示已添加 idc列表
		          adddic()          添加机房
		          updataidc()       修改机房信息
		          deleteidc()       删除机房
	
         *.机柜管理
              
	        函数文件： cabinet.py
                   
		          cbtlist()         机柜列表，显示已添加机柜信息
		          addcbt()      添加新机柜
		          updatacbt()   机柜信息修改
		          deletecbt()   删除机柜
			 
         *.服务器管理
     	    
	        函数文件: server.py
			 
		          serverlist()          显示已添加机服务器列表
		          addserver()       添加新服务器
		          updataserver()    更新服务器信息
		          deleteserver()    删除服务器
	                               
  3).工单系统
          
	        函数文件：  job.py
        	  
        *.工单申请
		    
		          jobadd()          添加新工单
			
        *.申请列表
			
		          joblist()         工单列表
		          jobupdata()       更新工单信息
		          jobdetail()       查看工单详情
			     
        *.历史工单
		    
		          historylist() 历史工单列表
			
			
  4).第三方接口	

	        函数文件：  ansibles.py  调用 ansible API 文件	  commands.py
			
		          ansible()         ansible远程执行命令
		          history()         ansible历史记录	  
                  					  

            			
  6).日志可视化
      
        *.日志状态饼图
		
  			函数文件：  log.py
			
		          log()             日志页面
		          status()          日志状态数据

        *.日志来源地图

  			函数文件：  map.py			

		          map()             地图展示
		          mapdata()         传输地图数据			
3流程图
![image](https://github.com/shaow333/cmdb/blob/master/img/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20171121140809.png)

4.演示
演示服务器地址 http://172.16.0.100:9999/login/ 账号: lhs 密码 12345678(公司内网启动，外网暂不能登录，后续更新）
用户登陆界面
![image](https://github.com/shaow333/cmdb/blob/master/img/1.png)
用户注册
![image](https://github.com/shaow333/cmdb/blob/master/img/2.png)
用户编辑
![image](https://github.com/shaow333/cmdb/blob/master/img/3.png)
添加服务器界面
![image](https://github.com/shaow333/cmdb/blob/master/img/4.png)
服务器更新界面
![image](https://github.com/shaow333/cmdb/blob/master/img/5.png)
工单申请界面
![image](https://github.com/shaow333/cmdb/blob/master/img/6.png)
工单处理界面
![image](https://github.com/shaow333/cmdb/blob/master/img/7.png)
工单历史界面
![image](https://github.com/shaow333/cmdb/blob/master/img/8.png)
日志来源地图
![image](https://github.com/shaow333/cmdb/blob/master/img/11.png)
