---
编译原理一般流程
---
1. 配置（configures）
    configure/脚本文件/
    由auotoconf/工具生成/
    编译器运行脚本，获得编译参数
2. 确定标准函数库（standard library）和头文件（harder）
3. 确定依赖关系
    编译顺序保存在makefile文件中，并由configure运行生成
4. 头文件的预编译（precompliation）
5. 预处理（preprocessing）
6. 编译（compliation）
    源码——>汇编码（assembly）——>机器码
    or  源码——>机器码
    对象文件（object file）转码后的文件
7. 连接（linking）
    把外部函数的代码（通常是后缀名为.lib和.a文件）添加到可执行文件中
    >注：make命令作用：完成4-7步

8. 安装（Installion）
    创建目录，保存文件，设置权限。。。
9. 操作系统连接
    >注：make，install命令作用：完成8、9两步

10. 生成安装包
11. 动态连接【运行时动态引用外部函数库】（Dynamic linking）
    G.安装包会比较小，多个应用程序可以共享库文件
    B.用户必须事先安装好库文件，而且脚本和安装位置都必须符合要求，否则就不能运行
