### 相关问题

说是面试题，并不是为了读者去利用这个去参加面试，只是为了一些图像算法相关问题的深入理解，这里面的一些问题，除了参考网上的解答，也包含了
部分我们自己的理解，不当之处欢迎指出。


##### 1.CNN的特点以及优势

   改变全连接为局部连接，这是由于图片的特殊性造成的（图像的一部分的统计特性与其他部分是一样的），通过局部连接和参数共享大范围的减少参数值。可以通过使用多个filter来提取图片的不同特征（多卷积核）。 
    
   CNN使用范围是具有局部空间相关性的数据，比如图像，自然语言，语音

    1.局部连接：可以提取局部特征。
    2.权值共享：减少参数数量，因此降低训练难度（空间、时间消耗都少了）。 
    3.可以完全共享，也可以局部共享（比如对人脸，眼睛鼻子嘴由于位置和样式相对固定，可以用和脸部不一样的卷积核）
    4.降维：通过池化或卷积stride实现。
    5.多层次结构：将低层次的局部特征组合成为较高层次的特征。不同层级的特征可以对应不同任务。
    
    
##### 2.deconv的作用

##### 3.dropout作用以及实现机制

##### 4.深度学习中有什么加快收敛/降低训练难度的方法： 

    1.瓶颈结构
    2.残差
    3.学习率、步长、动量
    4.优化方法
    5.预训练
    
##### 5.什么造成过拟合，如何防止过拟合

    1.data agumentation
    2.early stop
    3.参数规则化
    4.用更简单模型
    5.dropout
    6.加噪声
    7.预训练网络freeze某几层
    
##### 6.LSTM防止梯度弥散和爆炸 

   LSTM用加和的方式取代了乘积，使得很难出现梯度弥散。但是相应的更大的几率会出现梯度爆炸，但是可以通过给梯度加门限解决这一问题
   
##### 7.为什么很多做人脸的Paper会最后加入一个Local Connected Conv?

##### 8.不同的权值初始化方式以及其造成的后果?为什么会造成这样的结果?

##### 9.Convolution、 pooling、 Normalization是卷积神经网络中十分重要的三个步骤，分别简述Convolution、 pooling和Normalization在卷积神经网络中的作用。

##### 10.dilated conv优缺点以及应用场景

##### 11.判别模型和生成模型解释

##### 12.如何判断是否收敛

##### 13.正则化方法以及特点



#### 实践部分

1.python中range和xrange有什么不同

    说明了两者的区别是xrange返回的是一个可迭代的对象，range返回的则是一个列表. 同时效率更高，更快。
    
2.python中带类和main函数的程序执行顺序

    1)对于  if __name__ == '__main__': 的解释相关博客已经给出了说明，意思就是当此文件当做模块被调用时，不会从这里执行，
      因为此时name属性就成了模块的名字，而不是main。当此文件当做单独执行的程序运行时，就会从main开始执行。
      
    2)对于带有类的程序，会先执行类及类内函数，或者其他类外函数。这里可以总结为，对于没有缩进的程序段，按照顺序执行。然后，才
      到main函数。然后才按照main内函数的执行顺序执行。如果main内对类进行了实例化，那么执行到此处时，只会对类内成员进行初始
      化，然后再返回到main 函数中。 执行其他实例化之后对象的成员函数调用。



    
    
#### 参考文献

[1] https://blog.csdn.net/u014722627/article/details/77938703

