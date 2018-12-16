# state vs props

## 前言

state 和 props 作为 React 内两项重要的概念，总是让一些初学者难以分辨二者的使用场景。

在这里我们先给出一个结论：尽量少用 state，更多的使用 props。

## 相同

1. 二者都作为 React 内更新视图的依据，只有它们变化时，React 才会进行相应的更新。
2. 二者都不可以通过直接赋值的方式更新。
3. 二者都可以使用任意类型的值。
4. 二者都可以设置默认值。

## 不同

1. 更新方式不同：state 通过 `setState` 方法更新（只能在组件内部更新），props 则通过更新传入的值实现（组件内不可变）。
2. state 只维护组件内部的状态，props 让外部维护组件的状态。

## 总结

通过比较二者异同，我们可以说使用 state 的组件“不纯”，因为它内部维护自己的一套状态，导致我们维护的成本加大。

React 鼓励使用函数式组件，部分原因是函数式组件更像是纯的视图组件。我们也推荐多使用函数式组件，这样既能提高组件的可复用性，又能降低维护成本