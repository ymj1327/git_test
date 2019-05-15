1, 登录服务器：ssh fengye@114.212.85.200

2, 拷贝文件\文件夹到服务器
文件：
   命令格式：scp local_file remote_username@remote_ip:remote_folder 
   示例：scp /home/space/music/1.mp3 root@www.runoob.com:/home/root/others/music
        scp ~/test/1.txt fengye@114.212.85.200:~/yimengjun
文件夹：
   命令格式：scp -r local_folder remote_username@remote_ip:remote_folder
   示例：scp -r /home/space/music/ root@www.runoob.com:/home/root/others/ 
        scp -r /media/psf/robocup代码/12/34/ fengye@114.212.85.200:~/yimengjun/

注：从服务器拷贝文件
   示例：scp fengye@114.212.85.200:~/gaozhongye/RoboCup3D/kick2.skl ~
	scp -r fengye@114.212.85.200:~/yimengjun/12/ ~

3, 服务器A：运行rcssserver3d

4, 本地：本地运行RoboViz
	cd ~/robocup/RoboViz-dev/bin/linux-amd64
	./roboviz.sh --serverHost=114.212.85.200

RoboViz相关:https://github.com/magmaOffenburg/RoboViz

5, 服务器B：执行代码

6, 退出服务器：logout