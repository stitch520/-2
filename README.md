#对字符串求长度
s="hello world!"
print(len(s))

#通过索引获取单个字符
print(s[0])
print(s[11])
print(s[len(s)-1])
#布尔类型
b1=True
b2=False

#空值类型
n=None

#type函数
print(type(s))
print(type(b1))
print(type(n))

#将一些朋友的姓名存储到一个列表中
names=["小于","小陈","小曾"]
print(names[0])
print(names[1])
print(names[2])
#给每个朋友打印一条消息
greeting="你好呀！"
print(greeting + names[0])
print(greeting + names[1])
print(greeting + names[2])

print( names[0] +greeting)
print( names[1] +greeting)
print( names[2] +greeting)
#嘉宾名单
names=["小于","小陈","小曾"]
invite="一起吃个饭吧？"
print(invite + names[0])
print( invite+ names[1])
print(invite + names[2])
#修改嘉宾名单
names=["小于","小陈","小曾"]
invite="一起吃个饭吧？"
print(names[2]+"不能赴约")
names[2]="小田"
print(invite + names[0])
print( invite+ names[1])
print(invite + names[2])
#添加嘉宾
#使用insert()将一位新的嘉宾添加到列表开头
#使用insert()将一位新的嘉宾添加到列表中间
#使用append()将一位新的嘉宾添加到列表末尾
print("找到一个更大的餐桌")
names.insert(0,"小林")
names.insert(2,"小张")
names.append("小邓")
print(invite + names[0])
print(invite + names[1])
print(invite + names[2])
print(invite + names[3])
print(invite + names[4])
print(invite + names[5])
#比萨，存储到列表中，在用for循环，将比萨打印出来
pizza_list=["香肠披萨","芝士比萨","榴莲比萨"]
for pizza in pizza_list:
    print("我喜欢"+pizza)
print("我真的很喜欢披萨！")

#1加到100的和
total = 0
for i in range(1,101):
    total = total+i
print(total)
#一百万
numbers=[]
for num in range(1,1000001):
    numbers.append(num)
#for num in numbers:
#    print(num)
#
print(min(numbers))
print(max(numbers))
#使用sum计算1到1000000的和
print(sum(numbers))
#mood_index是0到100之间的整数
#is_at_home 是布尔值
# if mood_index < 60:
#     if is_at_home:
#         print("放弃游戏，低调做人")
#
#     else:
#         print("自由")
# if mood_index < 60:
#     if is_at_home:
#         print("情绪低落且在家，建议放弃游戏，低调做人")
#     else:
#         print("情绪低落但不在家，可以选择自由活动")
# else:
#     print("情绪良好，可以尽情享受生活")
#外星人的颜色
# alien_color="green"
# if alien_color=="green":
#     print("You got 5 points!")
#外星人的颜色2
# alien_color="green"
# if alien_color=="green":
#     print("You got 5 points!")
# else:
#     print("You got 10 pints!")
# alien_color="green"
# if alien_color=="yellow":
#     print("You got 5 points!")
# else:
#     print("You got 10 pints!")
#外形人3
# # alien_color="red"
# # if alien_color=="yellow":
# #     print("You got 5 points!")
# # elif alien_color=="red":
# #     print("You got 10 points!")
# # else:
# #     print("You got 15 pints!")
# # #人使用字典 姓名
# # friend={"first_name":"小尹","last_name":"陈","age":25,"city":"深圳"}
# # print("姓名:"+friend["last_name"]+friend["first_name"])
# # print("年龄:"+str(friend["age"]))
# # print("城市:"+friend["city"])
# # #河流 创建一个字典,在里面存储三条河流及其流经的国家
# # rivers={"Nile":"Egypt","Yangtze River":"China","Amazon River":"Brazil"}
# # for river,country in rivers.items():
# #     print("The"+river +"run through"+country)
# # for river, country in rivers.items():
# #     print(river)
# # for river in rivers.keys():
# #     print(river)
# # for country in rivers.values():
# #     print(country)
# #
# # #10的倍数
# # # number=int(input("请输入一个数字："))
# # # if number % 10==0:
# # #     print("您输入的数字是10的倍数")
# # # #比萨配料
# # # user_input=input("请输入您想要添加的比萨配料:")
# # # while user_input!="quit":
# # #     print("好的，比萨里会为您添加"+ user_input)
# # #     user_input = input("请输入您想要添加的比萨配料:")
# # #喜欢的图书
# def favorite_book(title):
#     print(f"One of my favorite books is {title}.")
# favorite_book("三体")
# #城市名
# def city_country(city,country):
#     return f"{city}, {country}"
# print(city_country("深圳","中国"))
# print(city_country("多伦多","加拿大"))
# print(city_country("旧金山","美国"))
# 定义大矩阵
matrix = [
    [9719, 7515, 5916, 6467, 7157, 9614, 8560, 9075, 2099, 2838, 1403, 7652, 6238, 1699, 8907, 1804, 5384, 7942, 7546, 1978],
    # 在这里添加其余的行
    # ...
]

# 定义子矩阵大小
submatrix_size = 5

max_sum = float('-inf')  # 初始化最大和为负无穷

# 遍历大矩阵中所有可能的子矩阵
for i in range(len(matrix) - submatrix_size + 1):
    for j in range(len(matrix[0]) - submatrix_size + 1):
        current_sum = 0
        # 计算当前子矩阵的和
        for x in range(i, i + submatrix_size):
            for y in range(j, j + submatrix_size):
                current_sum += matrix[x][y]
        # 更新最大和
        max_sum = max(max_sum, current_sum)

print("5行5列子矩阵的和的最大值是:", max_sum)


def min_steps_to_top(n):
    if n == 0:
        return 0
    if n == 1:
        return 1
    if n == 2:
        return 1
    if n == 3:
        return 1

    dp = [0] * (n + 1)
    dp[1] = 1
    dp[2] = 1
    dp[3] = 1

    for i in range(4, n + 1):
        dp[i] = min(dp[i-1], dp[i-2], dp[i-3]) + 1

    return dp[n]

# 读取输入
n = int(input())
# 调用函数计算最少步数
result = min_steps_to_top(n)
# 输出结果
print(result)


def count_steps(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    elif n == 2:
        return 2
    elif n == 3:
        return 3

    dp = [0] * (n + 1)
    dp[1] = 1
    dp[2] = 2
    dp[3] = 3

    for i in range(4, n + 1):
        dp[i] = dp[i - 1] + dp[i - 2] + dp[i - 3]

    return dp[n]


n = 10  # 台阶总级数
steps = count_steps(n)
print(f"小蓝上{n}级台阶至少需要{steps}步")

