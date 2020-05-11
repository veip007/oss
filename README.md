# oss
循环下载-刷流量

**使用方法**
```bash
wget -N --no-check-certificate https://github.com/veip007/oss/raw/master/oss.sh && chmod +x oss.sh &&  "https://www.baidu.com" &  #指定url
```
```bash 
#设定下载线程
wget -N --no-check-certificate https://github.com/veip007/oss/raw/master/oss.sh && chmod +x oss.sh &&  "https://www.baidu.com" 8 &   #指定url和8线程
```

**另一个脚本**

```
echo "while [ 1 ]" > _ins.sh
echo "do" >> _ins.sh
echo "wget -q -t0 -O /dev/null http://kuailehuzanapp.oss-cn-beijing.aliyuncs.com/kuailehuzan.apk" >> _ins.sh
echo "done" >> _ins.sh
for i in `seq 1 20`
do
     nohup bash _ins.sh > /dev/null 2>&1 &
     echo "thread $i start!"
done


#手动更改链接，保存为sh然后自动后台20线程运行。20线程可以手动修改增加或减少

reboot重启来关闭脚本
```
