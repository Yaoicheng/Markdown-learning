## 标题
```
# A first-level heading
## A second-level heading
### A third-level heading
...
###### A sixth-level heading
```
使用两个或多个标题时，GitHub 会自动生成一个目录，可以通过单击文件标题中的  来访问该目录。 每个标题都列在目录中，可以单击某个标题导航到所选部分。

![](https://docs.github.com/assets/cb-82863/mw-1440/images/help/repository/headings-toc.webp)
## 文本样式
|Style|符号|快捷键|示例|
|---|---|---|---|
|加粗|`** **` 或 `__ __`|`ctrl+B`|**加粗**|
|斜体|`* *` 或 `_ _` |`ctrl+I`|*斜体*|
|删除线|`~~ ~~`||~~删除线~~|
|粗体和嵌入的斜体|`** **` 和 `_ _`||**This text is _extremely_ important**|
|全部粗体和斜体|`*** ***`||***All this text is important***|
|下标|`<sub></sub>`||This is a <sub>subscript</sub> text|
上标|`<sup> </sup>`||This is a <sup>superscript</sup> text|
## 引用文本
可以使用 > 来引用文本。
```
> Text that is a quote
```
> 引用文本缩进，具有不同的类型颜色。
## 引用代码
使用单反引号可标注句子中的代码或命令。

> 反引号中的文本不会被格式化。

你也可以按 `Ctrl+E` (Windows/Linux) 键盘快捷方式将代码块的反引号插入到 Markdown 一行中。

要将代码或文本格式化为各自的不同块，请使用三反引号。
### 隔离代码块
> 要在列表中保留格式，请确保将非围栏代码块缩进八个空格。
要在围栏代码块中显示三重倒引号，请将其包在四个倒引号内。
### 语法突出显示
您可以添加可选的语言标识符，以在围栏代码块中启用语法突显。

语法突出显示功能会更改源代码的颜色和样式，使其更易于阅读。

例如，要语法突显 Ruby 代码：
````
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
````
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
## 链接
通过将链接文本用方括号 `[ ]` 括起来，然后将 URL 用括号 `( )` 括起来，可创建内联链接。

`This site was built using [GitHub Pages](https://pages.github.com/).`

This site was built using [GitHub Pages](https://pages.github.com/).
### 章节链接
你可以直接链接到渲染文件中的某个部分，方法是将鼠标悬停在该部分标题上以显示 。
![](https://docs.github.com/assets/cb-55933/mw-1440/images/help/repository/readme-links.webp)
链接文本应位于一行上。 下面的示例将不起作用。
### 相对链接
......
## 图像
通过添加 `!` 并将 alt 文本用 `[ ]` 括起来，可显示图像。 替换文字是等效于图像中信息的短文本。 然后将图像的链接用括号 `()` 括起来。
### 指定图像显示的主题
你可以通过结合使用 HTML `<picture>` 元素和 `prefers-color-scheme` 媒体功能来指定在 Markdown 中显示图像的主题。 我们区分浅色和深色模式，因此有两个选项可用。 可以使用这些选项来显示针对深色或浅色背景进行了优化的图像。 这对于透明的 PNG 图像特别有用。

> 例如，以下代码显示浅色主题的太阳图像和深色主题的月亮：
```
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/25423296/163456776-7f95b81a-f1ed-45f7-b7ab-8fa810d529fa.png">
  <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>
```
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/25423296/163456776-7f95b81a-f1ed-45f7-b7ab-8fa810d529fa.png">
  <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

## 列表
可通过在一行或多行文本前面加上 `-`、`*` 或 `+` 来创建一个无序列表。

要对列表排序，请在每行前面添加一个编号。
```
1. James Madison
2. James Monroe
3. John Quincy Adams
```
### 嵌套链表
通过在一个列表项下面缩进一个或多个其他列表项，可创建嵌套列表。
```
1. First list item
   - First nested list item
     - Second nested list item
```
1. First list item
   - First nested list item
     - Second nested list item
## 任务列表
若要创建任务列表，请在列表项前加连字符和空格，后接 `[ ]`。 要将任务标记为完成，请使用 `[x]`。
```
- [x] #739
- [ ] https://github.com/octo-org/octo-repo/issues/740
- [ ] Add delight to the experience when all tasks are complete :tada:
```
- [x] #739
- [ ] https://github.com/octo-org/octo-repo/issues/740
- [ ] Add delight to the experience when all tasks are complete :tada:
如果任务列表项说明以括号开头，则需要使用 \ 进行转义：
## 提及人员和团队
可以在 GitHub 上提及人员或团队，方法是键入 @ 加上其用户名或团队名称。 这将触发通知并提请他们注意对话。 如果您在编辑的评论中提及某人的用户名或团队名称，该用户也会收到通知。
## 使用表情符号
你可以通过键入 `:EMOJICODE` :（冒号后跟表情符号的名称）将表情符号添加到写作中。
键入 : 将显示建议的表情符号列表。 列表将在你键入时进行筛选，因此一旦找到所需表情符号，请按 Tab 或 Enter 键以填写突出显示的结果 。

>有关可用表情符号和代码的完整列表，请参阅 Emoji-Cheat-Sheet。
## 段落
通过在文本行之间留一个空白行，可创建新段落。
## 脚注
您可以使用此括号语法为您的内容添加脚注：
```
Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].

[^1]: My reference.
[^2]: To add line breaks within a footnote, prefix new lines with 2 spaces.
  This is a second line.
```
Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].

[^1]: My reference.
[^2]: To add line breaks within a footnote, prefix new lines with 2 spaces.
  This is a second line.

Wiki 不支持脚注。
## 警报
警报是基于块引用语法的 Markdown 扩展，可用于强调关键信息。 在 GitHub 上，它们以独特的颜色和图标显示，以指示内容的显著性。

> 只有在对用户成功至关重要时才使用警报，并将每篇文章的警报限制在一到两个，以防止读者负担过重。 此外，应避免连续发出警报。 警报无法嵌套在其他元素中。

要添加警报，请使用指定警报类型的特殊块引用行，然后在标准块引用中添加警报信息。 可以使用以下五种类型的警报：
```
> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.
```
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.
## 隐藏有评论的内容
您可以通过在 HTML 评论中加入内容来指示 GitHub 隐藏渲染的 Markdown 中的内容。
```
<!-- This content will not appear in the rendered Markdown -->
```
<!-- This content will not appear in the rendered Markdown -->
## 忽略 Markdown 格式
通过在 Markdown 字符前面输入 \，可指示 GitHub 忽略 Markdown 格式（或对其进行转义）。
## 使用表格组织信息
### 创建表
可以使用竖线 | 和连字符 - 创建表。 连字符用于创建每列的标题，而竖线用于分隔每列。 必须在表格前包含空白链接，以便其正确呈现。
```
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
```
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
表格末尾的竖线可选。

单元格的宽度可以不同，无需在列内准确对齐。 标题行的第一列中必须至少有三个横线。
```
| Command | Description |
| --- | --- |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
```
| Command | Description |
| --- | --- |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
### 格式化表格中的内容
可以在表格中使用格式，例如链接、内联代码块和文本样式：

可以通过在标题行中连字符的左侧、右侧或两侧添加***冒号** :，来靠左、靠右或居中对齐列中的文本。
```
| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |
```
| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |
## 使用折叠部分组织信息
### 创建折叠部分
可以通过创建读者可以选择展开的折叠部分来暂时隐藏 Markdown 的分区。

`<details>` 块中的任何 Markdown 都将被折叠，直到读者单击  展开详细信息。

在 `<details>` 块中，使用 `<summary>` 标记让读者知道里面的内容。 标签显示在  的右侧。
```
<details>

<summary>Tips for collapsed sections</summary>

### You can add a header

You can add text within a collapsed section. 

You can add an image or a code block, too.

```ruby
   puts "Hello World"
```

</details>
```
<details>

<summary>Tips for collapsed sections</summary>

### You can add a header

You can add text within a collapsed section. 

You can add an image or a code block, too.

```ruby
   puts "Hello World"
```

</details>

## 创建关系图
### 关于创建关系图
可以使用以下三种不同的语法在 Markdown 中创建关系图：mermaid、geoJSON 和 topoJSON、ASCII STL。 关系图可在以下项中呈现：GitHub Issues、GitHub Discussions、拉取请求、Wiki 和 Markdown 文件。
### 创建 Mermaid 关系图
Mermaid 是一款受 Markdown 启发的工具，可将文本呈现为关系图。 例如，Mermaid 可以呈现流程图、序列图、饼图等。 

例如，可以通过指定值和箭头来创建流程图。
````
Here is a simple flow chart:

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
````
## 编写数学表达式
......
