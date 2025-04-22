[原创]某企业级加固[四代壳]VMP解释执行+指令还原 
发表于: 2020-1-5 05:42  22661
  

A | G | op BBBB F|E|D|C 

根据opcode克制总共6个字节，对应的就是 

A=1  G=0 op=6f  BBBB就是 331c,然后是C=1 D=0 E=0 F=1

    所以这里转换过来就是

next

--------------------------------------------------------------------------------------------------------------------------------

5511   6d00[A=2]op{vC, vD},kind@BBBB

1155 invoke-virtual  

006d  取MethodiD  requestWindowFeature     (I)Z

0001  参数

iput-object p0, p0,Lcom/wangzhong/fortune/ui/activity/BaseActivity;->a:Lcom/wangzhong/fortune/ui/activity/BaseActivity;;

--------------------------------------------------------------------------------------------------------------------------------



next  继续往下走，

--------------------------------------------------------------------------------------------------------------------------------

53 10 6D 00         [A=2]op{vC, vD},kind@BBBB

1053 invoke-virtual  

006d  取MethodiD  requestWindowFeature     (I)Z

0001  参数

iget-object p0, p0,Lcom/wangzhong/fortune/ui/activity/BaseActivity;->a:Lcom/wangzhong/fortune/ui/activity/BaseActivity;

--------------------------------------------------------------------------------------------------------------------------------





next  脚本执行结果如下

