利用burpsuit截获邮件（含附件）
</br>之前我们组一直遇到虚拟机不能联网的问题，经老师解说后，我们将网络模式改为桥接模式，并给虚拟机配置和物理主机在同一网段的IP以及子网掩码和网关
</br>![](https://github.com/hua12/MyPic/blob/master/%E7%BD%91%E7%BB%9C%E6%A8%A1%E5%BC%8F%E4%B8%BA%E6%A1%A5%E6%8E%A5.PNG)
</br>![](https://github.com/hua12/MyPic/blob/master/%E4%B8%BB%E6%9C%BAIP%E4%BF%A1%E6%81%AF.PNG)
</br>![](https://github.com/hua12/MyPic/blob/master/%E8%99%9A%E6%8B%9F%E6%9C%BAP%E4%BF%A1%E6%81%AF.PNG)
</br>但是我们仍不能一直做到联网，当把burpsuit中intercept关掉的时候才可以联网，然后打开需要截获的界面后再将intercept打开！
</br>实验步骤如下：
</br>（1）首先打开burpsuit设置代理，监听本地8080端口
</br>![](https://github.com/hua12/MyPic/blob/master/burp%20suite%E4%BB%A3%E7%90%86%E8%AE%BE%E7%BD%AE.PNG)
</br>（2）接着设置浏览器代理，跟burpsuit里面对应
</br>![](https://github.com/hua12/MyPic/blob/master/%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BB%A3%E7%90%86%E8%AE%BE%E7%BD%AE.PNG)
</br>（3）接着，打开要进行截获的邮箱发送页面，可以看到burpsuit的proxy工具颜色变橙色
</br>（4）在拦截的页面输入收件人地址等信息，并上传附件，发送
</br>![](https://github.com/hua12/MyPic/blob/master/%E6%8F%92%E5%85%A5%E9%99%84%E4%BB%B6%E5%8F%91%E9%80%81%E9%82%AE%E4%BB%B6_%E7%9C%8B%E5%9B%BE%E7%8E%8B.png)
</br>（5）拦截成功！
</br>![](https://github.com/hua12/MyPic/blob/master/附件_看图王.png)
</br>从中可以看到关于附件的一些信息，但是是一堆乱码，还需要利用字典进一步的破解，然而我并没有找到字典，本想从网上下载，但是没有找到资源
