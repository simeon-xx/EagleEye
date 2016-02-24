# 使用cProfile和line_profiler分析代码

## 前置条件
安装line_profiler:`pip install line_profiler`

## 使用
在tests/utils中写了两个装饰器

1. do_func_profile：使用cProfile分析调用方法执行时间
2. do_line_profile：使用line_profiler分析每行代码执行时间

PS:再python文件中加入`from tests.utils import do_func_profile, do_line_profile`

### do_func_profile示例：
`@do_func_profile
def get_editor_moments(self, value):`


### do_line_profile示例：
`@do_line_profile(follow=[func_name])
def get_editor_moments(self, value):`