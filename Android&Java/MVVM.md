#Data binding(MVVM，Model-View-ViewModel)

##组成部分
+  Model：数据，业务逻辑
+  View：显示，UI
+  ViewModel：绑定前两者  

##工作流程
传统MVC模式中，controller把model推到view中，而在MVVM中，ViewModel改变Model的内容后，framework将负责把变化更新到View中；Model和View通过ViewModel的接口若耦合；  
得益于此，MVVM的测试不依赖于View的存在，只需注入相应依赖即可；测试model时，检查ViewModel的对应方法是否被调用；测试View时，使用mock Model，检查View内容的显示正确性；