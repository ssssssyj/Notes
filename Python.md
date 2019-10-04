# Intstall offline Python packages

情境：很多公司防火墙环境下无法使用 pip install 直接安装 packages，可以用以下方法解决

## Solution:

1. 使用可以连接外网的设备安装所需要的 packages
2. 在该设备上 cmd 中进行操作
   ```
   pip freeze > nameitasyouwant.txt
   pip download  -r nameitasyouwant.txt  -d  /user/.../bags
   ```
   ##### Note: 
   - txt文件里会包含 pip 安装过的包，有哪些已安装的包可以通过下面的代码直接查看
   ```
   pip list
   ```
   - pip download 代码行最后的路径是你希望的输出路径，如果不进行操作文件会存储在 cmd 打开后的默认路径下
3. 此时相关的包就已经完成下载并存储至本地，可以直接拷贝至需要安装包的机器上，按照常规的操作在cmd中 pip install 命令后直接拖拽安装文件即可

   ##### Note:
   此方法并非最优解，与大部分互联网可查的解决方法有较大出入，但实际操作上比较简单，对新手更友好
