下面是一个Python代码示例，用于生成自述文件的Markdown模板，并包含详细的注释与解释。

```python
# 导入os模块，用于与操作系统进行交互
import os

def create_readme(file_name='README.md'):
    """
    创建一个Markdown格式的自述文件模板

    参数:
    file_name (str): 要创建的文件名，默认是'README.md'
    """
    # 定义Markdown模板内容
    template_content = """
    <!-- This is the markdown template for the final project of the Building AI course,
    created by Reaktor Innovations and University of Helsinki.
    Copy the template, paste it to your GitHub README and edit! -->

    # Project Title
    Final project for the Building AI course
    
    ## Summary
    Describe briefly in 2-3 sentences what your project is about. About 250 characters is a nice length! 

    ## Background
    Which problems does your idea solve? How common or frequent is this problem? What is your personal motivation? Why is this topic important or interesting?

    This is how you make a list, if you need one:
    * problem 1
    * problem 2
    * etc.

    ## How is it used?
    Describe the process of using the solution. In what kind situations is the solution needed (environment, time, etc.)? Who are the users, what kinds of needs should be taken into account?

    Images will make your README look nice!
    Once you upload an image to your repository, you can link to it like this (replace the URL with your image's URL).
    """

    # 使用with语句打开文件，确保文件会被正确关闭
    with open(file_name, 'w', encoding='utf-8') as file:
        # 将模板内容写入文件
        file.write(template_content.strip())  # 使用strip()去除首尾的空白字符

    print(f'{file_name} created successfully!')

# 调用函数以生成README.md文件
create_readme()
```

### 代码解释

1. **导入模块**: 使用`import os`导入操作系统模块，虽然在本例中并未直接使用，但通常用于处理文件和目录操作。

2. **定义函数**: `create_readme`函数接收一个参数`file_name`，用于指定生成的自述文件名，默认为`README.md`。

3. **Markdown模板**: `template_content`字符串包含了自述文件的基本结构和内容，使用Markdown语法编写，方便后续修改。

4. **写入文件**:
   - 使用`with open(file_name, 'w', encoding='utf-8') as file`打开文件，这会在当前目录下创建一个新的文件，或者覆盖已存在的文件。
   - `file.write(template_content.strip())`将模板内容写入文件，同时使用`strip()`方法去除字符串首尾的空白字符。

5. **提示用户**: 打印一条消息，确认文件已成功创建。

6. **调用函数**: 在脚本的最后，调用`create_readme()`函数以生成README文件。

通过运行此代码，您将获得一个包含格式化示例文本的README.md文件，可以根据自己的项目需求进行编辑与修改。
