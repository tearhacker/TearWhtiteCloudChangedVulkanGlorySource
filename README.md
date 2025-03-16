# 降价状态 源码完整联系泪心钉钉或者泪心电报作者@tearcryingm 或者泪心QQ

# 加: 无后台辅助运行原理
   - 如果手机使用的kernelsu或者Apatch 那么全局都拥有无后台的效果！ 就是可以随便关闭MT管理器！ 加入无后台代码反而导致卡- 死！
   - 如果手机是magisk面具，那么不存在无后台运行辅助功能！mt管理器必须锁定APP，除非加入无后台执行代码！  缺点就是每次必须编译两个文件！

## 源码特点

1. **Dear ImGui, v1.91.5 WIP VULKAN渲染绘制**  
   - 零针延迟，秒响应。
   - 泪心独立无后台绘制源码写法，适配Magisk面具无后台执行辅助！

2. **安卓分辨率锁定**  
   - 使用最新函数库锁定获取安卓手机分辨率，支持安卓15手机系列。  
   - `::displayInfo = android::ANativeWindowCreator::GetDisplayInfo();`

3. **安卓15触摸支持**  
   - 采用国外最新native层安卓15触摸支持依赖头文件，解决安卓15手机卡死无法触摸问题。

4. **RT最新驱动系列支持**  
   - 支持安卓15驱动内核6.6版本号。

5. **泪心自研魔改解析静态库源**  
   - 享有完美验证百度代理心跳代理联网修改映射down的权限。  
   - 额外教学端游服务器封包，另外收费！

9. **泪心解析 支持游戏中闪退后再次执行解析绘制**
   - 解决游戏中二次开解析导致的三方问题
   - 解决游戏中开解析绘制导致的各类问题
   - 代码异次元判断 额外收费 不免费服务

7. **泪心自写驱动魔改对接支持kernel文件**  
   - 支持QX全部系列、GT全部系列，附带支持RT全系列驱动。  
   - 自动识别驱动，玩家刷入什么内核，就识别到什么内核！  
   - 未刷入驱动将无法打开辅助，提示请刷入驱动！

8. **泪心完整源码可读性**  
   - 分模块和文件夹详细清点各分类函数作用和注释，不会出现代码大杂乱的情况。  
   - 整体架构：  
     - `Include->SuLib` 控制整体引入导入静态库文件。  
     - `Src->Android_draw` 文件夹控制绘制菜单设计、绘制内容读取、绘制头文件变量定义等完整模块代码。  
   - **注意点一**：泪心游戏变量和游戏结构体分开定义，防止代码凌乱看得人模糊不清。  
   - **注意点二**：泪心王者荣耀图片载入是特殊化个人写的，需要150元技术费用。因为此方案目前无开源，基本都不会载入分析图片转二进制数据。能看懂和分析C++代码的人很少，都是靠买，即使买了源码也不懂。  
   - **注意点三**：切片化保留了原名人名言的语句显示和刷新，分离了函数和实际UI层面的调用代码，方便理解代码。

9. **源码来源**  
   - 本源码由白云老掉牙的`native_surface`安卓8~13开源而来，泪心套入VULKAN渲染imgui新版，自定义魔改了全新UI外观菜单，并载入了王者荣耀个性化绘图源码hpp文件。

10. **优点**  
   - 可以开启绘制状态，点击防录屏，自动切换为过直播模式，也可以再次点击防录屏，取消过直播模式。  
   - 截图功能和录制功能按钮都是强制安卓14以上截图和录屏！在此之下的手机均可以在非防录屏情况下正常使用手机截图快捷键。

## 额外定制点

- **适配全机型分辨率一键调整并自动保存该手机配置参数文件夹问题**  
  - 这些分辨率的适配需求理应额外进行100元技术收费，采用了分离函数保存和实时点击替换绘制配置效果显示。  
  - 任何玩家选择好自己的分辨率后，小地图都是即时生效并且保留配置文件在当前手机目录下。  
  - 关于配置文件导致外挂180的谣言：触摸驱动拉闸，QX驱动拉闸跟文件有什么关系？跟文件有关系那你思考下为什么端口作者永远说环境问题！  
  - 不说环境问题端口怎么圈钱啊，对不对？逃避责任是常态！说穿了同行之间都不舒服！大家都是端口作者，这怎么玩呢？对不对！

```cpp
if (ImGui::Selectable("3200x1440")) currentChoice = 1;
if (ImGui::Selectable("2712x1220")) currentChoice = 2;
if (ImGui::Selectable("2400x1080")) currentChoice = 3;
if (ImGui::Selectable("2560x1600")) currentChoice = 4;
if (ImGui::Selectable("3192x1368")) currentChoice = 5;
if (ImGui::Selectable("2340x1080")) currentChoice = 6;
if (ImGui::Selectable("2800x1800")) currentChoice = 7;
if (ImGui::Selectable("2460x1080")) currentChoice = 8;
if (ImGui::Selectable("小米14专属")) currentChoice = 9;
if (ImGui::Selectable("3168x1440")) currentChoice = 10;
if (ImGui::Selectable("2800x1968")) currentChoice = 11;
```

主体适配分辨率十几个函数单独包装到了保存绘制参数的头文件中，不会再UI设计菜单文件造成代码紊乱的视觉效果。

<span style="color: green;">非常轻松看懂代码，好的代码整洁性请放心，泪心亲自写了很多注释和删除了不相干代码！</span>

解析内置端口绘制问题
验证百度后可以根据"<和h和1和>"标题内容进行百度验证，如若标题1内容和本地文件字符串变量不匹配，就直接结束！

修改CCproxy账号密码即可直接远程关闭一切解析绘制版本！

加密编译后即可隐藏一切特征，无需害怕服务器被攻击！

解析优点：<span style="color: green;">无视一切破解，也无视一切流量攻击。泪心解析源码并带有百度验证网页。</span>

端口APP任你如何加密加固，服务器ip地址还是随便破解，随便攻击ddos服务器。

关于行为180问题
任何说端口修改down、处理心跳联网可以过行为180的，就是为了圈钱！

端口过行为，痴人说梦！内存杀67过行为，没错是这么个理！端口诈骗犯！宣传犯！

端口作者都是拿着最脏的钱，干着最没人性最冷血的活，说的全是假的，没一句实话！

现在主打一个不说的天花乱坠无人消费！怎么可能没钱呢！人性很贪婪，会掩盖技术的落后！

端口都是拿着本不该存在的好处硬瞎叫，端口作者为什么叫小学生？因为没能力只有一张嘴！

任何一个端口作者，他说他有能力，怎么证明？看一看端口作者开发的易语言TCP网络编程工具？

看一看端口作者独立开发的流量处理框架！看一看端口作者独立自动化处理的封包AI成品！

拿不出实际项目的端口作者，光靠一张嘴，一个APP成品软件，一个百度验证，几张图片！

任你天花乱坠！你只需要知道一点，百分百诈骗！绝对是假的！

任你天花乱坠！你只需要知道一点，百分百诈骗！绝对是假的！

任你天花乱坠！你只需要知道一点，百分百诈骗！绝对是假的！

任你天花乱坠！你只需要知道一点，百分百诈骗！绝对是假的！

端口作者不可能有能力的，有能力的端口作者早就内防端口动态调试检测防封，而不是单端口！

对抗端口最直接的方式
火速成为端口作者，B站自学端口封包，成为端口，就不再被端口作者用一个APP软件百度验证欺诈欺骗致死。
