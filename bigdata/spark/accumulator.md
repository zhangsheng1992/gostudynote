> 驱动程序中定义的变量,在进行转化操作时,工作节点得到的只是该变量的一份副本,
> 对副本的修改无法影响到原始值,这在某些情况下十分不便.
> 因此,spark提供了两个共享变量累加器与广播变量,可以在所有工作节点进行共享

## 案例
有一个文件内容如下
```python
field1 field2
a       1
b       2
c       1
d       2
```


我们需要对数据进行**map()**转化,统计其中**filed2**字段值为2的项的数量  