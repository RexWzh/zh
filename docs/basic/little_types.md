# 小类型
## 无
`Nothing`，具有唯一值`nothing`，用于对应`C`中的`void`\
`nothing`不会被REPL特别显示
```jl
julia> "a";nothing

julia>
```

## 未定义
`UndefInitializer`，通常用于数组初始化，开源用`undef`替代`UndefInitializer()`

## 元组
`Tuple`一个容纳任意有限多个数据的类型\
```jl
julia> tup=(1,2,3)
(1, 2, 3)

julia> typeof(tup) # 这表明tup的3个参数类型均为Int64
Tuple{Int64, Int64, Int64}

julia> Tuple{Vararg{Int64,3}} # 一种仅对Tuple有效的简写方式
Tuple{Int64, Int64, Int64}

julia> tup[1] # 获取第一个数据
1
```