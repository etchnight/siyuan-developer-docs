---
outline: deep
---

# 类型转换函数

Sprig 提供了以下类型转换函数：

- `atoi`：将字符串转换为整数。
- `float64`：转换为 `float64` 类型。
- `int`：按系统的宽度将值转换为 `int` 类型。
- `int64`：转换为 `int64` 类型。
- `toDecimal`：将 unix 八进制转换为 `int64` 类型。
- `toString`：转换为字符串。
- `toStrings`：将列表、切片或数组转换为字符串列表。

只有 `atoi` 需要输入是特定类型的。其他函数会尝试将任何类型的值转换为目标类型。例如，`int64` 可以将浮点数转换为整数，也可以将字符串转换为整数。

## `toStrings`

给定一个类似列表的集合，生成一个字符串切片。

```
list 1 2 3 | toStrings
```

以上将 `1` 转换为 `"1"`，`2` 转换为 `"2"`，依此类推，然后将它们作为列表返回。

## `toDecimal`

给定一个 unix 八进制权限标志字符串，生成一个十进制数。

```
"0777" | toDecimal
```

以上将 `0777` 转换为 `511`，并将该值作为 `int64` 返回。
