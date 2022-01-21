# china_regions
中国行政区划数据最新版，适用于地址选择器。

## 数据格式

### provinces.json

从国家统计局爬取的2021最新版数据。

http://www.stats.gov.cn/tjsj/tjbz/tjyqhdmhcxhfdm/2021/index.html

```json
{
  "code": "行政区划12位数字代码",
  "name": "名称全称",
  "parent": "父级行政区划的代码, 省级为null",
  "children": [{"code": ..., "name": ..., "parent": ..., "children": ...}],
}
```

### provinces-slim.json

从国家统计局爬取的2021最新版数据。
不包含 `"parent"` 和 `"code"` 字段，只有50K，可以在前端使用。

```json
{
  "code": "行政区划12位数字代码",
  "name": "名称全称",
  "children": [{"code": ..., "name": ..., "parent": ..., "children": ...}],
}
```
