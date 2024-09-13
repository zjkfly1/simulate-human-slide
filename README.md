# simulate-human-slide
模拟人的滑动验证码的滑动行为

# 0.背景
在破解滑动验证码时，即使获取到待滑动的距离，但是当使用无头浏览器组件滑动时很容易被机器识别出来。
因此，需要进行模拟人的操作来进行代码指令滑动。

# 1.示例
具体图片如下

<img alt="img.png" height="300" src="img.png" width="400"/>

# 2.使用示例

// 输入滑动距离

    tracks = get_simulate_track(123)


// tracks 为三元组列表，第一个元素是横坐标移动距离，第二个元素是纵坐标移动，第三个元素是停留时间，单位为毫秒

    for track in tracks:
        print(f"横坐标位移:{track[0]}  纵坐标位移:{track[1]} 暂停时间/毫秒:{track[2]}")
