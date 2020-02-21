##### 显示文件列表  ls

- -i  显示文件的内容（链接的时候可以看出来）

##### 只能显示文件内容，不能修改 cat

-  cat 文件名 文件名 可以显示连接多个文件显示


##### 分页显示文件内容, 不能修改 less
- 回车  	前进一行
- 空格      前进一页
- d           前进半页
- y           后退一行
- b           后退一页
- =          显示在文件中的位置
- h          显示帮助文档  按q可推出
- /            进入搜索模式  
  - 回车  		显示结果
  - n               下一个
  - N               上一个

##### 显示文件开头行  heade  默认为10行

- -n   显示多少行

##### 显示文件末尾 tail

- -n  显示多少行   tail -n 30 syslog
- -f  实时检查文件是否有追加内容并显示
- -f  -s  每隔多少秒检查文件是否更新    tail -f -t 5  syslog  默认是1秒

##### 创建空白文件 touch

- touch 文件名  			文件名   创建多个文件
- touch  "文件   名"       添加双引号可以创建有空格文件

##### 创建文件夹  mkdir

- mkdir 文件夹名  文件夹名  创建多个文件夹
- mldir "文件夹   名"  添加双引号可以创建有空格的文件夹
- -p  递归创建文件夹      mkdir -p   one/two/three

##### 拷贝文件和目录   cp

- cp  file   newfile 复制 
- cp file  one/  复制文件到one文件夹下
- cp file  one/newfile   复制文件到one文件夹下且改名为newfile
- cp -r one  onecopy   复制文件夹
- cp  *.txt  folder   复制所有的txt到folder子文件夹下

##### 移动文件   mv

- mv  file  one/  移动file到one下
- mv  file  newfile  改名字
- mv  a*  one/  移动a开头的到one下

##### 删除文件  rm

- rm  a.txt  b.txt   删除多个文件
- -i  a.txt   询问是否删除a.txt
- -f  强力删除，不会询问
- -r  递归删除

##### 链接文件 ln

- ln  file1 file2   硬链接，两个文件共享内容（硬链接只能链接文件）
- -s   创建软链接   ln -s  file1 file2

##### 切换到超级用户

- sudo su （ubuntu）
- sudo su -   (centos等)

##### 添加用户  adduser

- adduser  userName

##### 修改用户密码  passwd

- passwd userName

##### 删除用户 deluser

- deluser userName
- --remove-home   连带删除此用户的home文件夹

##### 查看群组

- groups  userName

##### 创建群租 addgroup

- addgroup  groupName

##### 修改用户账户  usermod

- -g  给用户切换群组（原来群组内没有这个用户了）  usermod -g groupName  userName
- -G  切换多个群组 （原来群组内没有这个用户了）    usermod -G groupName1,groupName2,groupName3 userName
- -a 保留原来群组    usermod -aG newGroupName userName

##### 删除群组   delgroup

- delgroup  groupName

##### 修改文件的所有者和群组（root）

- chown newUserName file   改变文件的所有者
  - -R  递归，所有
- chgrp  newGroup file   改变文件的群组