# 移动端布局常见问题
1. 横竖屏限制问题  
    
        <meta name="x5-orientation" content="portrait | landscape" />  只支持x5内核
        <meta name="screen-orientation" content="portrait">   只支持uc浏览器
         
2. 全屏限制问题  
   
        <meta name="x5-fullscreen" content="true" />   只支持x5内核
        <meta name="full-screen" content="yes">   只支持uc浏览器
        
3. 禁止识别电话号码和邮箱

        <meta name="format-detection" content="telephone=no, email=no" />
  
    **禁止识别后页面当中所有的邮箱和电话将不会识别,如果有特殊需求,要配合一下代码实现**
     
        <a href="tel:110">请拨打电话110</a>
        <a href="qq@.com">请发送邮件qq@.com</a>        
        
4. 消除链接\表单\按钮 默认背景

        -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
5. 消除按钮圆角

        -webkit-appearance: none;

6. 移动端字体
* ios系统  
    * 默认中文字体是Heiti SC   
    * 默认英文字体是Helvetica   
    * 默认数字字体是HelveticaNeue   
    * 无微软雅黑字体   
* android 系统
    * 默认中文字体是Droidsansfallback  
    * 默认英文和数字字体是Droid Sans  
    * 无微软雅黑字体  
* winphone 系统
    * 默认中文字体是Dengxian(方正等线体)  
    * 默认英文和数字字体是Segoe  
    * 无微软雅黑字体   
    
**结论**
* 各个手机系统有自己的默认字体，且都不支持微软雅黑
* 如无特殊需求，手机端无需定义中文字体，使用系统默认
* 英文字体和数字字体可使用 Helvetica ，三种系统都支持
           
        body{font-family:Helvetica;}
                      
7. 禁止用户设置字体大小

        -webkit-text-size-adjust:100%  

8. 禁止文字选中

        -webkit-user-select:none  //安卓不支持
                
9. font boosting 
   **移动端设备为了使用户能看清楚大批量的字体,会自动对字体进行放大,但是只要指定了容器的高度,就能解决**

        p{max-height:9999999px}      
                  
10. 固定定位问题 
                  
11.                   