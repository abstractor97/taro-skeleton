# Skeleton 骨架屏
基于 taro 到一个简单易用到骨架屏组件

### 支持多端平台使用 
1. 微信小程序
2. h5
3. 其它平台未测试

### 引入

``` javascript
import Skeleton from 'taro-skeleton'
```

## 代码演示

### 基础用法

通过`title`属性显示标题占位图，通过`row`属性配置占位段落行数

``` jsx
<Skeleton title row={3} />
```

### 显示头像

通过`avatar`属性显示头像占位图

``` jsx
<Skeleton title avatar row={3} />
```

### 展示子组件

将`loading`属性设置成`false`表示内容加载完成，此时会隐藏占位图，并显示`Skeleton`的子组件

``` jsx
<Skeleton
  title
  avatar
  row={3}
  loading={loading}
>
  <Text>实际内容</Text>
</Skeleton>
```

```jsx
export default class Index extends Component {
  state = {
    loading: false
  }
  render () {
    return (
      <View className='index'>
        <Skeleton loading={this.state.loading} title avatar row={2} action></Skeleton>
      </View>
    )
  }
}
```

## API

### Props

| 参数 | 说明 | 类型 | 默认值 | 版本 |
|------|------|------|------|------|
| row | 段落占位图行数 | `number` | `0` | - |
| row-width | 段落占位图宽度，可传数组来设置每一行的宽度 | `number | string | number[] | string[]` | `100%` | - |
| title | 是否显示标题占位图 | `boolean` | `false` | - |
| title-width | 标题占位图宽度 | `number | string` | `40%` | - |
| avatar | 是否显示头像占位图 | `boolean` | `false` | - |
| avatar-size | 头像占位图大小 | `number | string` | `90px` | - |
| avatar-shape | 头像占位图形状，可选值为`square` | `string` | `round` | - |
| action | 显示右边操作按钮占位图 | `boolean` | `false` | - |
| loading | 是否显示占位图，传`false`时会展示子组件内容 | `boolean` | `true` | - 
| animate | 是否开启动画 | `boolean` | `true` | - |
