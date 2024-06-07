## TNT
TNT: Take is Not Transfer

### Data Unit
##### 优化方案
+ 如果手机相机能识别的二维码，所能装的数据量小，可考虑把字段名减小一些

``` ts
interface TNT {
  meta: {
    protocal: 'tnt'
    version: '0.0.1'
  }
  integraty: {
    hash: string
    unit_hash: string
    index: number // 文件（或数据）量大时，一个二维码可能不够用的
    length: number // 二维码总数
  }
  use: {
    type: 'clipboard' | 'save_as_file'
  }
  data: unknown
}
```

### 小段子
1. 一辆装满硬盘的卡车，在高速路上行驶，求数据传输带宽
2. 二维码是一种存储数据的格式，相机像素足够高时，拍照的带宽也会相当高
