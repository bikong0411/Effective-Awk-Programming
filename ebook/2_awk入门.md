#2 awk入门

awk的基本功能就是从文件的行(或者其他的文本单位)中去搜索包含的模式。当某一行匹配到众多模式中的一个时就会对这那一行执行特定的动作。awk保持这种方式处理输入文件只到达文件的末尾。

awk程序不同于其他大多数程序，因为awk程序是数据驱动的。也就是说，你需要描述出你希望处理的数据，并且还要描述出当你找到这些数据之后下一步该如何去做。大多数其它语言的程序，你需要很详细的去描述每一步程序程序需要去做什么，当使用这些语言工作的时候，通常很难清楚的描述出你的程序将要处理的数据。出于这个原因awk程序经常能很清爽容易的对数据进行读取和写入。

当你执行awk的时候，你需要知指定一个awk程序，告诉awk做什么。程序包含一系列规则(可能包含函数定义，一个先进的功能，现在我们将忽略，第13章[用户自定义函数]会提到)，每一个规则指定了一个要查找的模式和一个查找到模式之后要执行的动作。

在语法上规则由一个动作接着一个模式。在大括号内的动作模式分开。规则通常由换行符分隔。因此，awk程序看起来像这样：

<pre>
pattern { action } 
pattern { action }
 ...
</pre>

