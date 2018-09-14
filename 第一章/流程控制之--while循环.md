流程控制之--while循环
======

##### 基本循环

```python
while 条件:
    # 循环体
    # 如果条件为真，那么循环体则执行
    # 如果条件为假，那么循环体不执行
```

##### 循环中止语句 

如果在循环的过程中，因为某些原因，你不想继续循环了，怎么把它中止掉呢？这就用到break 或 continue 语句

break用于完全结束一个循环，跳出循环体执行循环后面的语句

continue和break有点类似，区别在于continue只是终止本次循环，接着还执行后面的循环，break则完全终止循环

###### 例子:break

```python
count = 0
while count <= 100 : #只要count<=100就不断执行下面的代码
    print("loop ", count)
    if count == 5:
        break
    count +=1 #每执行一次，就把count+1，要不然就变成死循环啦，因为count一直是0

print("-----out of while loop ------")
```

输出:

```python
loop  0
loop  1
loop  2
loop  3
loop  4
loop  5
-----out of while loop ------
```

###### 例子：continue

```python
count = 0
while count <= 100 : 
    count += 1
    if count > 5 and count < 95: #只要count在6-94之间，就不走下面的print语句，直接进入下一次loop
        continue 
    print("loop ", count)

print("-----out of while loop ------")
```

输出:

```python
loop  1
loop  2
loop  3
loop  4
loop  5
loop  95
loop  96
loop  97
loop  98
loop  99
loop  100
loop  101
-----out of while loop ------
```

##### while ... else ..

与其它语言else 一般只与if 搭配不同，在Python 中还有个while ...else 语句

while 后面的else 作用是指，当while 循环正常执行完，中间没有被break 中止的话，就会执行else后面的语句

```python
count = 0
while count <= 5 :
    count += 1
    print("Loop",count)

else:
    print("循环正常执行完啦")
print("-----out of while loop ------")
```

输出:

```python
Loop 1
Loop 2
Loop 3
Loop 4
Loop 5
Loop 6
循环正常执行完啦
-----out of while loop ------
```

如果执行过程中被break啦，就不会执行else的语句啦

```python
count = 0
while count <= 5 :
    count += 1
    if count == 3:break
    print("Loop",count)

else:
    print("循环正常执行完啦")
print("-----out of while loop ------")
```

输出:

```python
Loop 1
Loop 2
-----out of while loop ------
```


