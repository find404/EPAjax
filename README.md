# SelfAjax

自用的项目中封装的jq的ajax方法

self :: function 

在项目中频繁的$.post和$.get繁琐无比，在这里直接封装成了一个方法，每个网站下面都可以引用。

规范起来每个到后台的接口，让所有的发起ajax都只用这一个方法。


![image](https://github.com/find404/SelfAjax/blob/master/images/remd.png)
 
                               事件发起（Start）
                                    |
                                    |
                                    |
    验证基本数据 (Verification)      |
                            \				   |
                              \			  |
                                \		 |
                                  \	|
                                    \       
                                    |     不同业务逻辑间应对的不同的业务方法（Demand）
                                    |				/
                                    |			/
                                    |		/
                                    |	/
                                    /
                                    |
                  ajax Start        |
                            \				   |
                              \			  |
                                \		 |	
                                  \	|
                                    \

 

eg :

SelfAjax('post','/Admin/Infor/find404',FromData,'get_ordinary');
