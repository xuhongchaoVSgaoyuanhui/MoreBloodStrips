# MoreBloodStrips---（它还是个测试版--It's still in beta.）
This plugin makes it quick and easy to build UI blood bars, and it allows users to use custom UserWidget.

中文：这个插件能快速，方便得构建UI血条，并且它可以让用户自定义UserWidget控件蓝图。




How to construct one's own UserWidget?
How many steps are needed?
1. Create your own UserWidget and add a canvas panel, making it "variable". In the "Role", you need to declare some variables, such as HP and Equal In Value (not necessarily mandatory, but for subsequent expansion).
2. Call the FU_CompatibleWithc_Custom_Class function and cast the returned object to your own UserWidget object.
3. Call the FU_CustAddChildWidget_to_ParentWidget function and make your preferred settings for it, override the default values, and promote the returned bp_Implementation_Object object reference to a variable for convenient subsequent operations.
   
---After completing the above steps, you can already obtain the UI health bar defined by yourself. The following is the interaction of the health bar. ---

1. Call the FU_SetDamage function. It requires a reference to the bp_Implementation_Object object, which is why it was promoted to a variable in the third step.
2. Set the returned value to the HP you created. Success.

   
中文：如何构建自己的UserWidget？

需要多少步骤？

1.新建你自己的UserWidget，并添加一个画布面板，把它“变量化”。在“角色”中，你需要声明一些变量，比如HP和Equal In Value（不一定强制性，只是方面后续扩展）

2.调用FU_CompatibleWithc_Custom_Class函数，并将返回对象cast to你自己的UserWidget对象。

3.调用FU_CustAddChildWidget_to_ParentWidget函数，并对其进行你喜欢的设置，重载默认值，并且把返回的bp_Implementation_Object对象引用提升为变量，以方便后续操作。

-------完成以上步骤，你已经可以获得自己定义的UI血条了，以下是血条交互。-------


1.调用FU_SetDamage函数。它需要bp_Implementation_Object对象引用，这就是为什么第三步要提升为变量。

2.将返回值设置给你创建的HP。大功告成。
