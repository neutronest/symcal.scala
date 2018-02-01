# Inception

Symcal.scala 是一个简易的符号计算库。期望支持符号定义，延迟求值，可反向求导，可观察其中变量的数学表达式，可接入 Python, Lisp, OpenCL 等各种后端。

对其定位是一个实验性质的 Demo， 而不是生产环境中可用的 industry production library。我们希望籍此加强对符号计算，Scala 高级特性，反向传播等 field 的理解。



## Example

我们希望她看上去是这个样子的：

```
x = context.FloatCube("x")
y = context.FloatCube("y")
z = x + y

xs = context.SeqCube[FLoatCube]("xs")
xss = xs ++ z
context.set_output(xss)

## compile 
res = context.compile()
println(res)

## compile to other backend
python_res = context.compile_to_python()

#### Using python to evaluate value
eval(python_res)

#### other backend





```

## Q1

一期应该