
# readme

这个地方是通过 run文件来进行安装.

1. Perform the [pre-installation actions.](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html#pre-installation-actions)
2. Disable the Nouveau drivers.
3. Reboot into text mode (runlevel 3).



***

## 7.3 Disabling Nouveau


### 7.3.6. Ubuntu

1. Create a file at /etc/modprobe.d/blacklist-nouveau.conf with the following contents

```
blacklist nouveau
options nouveau modeset=0
```

2. Regenerate the kernel initramfs
```shell
sudo update-initramfs -u
```

3. 以文本的方式启动 

4. Verify that the Nouveau drivers are not loaded. If the Nouveau drivers are still loaded, consult your distribution's documentation to see if further steps are needed to disable Nouveau.

5. 进入安装提示:

6. Reboot the system to reload the graphical interface.


```text
===========
= Summary =
===========

Driver:   Installed
Toolkit:  Installed in /usr/local/cuda-11.6/

Please make sure that
 -   PATH includes /usr/local/cuda-11.6/bin
 -   LD_LIBRARY_PATH includes /usr/local/cuda-11.6/lib64, or, add /usr/local/cuda-11.6/lib64 to /etc/ld.so.conf and run ldconfig as root

To uninstall the CUDA Toolkit, run cuda-uninstaller in /usr/local/cuda-11.6/bin
To uninstall the NVIDIA Driver, run nvidia-uninstall
Logfile is /var/log/cuda-installer.log

```

7. Verify the [device nodes]()  are created properly.


这个也测试成功.

8. Perform the [post-installation actions]().

这个地方看看有什么.





***

测试 OK, 这个地方临时记录如下:

1. 安装的有 opengl. YES
2. 没有安装 nvidia-drm . NO
3. 安装的有 update NVIDIA X Config , YES


