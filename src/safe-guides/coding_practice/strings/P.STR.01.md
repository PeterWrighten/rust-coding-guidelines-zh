## P.STR.01   处理字符串元素时优先按字节处理而非字符

**【描述】**

处理字符串有两种方式，一种是按字符处理，即把字符串转为字符数组`[char]`，另一种是直接按字节处理`[u8]`。

两者之间的一些区别：

- `[char]`  保证是有效的 Unicode，但不一定是有效的 UTF-8，一般将其看作是 UTF-32 。将字符数组转换为字符串需要注意。
- `[u8]` 不一定是有效的字符串，它比 `[char]` 节省内存。将其转换为字符串需要检查 `UTF-8`编码。

