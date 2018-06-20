- 一个python的dict，按照key-value存储，如何按照value排序
```python
from collections import OrderedDict
OrderedDict(sorted(before.items(), key=lambda x: x[1]))
```

- static的类有什么用
> @staticmethod不需要表示自身对象的self和自身类的cls参数，就跟使用函数一样，这有利于组织代码，把某些应该属于某个类的函数给放到那个类里去，同时有利于命名空间的整洁

- 如何实现一个只能实例化一次的类
```python
# 单例
class singleton:
    def __init__(self, cls):
        self.cls = cls
        self.instance = None

    def __call__(self, *args, **kwargs):
        if self.instance is None:
            self.instance = self.cls(*args, **kwargs)
        return self.instance

# 包/模块
```
