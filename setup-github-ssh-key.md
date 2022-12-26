### 1. 查看本地是否存在SSH Key
终端：ls -al ~/.ssh  
若id_rsa和id_rsa.pub存在，证明本地已经存在SSH密钥，跳转步骤3   
note: id_rsa 可以自定义名称    
### 2.生成SSH Key
> 生成：ssh-keygen -t rsa -C “emAIl@xxx.com”    

生成后会提示一下消息   
Generating public/private rsa key pAIr.   
Enter file in which to save the key (/Users/xxx/.ssh/id_rsa):   

之后系统会提示你输入key 文件的名称     
提示输入passphrase时, 可以直接回车不设定密码。 
> 添加：ssh-add ~/.ssh/id_rsa (或者是其他自己定义的key文件名称)    

此时会要求输入密码,之前输入了密码,此时就再次输入,没输入就enter   
成功之后终端会显示以下消息。  

Identity added: /Users/xxx/.ssh/id_rsa (/Users/xxx/.ssh/id_rsa)

### 3.查看SSH key
进入目录: cd ~/.ssh    
查看: cat id_rsa.pub (或者是其他自己定义的key文件名称)    
拷贝public key文件中内容

### 4.创建Github SSH key, 建立和本地信任
登陆github账号  
点击右上角的profile icon. 选择settings  
在打开的account settings中, 点击SSH and GPG keys, 并新建一个SSH key

到此为止, 便可以使用git 命令行来操作和git repo的交互了.


