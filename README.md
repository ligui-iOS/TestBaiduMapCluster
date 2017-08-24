**1.整体结构**
类名 | 描述
---|---
BMKClusterAlgorithm | 点聚合算法类
BMKClusterItem | 标注
BMKClusterManager | 点聚合管理
BMKClusterQuadtree | 经纬度坐标转换为地图点坐标以及判定点是否在区域内
***
#### 主流程图
```
graph TD
A[mapdidload OR 重绘地图] --> B[更新聚合状态]
B --> C[绘制聚合后的标注]
```
#### 聚合流程图
```
graph TD
A[获取地图比例尺级别]
A-->  B(根据比例尺级别标注坐标以及距离计算块大小)
B--> C(将标注划入快中)
C--> D(形成聚合标注)
```


