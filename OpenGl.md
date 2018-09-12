#图形绘制流程
##流程
1. glBufferData()  //准备向OpenGl传输数据  
2. glDrawArrays()   //绘制数据传输到OpenGl服务端  
3. pass-through shader //顶点着色  
4. tessellation shader  // 细分着色  
5. 几何着色  
6. 图元装配  
7. 剪切  
8. 光栅化 
9. 片元着色  
10. 逐片元的操作  //在这个阶段里会使用深度测试

##示例代码
```
void display(void)  
{
    glClear(GL_COLOR_BUFFER_BIT);
    glBindVertexArray(VAOs[Triangles]);
    glDrawArrays(GL_TRIANGLES, 0, NumVertices);
    glFlush();
}
```


#着色器基础
##概念
1. in 存储限制符 // 用于定义着色器阶段的输入变量
2. out 存储限制符 // 用于定义着色阶段的输出变量
3. uniform 存储限制符 // 用于制定一个在应用程序中设置好的变量




