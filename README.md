# iphone_dcim_backup
backup iphone photo

231027： 
添加：
1. 将照片/视频文件按年月分文件夹的代码。
2. 提取和照片同名MOV文件的代码。

使用说明：
1. 执行"move_by_year"将文件从总路径移动到年份路径。
2. 执行"move_by_month"将年份路径中的文件按月添加到月份子文件夹中。
3. 执行"move_mov"将和照片/视频同名的mov文件提取到年份文件夹的对应[MOV_月份]文件夹中。



# 使用说明：
## 实现功能：
	在windows系统的电脑上有线备份iphone相册所有内容，运行代码即可开始备份。
	若备份过程中停止，重新开始备份可以继续备份未备份内容。

## 准备工作：
	Iphone方面：
		1. 电脑上安装itunes软件
		2. 有线连接iphone和电脑，点击确认手机上弹出的信任设备提示，确保“我的电脑”中能显示Iphone这个设备路径，并且路径中DICM文件夹不为空。每次备份时都要确保这步的条件成立。
	
	代码方面：
		1. 安装python
		2. 安装python依赖包：
		pythoncom、argparse、pypiwin32、tqdm、json
	
## 备份步骤：
	1. 连接iphone和电脑，确保iphone设备在“我的电脑”中显示，并且设备路径中的DICM路径下不为空，可能需要等待1-2min。
	2. 在代码开头处根据实际修改DICM路径和备份的目标路径，运行代码。路径示例：
	
	
## 注意：
	1. 如果备份过程中iphone和电脑莫名断开连接*，无须操作，代码会自动等待iphone重连上然后继续备份。
	2. 代码运行时会生成两个log文件，记录了已成功备份的文件，若删除，则下次备份时会重新备份所有文件，否则只备份没有备份过的文件。
	
*莫名断开连接是指通常我在备份1、200个文件后，尽管没有碰连接线，但是“我的电脑”中突然不显示iphone设备或者DICM文件夹下变为空，即电脑和iphone失去通信，这个问题在我备份时总会遇到，可能是我的线的问题，也可能是iphone的某种“机制”使然。不过不管怎么样，通常等待一会iphone会再次连接上电脑。

## 参考：
	1. https://gitlab.com/lassi.niemisto/iphone-photo-dump
主要根据这位大神的代码简易修改而来


![image](https://github.com/Li-Mingshuang/iphone_dcim_backup/assets/71756865/97611749-042f-4fdc-a8e8-3f68fd74f727)
![image](https://user-images.githubusercontent.com/71756865/210072452-db101dcb-d0d3-45d0-8d59-e28d03d2fdd1.png)
