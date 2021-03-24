# 车道线误识别威胁
许多车的辅助驾驶功能里都会有车道线居中的功能。该功能的主要部分是车道线识别。从安全评估角度触发，如何量化车道线识别出现偏差后所造成的安全隐患，目前没有标准的方法。我们在这里对这一安全问题稍作展开讨论。

# 车道线误识别示例
![Image of Lane Detection Error ](https://octodex.github.com/images/yaktocat.png)

如图所示：通常情况下，高速道路的车道宽度大致是3.65米（北美高速）。而小型车（本田雅阁）的宽度是1.8米。蓝色实线代表原始车道线位置，紫色虚线则代表车道线模型给出的识别。如果按照模型的预测结果，
自动（辅助）驾驶中的车道线居中功能会引导小型车逐渐偏离现有的驾驶车道。当小型车行驶到当前车道边缘时，甚至于在非换道情况下超出当前车道行驶到临近车道时，我们把这类的情况归类为非安全驾驶行为。以图中为例，
当行驶到威胁点的时候，小型车的水平位移d是0.925米。如果当前车速为每小时50公里，且在垂直50米的距离完成这一变线的话，则只需要3.6秒的时间。如果需要在更短的垂直距离(10米)完成这一变线的话，所需的时间则只需0.72秒。
所以该车道线误识别到行车进入危险区域的时间是瞬间完成的，很容易造成与临近车辆的擦碰或撞击。
