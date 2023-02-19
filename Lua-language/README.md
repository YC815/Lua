Lua memo
===
### 教材
- https://ithelp.ithome.com.tw/articles/10246245
## print
```lua
print("<text>")
```

## function
```lua
function <FunctionName>(<parameters>) -- parameters: 參數
    ...
end

-- 呼喚
FunctionName(<argument>) -- argument 引數
```

## 有不固定參數的function
```lua
function <FunctionName>(...)
    local <CustonName> = {...} -- 可以給不定長參數(...)一個名字
    ...
end
```
## 變數
```lua
-- 全局變數
x = 1

-- 局部變數
local x = 1
```

## 資料型態
```lua
-- 字串轉數字
tonumber("1.0")

-- 數字轉字串
tostring(1.0)
```

## 導入模組
```lua
local <cutsom name> = require "<mod>"

-- 導入數學模組
local math = require "math"
```

## 字串長度
```lua
-- Chinese
-- True
print(utf8.len("我")) => 1

-- False
print(string.len("我")) =>3

-- English
print(#"hello")
```

## 字串儲存
```lua
-- 單行字串
x = "Hello, world!"

-- 多行字串
x = [[
    Hello
    world!
]]
```

## 字串連接
```lua
print("hello" .. "world")
```

## Boolean and nil
- Boolean
  > true<br>
  > false
- nil
   > nil

- 真值的定義: 除了false和nil以外的所有值(包含: 0, {}, "")
- 假值的定義: false和nil

## 邏輯運算
x 等於 y
```python
# Python
if x == y:
    print("Hi")
```
```lua
# Lua
if x == y then
    print("Hi")
end
```
x 不等於 y
```python
# Python
if x != y:
    print("Hi")
```
```lua
# Lua
if x ~= y then
    print("Hi")
end
```

## 註解
```lua
-- 單行註解
--[[
    多行
    註釋
]]
```

## if and else
```lua
-- elseif √
if <條件> then
    print("block I")
elseif <條件> then
    print("block II")
else
    print("block III")
end

-- else if
if <條件> then
    print("block I")
else if <條件> then
    print("block II")
else
    print("block III")
end
end
```

## switch
```lua
a = {
    user = function () print "run user code" end,
    server = function () print "run server code" end,
}

run = "user"
a[run]() -- run user code

run = "server"
a[run]() -- run server code
```

## for
```lua
-- print 1..10
for i = 1, 10 ,1 do
    print(i)
end

-- print 10 .. 1
for i = 10, 1, -1 do
    print(i)
end
```

## while
先判斷再執行。未達成條件就無限執行
```lua
while <條件> do
    ...
end
```

## repeat and until
先執行再判斷。未達成條件就無限執行
```lua
repeat
    ...
until <條件>
```

