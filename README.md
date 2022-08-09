# trace-cmd
trace-cmd for arm android
***********************************************************************  
Author: duguowei  
Date: 2021-12-8  
Email: duguoweisz@gmail.com  
Phone: 13417431640  
WeChat: dgw_cn  
Kernel: 5.10.66  
Android: 12  
***********************************************************************  
在Ubuntu上编译可在android上独立使用的静态trace-cmd，如下:  
***********************************************************************  
1.apt-get source trace-cmd  
        https://trace-cmd.org/  
        Latest stable release: trace-cmd-v2.9.6  
        
2. install arm gcc  
        apt-get install gcc-arm-linux-gnueabi  
        
3. Compile  
        make LDFLAGS=-static CC=arm-linux-gnueabi-gcc trace-cmd  
        
4. Fetch data  
        adb push trace-cmd /data/local/tmp/  
        adb shell /data/local/tmp/trace-cmd ...  
        adb pull /data/local/tmp/*.dat .

5. apt-get install kernelshark  
        kernelshark *.dat
***********************************************************************  
6.如果仅仅是在ubuntu上安装，如下即可：  
sudo apt install trace-cmd  
sudo apt-get install kernelshark
