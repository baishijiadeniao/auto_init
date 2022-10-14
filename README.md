装机自动化脚本

搜索"务必修改"字眼，将ip和主机名进行修改
脚本默认服务器的主机名为gpu01，如果不是则需要将server和client中的光谱改为你nfs服务器和nis服务器的主机名

<!-- 执行方法：
sh install_ansible
ansible all -m script -a "/root/auto_init_test/init"
ansible all -a "reboot"
ansible server -m script -a "/root/auto_init_test/server"
ansible other -m script -a "/root/auto_init_test/client" -->

测试脚本的时候常常卡在ansible中，建议单个脚本执行：

server执行：

sh install_ansible

sh init

sh server



client执行：

sh init

sh client
