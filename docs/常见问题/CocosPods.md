---
sort: 14
---

# CocosPods

1. pod install失败了?
> 请先【重置】恢复到原始工程，然后pod install --no-repo-update 就能解决问题（之所以失败，就是因为pod生成的工程文件有某些校验机制）。
>

2. 我需不需要 pod install？
> 使用了CocosPod的项目，请在混淆工程先，执行一下这个命令，确保工程能正常编译过，并且保证Pods创建的工程没问题。
>

3. pod install 提示 [Xcodeproj] Unable to find compatibility version string for object version `70`. 错误?
>
```
步骤1.点[重制]按钮
步骤2.找到出错的xcodeproj文件，比如说 Runner.xcodeproj 右键菜单选择[显示包内容]
步骤3.文本编辑器打开 project.pbxproj  把 objectVersion = 70; 改成 objectVersion = 54;
步骤4.再点[开始混淆]就解决了
```