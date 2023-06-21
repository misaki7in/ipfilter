`    ## 0X01 工具背景
    在护网场景中，作为乙方公司的蓝队防守人员，经常会遇到一些客户具有相当多的**不可封禁的IP地址**，如**负载均衡IP，站前代理IP，内网漏扫IP，云防节点IP地址**。尽管我们在研判流量威胁时，已经确认了这些IP地址确实存在攻击流量，但是在防火墙封锁恶意IP地址的时候，经常要手工剔除这些IP，十分繁琐。
    之前笔者在SXF担任应急响应工程师时，经常会看见一线安服工程师因为封锁IP未过滤不可封禁IP地址，导致**客户的业务中断甚至全部断网【封锁了出口IP】，最后被记二级黑事件甚至辞退。**
    于是针对该场景于2022年8月hvv时开发了IP地址的自动过滤工具，并于2023年3月添加**了微步自动化查询IP地址和IP属性【是否具备恶意标签】**的功能，方便防守人员快速输出威胁IP话术，具体使用如下图所示:
    ## 0X02 使用方法
    1.录入白名单的标题，如**XX单位【云防节点】，**输入白名单规则，支持三种IP格式的输入。
    [![pCGnhVS.png](https://s1.ax1x.com/2023/06/21/pCGnhVS.png)](https://imgse.com/i/pCGnhVS)
    [![pCGnWb8.png](https://s1.ax1x.com/2023/06/21/pCGnWb8.png)](https://imgse.com/i/pCGnWb8)
    <br>
    2.根据需求启用或新建白名单规则，输入对应的IP段，即可实现IP地址的过滤
    [![pCGnoCj.png](https://s1.ax1x.com/2023/06/21/pCGnoCj.png)](https://imgse.com/i/pCGnoCj)
    3.如果你具有微步的APItoken的话【**注意:微步API需要申请，并且非企业用户每天可查询额度固定为50，超出则无法查询**】，可以输入APItoken，对IP地址进行威胁查询和地址查询，并过滤出恶意标签的IP地址。

    [![pCGn72n.png](https://s1.ax1x.com/2023/06/21/pCGn72n.png)](https://imgse.com/i/pCGn72n)
    <br>
    获取微步API的方式: 访问链接: [https://x.threatbook.com/v5/myApi](https://x.threatbook.com/v5/myApi) 

    **注意: 注意确认自己每日的API查询IP的额度，个人用户较少，每天只有50次，建议申请企业用户。**
    [![pCGnHvq.png](https://s1.ax1x.com/2023/06/21/pCGnHvq.png)](https://imgse.com/i/pCGnHvq)

    ## 0X03 效果展示
    
    [![pCGnqK0.png](https://s1.ax1x.com/2023/06/21/pCGnqK0.png)](https://imgse.com/i/pCGnqK0)
    **最终结果整理成值守话术，美滋滋~~~~,再也不担心封错IP地址。**
    [![pCGnT8s.png](https://s1.ax1x.com/2023/06/21/pCGnT8s.png)](https://imgse.com/i/pCGnT8s)
    ## 0X04 使用注意
    1.项目目录文件如下
    [![pCGn4Ug.png](https://s1.ax1x.com/2023/06/21/pCGn4Ug.png)](https://imgse.com/i/pCGn4Ug)
    2.项目文件哈希值如下**【注意别被攻击队钓鱼了】**
    [![pCGn55Q.png](https://s1.ax1x.com/2023/06/21/pCGn55Q.png)](https://imgse.com/i/pCGn55Q)
    ```
    SHA1 的 IPFilter.exe 哈希:
    ec2302560afdb52b2fe772570df7943808476158
    MD5 的 IPFilter.exe 哈希:
    f102e67b979a4daefd195ca8e859b537
    ```
    3.考虑到部分小伙伴有特殊的需求，可以加我微信拿源码
    [![pCGKfhQ.png](https://s1.ax1x.com/2023/06/21/pCGKfhQ.png)](https://imgse.com/i/pCGKfhQ)



`