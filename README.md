# amazingzyj.github.io
My Github Blog.
一、简述

Perl的现状

Perl的全称为Practical Extraction and Report Language, 由Larry Wall在1980年代中期发布. Perl是一门动态类型, 解释运行的语言, 跟传统的静态类型, 编译型语言相比, Perl的开发效率非常之高. Perl有强大的底层数据结构, 强大的内置函数和一系列以正则表达式为核心的文本处理工具, 通过”引用”还可以实现面向对象以及函数式等不同的编程范式. 

作为一门超过30岁的语言, Perl曾经在1990年代风靡程序员世界, 网络上的黑客(Hacker)都以探索Perl中的奇技淫巧为荣, 他们也是CPAN(Comprehensive Perl Archive Network)上代码的主要贡献者.

但是, 不得不承认, 在同类型语言中, 如今的Perl的热度已经完全不及Python, 甚至是跟Perl有着直接关系的后继者Ruby. 行业发展至今, 一个软件的规模越来越庞大, 代码的可读性和可维护性也越来也受到重视. 

Perl从诞生之初, 就有”write-only”的标签. Perl的设计哲学”一个问题有多种解决方案(There is more than one way to do it)”, 晦涩复杂的语言机制, 还有数量繁多把几乎所有符号用了个遍的内建变量[ 符号用的多不便记忆, 影响可读性是一个方面, 这个特性也会对网络内容搜索造成困扰, 因为搜索引擎会对特定的符号做转义.], 这些先天因素, 使得Perl在可读性和可维护性上始终是得分最低的一档. 

而作为Perl的”反面”, Python无论在词法[ 根据官方文档显示, Python的keywords只有33个.]还是语法上, 都显得非常的简洁克制. Python的OOP是内置的, 其他的扩展都通过函数调用或者对象方法接口来使用, 这样功能使用上的一致性也得到了保证. 于此, Python受到了很多非计算机领域的欢迎, 在网络社区上的热度越来越高, 甚至已经出现在小学的教材中了. 种种原因, 业界的新开发者, 入门者, 已经不会再选择Perl, 这就是Perl的现状. 

IC行业中的Perl

同其他行业一样, IC行业中的Perl也曾经是长久以来的首选脚本语言. Linux开发环境, 文本处理需求, 快速的写出一些小工具, 这些都是Perl的生存土壤. IC工程师用Perl开发了大量的工具, 比如flow控制, 验证平台搭建, 激励生成等工具. 但是, 这个行业的工程师, 特别是新工程师, 如果在项目上没有历史包袱的话, 还是更愿意用Python工具, 想一想我们项目里现在使用的验证平台生成工具, 还有寄存器模型生成工具.
那么, Perl还值得学习吗? 这里引用”小骆驼书”《Learning Perl(Perl语言入门)》中的一段话:

如果想知道Perl和X语言哪个比较好, 最好的方法就是把两者都学会, 看看后来最常用哪个, 那就是最适合你的语言. 反正, 你会因为学了X语言而增进对Perl的了解(反之亦然), 所以并没有浪费时间.
其实这种说法可以扩展, 作为工程师来讲, 多掌握一项工具技能总是有益的. Perl还是那个Perl, 只是需要重新定位一下. 平心而论, 尽管已经不适用于比较上规模的工具开发, 但是回顾一下Perl的优点: 语法灵活, 文本处理能力强大. 我们发现, 如果需要快速的写一个一次性的超短脚本, 或者直接在命令行直接进行一些文本处理, Perl还是很好的一个选择.
通过本教材的训练, 你会发现, Perl在命令行上是一个可以结合grep, sed和awk的特性的威力巨大的工具. 

本教程的覆盖范围和目标

本教程面向Perl初学者, 覆盖的范围包括:

1.Perl基础语法, 包括三大基础数据结构,基础分支和循环控制结构以及子程序;

2.正则表达式, 介绍最常用的一些正则表达式规范和匹配模式, 以及s表达式的使用;

3.Perl one-liners, 在命令行使用Perl进行一些文本处理任务;

也许Perl的命运最终会像前辈awk一样, 虽然可以用来写出篇幅巨大功能复杂的脚本, 但是人们还是更愿意在命令行使用Perl. 本教程的目标就是让读者通过这篇文档的学习, 通过Perl的基础语法, 和正则表达式的了解, 可以熟练掌握在命令行使用Perl进行文本处理任务. 

参考资料介绍除了本教程的内容之外, 读者还可以针对性的做一些扩展阅读, 本教程推荐的主要参考资料有:

1.骆驼书三部曲: (《Learning Perl(Perl语言入门)》、《Intermediate Perl(Perl进阶)》、《Mastering Perl(精通Perl)》). 三本书的作者都是Randal L. Schwartz, brian d foy和Tom Phoenix, 三本书内容由浅入深, 可读性非常高. 《Learning Perl(Perl语言入门)》介绍的是Perl最基础的一些特性, 包括基础语法和正则表达式的基本应用.《Intermediate Perl(Perl进阶)》加入了引用的内容, 并开始介绍大型程序的编写管理以及程序的测试. 《Mastering Perl(精通Perl)》涉及了更深入的细节, 包括Perl的调试技术, Perl的配置技术还有Perl的性能讨论等.

2.正则表达式: 《Mastering Regular Expression》. 在骆驼书三部曲里面, 已经有很多关于正则表达式的内容, 而这本书是骆驼书中推荐的正则表达式的扩展阅读书目. 这本书对正则表达式有着更细节更深入的探讨, 包括不同的正则表达式”风味”，正则表达式的世界是一个混乱的世界, 正则表达式通常作为一个插件”寄生”在各种语言和工具中, 虽然有POSIX定义的BREs(基础正则表达式)和EREs(扩展正则表达式)标准, 各种语言和工具还是会为正则表达式加入很多”私货”, 比如, VIM里面就同时存在着4套不同的正则表达式匹配规则.], 正则表达式的原理还有性能讨论.

3.命令行工具: 《PERL ONE-LINERS》. 这本书介绍了Perl在命令行环境下的使用, 并给出了大量的实例, 是工具手册性质的参考书. 本教材的第四部分内容主要取自于这本书.

4.官方文档: Perl doc. 每个版本的Perl doc都可以从perldoc.perl.org获取, 通常说来, 官方文档里面可以找到大部分问题的答案, 而且是最全面的答案[ 比如, 你可以在Perl doc的perlvar里查到所有的builtin特殊变量, 在perlrun里查到所有的Perl运行时模式开关.]. 

基于本教程的目标, 这里推荐重点阅读的是《Learning Perl(Perl语言入门)》和《PERL ONE-LINERS》, 其他的参考资料就当做是扩展阅读. 然后, 官方文档的话, 建议作为手边资源, 随时翻阅.




二、Perl基础语法

基础数据结构

Perl数据类型包括标量、数组和哈希.


标量

所谓变量, 就是存储一个或者多个值的容器的名称. 而标量, 就是单单存储一个值的变量. 标量的名称以美元符号$开头, 然后是变量的Perl标识符：由一个字母或下划线开头, 后接多个字母、数字或下划线. 标识符是区分大小写的, 不同的大小写字母、数字以及下划线构成不同的标识符, 所以下面的变量各不相同：

	$name
  	$Name
  	$NAME
  	$a_very_long_variable
  	$A_very_long_variable
  	$averylongvariable
  
对标量最常见的操作就是赋值了, Perl的赋值操作符为等号, 等号左边是变量名称, 右边为某个表达式, 对表达式求值的结果作为赋予变量的值. 

	$fred = 17; #将$fred的值设置为17
	$barney = ‘hello’; #将$barney的值设置为字符串’hello’
	$barney = $fred+3; #将$barney的值设置为$fred当前值加上3后的结果, 即20
	$barney = $barney*2; #将$barney的值设置为$barney当前值乘以2后的结果, 即40



数组

列表是标量的有序集合, 而数组是存储列表的变量. 在Perl中, 这两个术语经常混用. 数组中的每一个元素都是单独的标量变量, 拥有独立的标量值. 这些值是有序的, 也就是说, 从起始元素到终止元素的先后次序是固定的. 数组中的每个元素都有相应的整数作为索引, 此数字从零开始递增, 每次加1. 假如你对索引值超过数组尾端的元素进行赋值, 数组将会自动扩大（只要有可用的内存分配给Perl, 数组的长度是没有上限的）, 如果在扩展过程中需要创建增补元素, 那么它们的默认取值为undef：

	$rocks[0] = ‘bedrock’;
	$rocks[1] = ‘slate’;
	$rocks[2] = ‘lava’;
	$rocks[99] = ‘schist’;

有时候我们需要找出数组里最后一个元素的索引值, 数组rocks的最后一个元素的索引值为$#rocks, 这个索引值比数组元素的个数少1：

	$end = $#rocks; #99, 也就是最后一个元素的索引值

在Perl程序里, 需要经常建立简单的单词列表, 这时只需要使用qw简写, 就可以省去键入许多无谓引号的麻烦：

	(“fred”, “barney”, “betty”, “wilma”, “dino”)
	qw( fred barney betty wilma dino ) # 同上, 更简洁, 也更少击键
	
	Perl会将qw简写的内容当成单引号内的字符串来处理, 空格、制表符以及换行符都会被抛弃. 

	qw(fred
		barney     betty
		wilma dino) # 同上

前面的例子都是以圆括号作为定界符, 其实Perl允许任何标点符号作为定界符. 如果起始定界符是某种“左”字符, 那么结尾定界符必须是对应的“右”字符：

	qw{ fred barney betty wilma dino }
	qw< fred barney betty wilma dino >
	qw/ fred barney betty wilma dino /
	qw# fred barney betty wilma dino #

当你希望引用整个数组时, Perl提供了一个比较简单的记法：只要在数组名之前加上@字符就可以了, 可以读作“所有的/全部的”, 比如@rocks可以读作“所有的rocks”. 

常见的数组操作符有：pop、push、shift、unshift、splice、reverse、sort等. 


哈希

哈希和数组类似, 不同之处在于索引方式, 数组是以数字来索引, 而哈希则是以任意字符串来索引, 哈希的索引值称为键（key）. 

访问哈希元素, 使用如下语法：

	$hash{$some_key}

和访问数组类似, 只是使用了花括号而不是方括号. 而且, 索引值为字符串而不是数字：

	$family_name{$fred} = ‘flintstone’；
	$family_name{$barney} = ‘rubble’;

访问整个哈希, 可以用百分号（%）作为前缀. 因此前面我们使用的哈希准确来说应该称之为%family_name. 

哈希可以与列表互相转换. 对哈希赋值等同于在列表上下文中赋值, 列表中的元素应该为键-值对：

	%some_hash = (‘foo’, 35, ‘bar’, 12.4, 2.5, ‘hello’, ‘wilma’, 1.72e30, ‘betty’, “bye\n”)；

在列表上下文中, 哈希的值是简单的键-值对列表：

	@any_array = %some_hash;

我们把这个变换叫做展开哈希, 将它变成键-值对列表. 当然, 得到的键-值对不一定是按照当初赋值时的顺序展开：

	print “@any_array\n”;

#打印结果为：

	#betty bye
	#wilma 1072e30 foo 35 2.5 hello bar 12.4

之所以顺序乱掉是因为Perl已经为哈希的快速检索而对键-值对的存储做了特别的排序. 

在将列表赋值到哈希时常常会发现列表中的键-值对并不容易区分, 我们可以使用胖箭头“=>”来表示键-值对：

	my %last_name = (
	‘fred’ => ‘flintstone’,
	‘dino’ => undef,
	‘barney’ => ‘rubble’,
	);

这样键-值对就看起来清晰多了. 注意, 列表结尾有一个额外的逗号, 这种写法不但无伤大雅, 而且方便维护. 

哈希函数有：keys、values、each、exists、delete等. 

keys函数能返回哈希的键列表, values函数能返回对应的值列表. 如果哈希没有任何成员, 则两个函数都返回空列表. 

如果需要迭代（逐项处理每个元素）整个哈希, 可以使用each函数：

	while( ( $key, $value ) = each %hash ){
	...
	}

如果要检查哈希中是否存在某个键, 可以使用exists函数, 返回1则表示存在, 返回0则表示不存在. 

	if( exists $hash{“dino”}){
	...
	}

delete函数能从哈希中删除指定的键及其对应的值. 如果哈希中没有这样的键, 它就会直接结束, 不会发出任何警告或者错误信息. 

	delete $hash{“dino”};


标量上下文和列表上下文

所谓上下文, 指的是你如何使用表达式. 比如按照数字方式进行操作时得到的就是数字结果, 按照字符串方式进行操作时返回的是字符串结果. 并且, 起到决定性因素的是操作符, 而不是被操作的各种变量或直接量. 2*3中的*作为对数字的乘法运算符号时得到的结果就是数字6, 而2x3中的x则表示字符串重复操作, 所以得到的结果是字符串222. 

	42 + something # 这里的something必须是标量
	sort something # 这里的something必须是列表

就算something这个单词的拼写保持不变, 它却会在某种情况下得到单一的标量值, 在另外的情况下得到列表. 在Perl中, 表达式总是根据所需要的上下文返回对应的值：

	@people = qw( fred barney betty );
	@sorted = sort @people; # 列表上下文：barney, betty, fred
	$number = 42 + @people; # 标量上下文：42 + 3 = 45

即使在普通的赋值运算, 都可以有不同的上下文：

	@list = @people; # 得到3个人的姓名列表
	$n = @people; # 得到人数3

某些表达式不会在标量上下文中返回任何值, 比如sort表达式, 其实没人会统计列表排序后的元素个数, 所以sort在标量上下文中总是返回undef. 

下面列出一些常见的标量上下文：

	$fred = something; 
	$fred[3] = something;
	123 + something
	if(something) {...}
	while(something){...}
	$fred[something] = something;

下面列出一些常见的列表上下文：

	@fred = something;
	($wilma, $betty) = something;
	($dino) = something;
	push @fred,  something；
	foreach $fred (something){...}
	sort something
	reverse something
	print something


流程控制

foreach控制结构

foreach能逐项遍历列表中的值, 依次迭代：

	foreach $rocks ( qw/ abc def ghi jkl mno/ ){
	...
	}


while控制结构

	while(测试){
		程序主体；
		递增；
	}


if控制结构

（elseif else）后面的花括号{}是必须要有的

表达式为真时, 执行某块代码：

	if(表达式){...}
	else if(表达式){...}
	else{...}


unless控制结构（else）

与if用法一样, 但意义相反, 表达式为假时才执行模块代码


until控制结构

与while用法一样, 但意义相反


for控制结构

与其他高级语言一样

	for(初始值; 测试; 递增){
	程序主体；
	}



函数

Perl允许用户创建子程序, 也就是用户自定义的函数. 子程序可以让我们重复利用已有的代码. 子程序的名称也属于Perl标识符的范畴, 即由字母、数字和下划线组成, 但是不能以数字开头. 


定义子程序：

	sub 子程序名{
	...
	}


调用子程序：在子程序名前加上与号（&）

&子程序名；


返回值

在Perl中, 所有的子程序都有一个返回值, 但并不是所有的Perl子程序都包含有用的返回值. 既然任何Perl子程序都有返回值, 那么规定每次必须写“return”就非常费事了, 所以Perl将其简化了, 在子程序执行的过程中, 最后一次运算的结果（不管是什么）都会被自动当成子程序的返回值. 

	sub sum_of_fred_and_barney{
		print “Hey, you call the sum_of_fred_and_barney subroutine!\n”
		$fred + $barney; # 这就是该子程序的返回值
	}

注意, 如果在上面子程序代码结尾新增一条print语句：

	sub sum_of_fred_and_barney{
		print “Hey, you call the sum_of_fred_and_barney subroutine!\n”
		$fred + $barney; 
		Print “Hey, I’m returning a value now!\n” # 新增print语句
	}

最后执行的表达式并非加法运算, 它的返回值通常为1, 表示成功输出信息, 但是这并不是我们想要的返回的值. 所以在子程序里增加额外的程序代码时, 请小心检查最后执行的表达式是哪一个, 确定它是你要的返回值. 


参数

Perl子程序可以有参数. 要传递参数列表到子程序里, 只需在子程序调用的后面加上被括号圈引的列表表达式就可以了. Perl会自动将参数列表化名为特殊的数组变量@_, 该变量在子程序执行期间有效. 子程序可以访问这个数组, 以判断参数的个数以及参数的值. 

	$n = &max(10, 15);
	sub max{
		if( $_[0] > $_[1] ){
			$_[0];
		}
		else{
			$_[1];
		}
	}



子程序私有变量（my）

默认情况下, Perl里面所有的变量都是全局变量, 在程序的任何地方都可以访问它们. 但是我们可以借助my操作符来创建私有变量, 我们称之为词法变量：

	sub max{
		my($m, $n); # 创建该语句块中的私有变量
		($m, $n) = @_; # 将参数赋值给变量
		if( $m > $n ){ $m } else { $n }
	}

$m和$n就是属于封闭语句块的私有变量, 语句块之外任意地方的$m和$n都完全不受这两个私有变量的影响. 反过来, 外部变量也无法影响内部的私有变量. 

事实上, 词法变量可以使用在任何语句块内, 比如if、while、foreach语句块里面：

	foreach (1..10){
		my($square) = $_ * $_;
		print “$_ squared is $square.\n”;
	}

注意, my操作符并不会更改变量赋值时的上下文：

	my($num) = @_; # 列表上下文, 和 ($num) = @_; 一样
	my $num = @_; # 标量上下文, 和 $num = @_; 一样

还要注意, 在my操作符不加括号时, 只能用来声明单个词法变量：

	my $fred, $barney; # 只声明了$fred
	my( $fred, $barney ); # 两个都声明了


子程序的持久性私有变量（state）

在每次调用子程序时, 在子程序中使用my创建的私有变量都会被重新定义. 而使用state操作符来声明变量, 可以再子程序的多次调用期间保留变量之前的值, 并将变量的作用域局限在子程序内部. 这个特性是从Perl5.010开始引入的. 

	use 5.010;
	sub marine{
		state $n = 0; #持久性私有变量
		$n += 1;
		print “Hello, sailor number $n!\n”;
	}
多次调用上面的子程序后, $n的值会一直递增, 不会因为重新调用子程序后而清零. 


return操作符

	如果想要在子程序执行到一半时停止执行, 这就需要return操作符来完成了, 它会立即停止执行并从子程序内返回某个值. 

	my @names = qw/ fred barney betty dino wilma/;
	my $result = $which_element_is(“dino”, @names);
	sub which_element_is{
		my( $what, @array) = @_;
		foreach(0..$#array){
			if($what eq $array[$_]){
				return $_;
			}
		}
		-1;
	}

这个子程序用来找出@names数组中值为dino的元素的索引, 当搜索到dino后停止执行子程序, 并立刻返回其索引值. 如果没找到元素dino, 则会返回-1作为“查无此值”的数字代码. 



省略调用子程序的与号

如果编译器在调用子程序之前看到过子程序的定义, 或者Perl通过语法规则判断它只能是子程序调用, 那么对待该子程序就可以像内置函数那样, 在调用时省略与号. 要注意的是, 假如定义的子程序的名字和内置函数相同, 为了避免歧义, 就必须使用与号调用. 加上与号, 就说明调用的是我们自己定义的子程序. 



三、Perl中的正则表达式

在第一章, 我们提到过, 正则表达式通常作为插件存在于各种工具和语言中, 尽管有POSIX在正则表达式上的标准化尝试, 不同的工具和语言还是会在正则表达式上有小小的自由发挥. 本教程所谈论的正则表达式特指Perl中实现的正则表达式, 而且简便起见, 我们只会讨论ASCII字符集范围内的正则表达式匹配规则. 除了基础正则表达式语法规则外, 还会涉及Perl的一些选项. 


正则表达式规则

现在我们来正式的介绍一下正则表达式. 正则表达式是什么呢?

字符是计算机软件处理文字时最基本的单位, 可能是字母, 数字, 标点符号, 空格, 换行符, 汉字等等. 字符串是0个或更多个字符的序列. 文本也就是文字, 字符串. 说某个字符串匹配某个正则表达式, 通常是指这个字符串里有一部分（或几部分分别）能满足表达式给出的条件. 

很可能你使用过Windows/Dos下用于文件查找的通配符(wild-card), 也就是*和?. 如果你想查找某个目录下的所有的Word文档的话, 你会搜索*.doc. 在这里, *会被解释成任意的字符串. 和通配符类似,正则表达式也是用来进行文本匹配的工具, 只不过比起通配符, 它能更精确地描述你的需求——当然, 代价就是更复杂——比如你可以编写一个正则表达式, 用来查找所有以0开头, 后面跟着2-3个数字, 然后是一个连字号“-”, 最后是7或8位数字的字符串(像010-12345678或0376-7654321)[ 这个匹配可以用0\d{2,3}-\d{7,8}这个正则表达式来描述, 至于为什么是这样, 相信通过本章后续的阅读你就能理解了.]. 

总之, 正则表达式是用来做本文匹配的, 接下来我们会介绍具体的匹配规则[ 实际上本文档会介绍Perl的正则表达式中大约90%的最基本最常用匹配特性, 这部分以外的特性, 请参考《Mastering Perl》或是Perl doc中的perlre部分.].

常规字符
常规字符是最基本的匹配单元, Perl中所有的没有转译的常规字符如下:

	0 1 2 3 4 5 6 7 8 9
	a b c d e f g h i j k l m n o p q r s t u v w x y z
	A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
	` ~ ! @ # % & - = , : ; “ ‘ / < >

常规字符的匹配规则非常简单, 就是直接的按字符匹配, 比如abc可以匹配字符串”abcde”中的”abc”部分和其他直接包含”abc”的其他字符串中的”abc”部分.


测试工具

本教程建议读者在学习正则表达式的过程中, 使用正则表达式测试工具进行实时的练习. 正则表达式测试工具有很多, 如果可以上网的话, 可以查到很多在线工具或者是离线工具, 随便挑一个支持Perl正则表达式的就可以了.

如果是不能上网的话, 这里建议使用Linux下自带的grep工具, 使用命令:

	grep -P ‘regexp’
	
然后回车, 进入键盘输入交互模式. 命令中的-P(注意是大写)表示使用Perl的正则表达式, ‘regexp’就是你要测试的正则表达式, 这里用单引号避免一些命令行上变量的转义. 之后每一行的输入, grep就会作为正则表达式的匹配文本, 在下一行输出匹配结果, 如果下一行为空说明没有匹配上.

此外, 建议最好配置一下grep的环境变量:

	setenv GREP_OPTIONS --color=auto
	
设置为高亮模式, 这样匹配成功的话, 还会高亮显示具体匹配到的字符串.

这个截图是一个用正则表达式’abc’的测试示例, 输入的待匹配文本依次为”abc”, “ab”, “abca”, “abcaabcdef”. 匹配结果在每次输入的正下方, 可以看到除了”ab”没有匹配成功外, 其他字符串都有匹配成功并高亮显示了匹配成功的部分.

字符集合

[char_set]这种格式就是匹配所有在char_set中的一个字符(“[“和”]”不在常规字符集中, 这是我们下一节要讨论的元字符). 

比如, [ab]可以匹配”abcde”中的”a”和”b”, [aeiou]匹配任意的元音字符, fred可以匹配所有直接包含”fred”的字符串, 而[Ff]red可以匹配包含”fred”或者”Fred”的字符串.

字符集合可以支持范围操作符, 比如[0-9]表示0~9的集合, [a-z]表示a~z的集合.

[^char_set]这种格式匹配所有不在char_set这个字符集合中的一个字符, 是[char_set]的补集.

元字符

正则表达式中定义有特殊含义的字符为元字符(meta-character), 元字符是正则表达式的真正精华所在(也是各种工具中会发生歧义的地方). Perl中的所有元字符如下:

	\ ^ . [ ] $ { } * ( ) + | ?
	
我们不会把所有元字符的含义在这一节就讲完, 只打算介绍’.’和’\’, 后续的其他元字符还是按功能分类来逐步介绍.

.可以匹配任意的字符, 包括所有的可见字符和所有的不可见字符, 相当于是wildcard, 也可以用[^]来表示.

\为转义元字符, 表示\后面跟着的字符会组合成特定的匹配规则, 是正则表达式中功能最多的元字符.

如果需要匹配元字符本身, 需要用”\元字符”的形式, 比如要匹配”\”的话要用”\\”, 需要匹配”(abc)”的话要用”\(abc\)”.

\可以跟后续字符组合成匹配集合:

	模式		匹配内容				等效集合
	\w		所有的标识符字符		[_a-zA-Z0-9]
	\W		所有的非标识符字符		[^_a-zA-Z0-9]
	\d		所有的数字				[0-9]
	\D		所有的非数字				[^0-9]
	\s		所有的空白字符, 包括space和tab	
	\S		所有的非空白字符	

\可以跟后续字符组合表示ASCII字符集中的特殊字符:

	\t        tab                    (HT, TAB)
	\n        newline				 (LF, NL)
	\t        return				 (CR)
	\f        form feed		         (FF)
	\a        alarm(bell)			 (BEL)
	\e        escape(think troff)    (ESC)

\转义组合还有很多, 后面还会陆续介绍.


匹配次数限定符

前面讲的内容都是单次匹配, 正则表达式当然也支持多次匹配的模式, 这个在正则表达式的术语中称为匹配次数限定符. 匹配次数限定符跟在具体的匹配字符之后, 用来表示这个匹配字符匹配的次数. 

Perl中支持的匹配次数限定符如下:

	*       Match 0 or more times
	+       Match 1 or more times
	?       Match 1 or 0 times
	{n}     Match exactly n times
	{n,}    Match at least n times
	{n,m}   Match at least n but mot more than m times

有了匹配次数限定符之后, 正则表达式的强大之处的渐渐体现出来了, 此刻相信你已经知道用”0\d{2,3}-\d{7,8}”来匹配电话号码是怎么回事了. 

编程语言中一般会要求标识符不能以数字开头, 这样, 我们可以用”[_a-zA-Z]\w+”来匹配标识符, “\$[_a-zA-Z]\w+”则可以匹配一个Perl中的scalar变量, “\@[_a-zA-Z]\w+”可以匹配Perl中的array变量. 有了这些, 正则表达式已经可以实现一些基本的文本分析功能了.

匹配次数限定符默认情况下是”贪婪”模式的, 就是说会默认尽可能多次的匹配, 比如使用”a\w+a”去匹配字符串”abcabcabc”, 会匹配到”abcabca”. 如果需要进行”非贪婪”模式的次数匹配, 需要在匹配次数限定符后面加上’?’:

	*?      Match 0 or more times
	+?      Match 1 or more times
	??      Match 1 or 0 times
	{n}?    Match exactly n times
	{n,}?   Match at least n times
	{n,m}?  Match at least n but mot more than m times

在上个例子中, 如果用”a\w+?a”, 则匹配结果是”abca”.



位置匹配

正则表达式中, 还有不匹配具体字符, 只匹配位置的模式, Perl支持的位置匹配如下:

	模式	匹配位置
	^      行首
	$      行末
	\b    Word边界
	\B   非Word边界
	\A    字符串首
	\Z    字符串尾

有了位置匹配, 正则表达式的匹配就更加精确了. 比如, 你用”Don”可以匹配到”Donald”或者”MacDonald”中的”Don”, 用”\bDon\b”才能精确的匹配到”Don”. 

‘^’, ‘$’和‘\A’, ‘\Z’看过去是差不多的, 实际使用上也是差不多的, 只是在做多行匹配的时候会有不同的行为, 这个我们后面再讨论.


分组匹配

分组匹配是让正则表达式的能力进一步提升的特性, 不过也是让正则表达式变得晦涩, 复杂, 赋予其”write-only”属性的一个特性.

在分组匹配之前, 我们先来了解一下元字符’|’.

‘|’跟编程语言中的逻辑运算”或”的含义一致, 在正则表达式里面也是”或”的意思. “abc|def”可以匹配”abc”或”def”, 这个看上去很简单, 但是如果你想用一个正则表达式匹配”Paul Gasol”或者”Marc Gasol”, 要怎么操作呢? 

这个时候你就需要用分组匹配了, Perl中用括号()来生成一个分组, 现在你可以用”(Paul|Marc) Gasol”来同时匹配”Paul Gasol”或者”Marc Gasol”.

正则表达式的中分组没有数量限制, 而且可以嵌套组合使用. 这样就可以和其他匹配规则组合成相当强大同时也相当复杂的规则.

此外, 基于分组匹配这个特性, Perl中的正则表达式还支持分组捕获跟反向引用的特性. 具体说来就是, 正则表达式引擎会对每个分组进行编号, 然后后续\1, \2, ...这些可以引用前面的分组内容.

比如, 正则表达式“(abc)\1”相当于”abcabc”. 分组的编号规则是以左括号的出现顺序, 从1依次编号. 正则表达式中“(((Paul)|(Marc)) (Gasol))”, \1的内容是”((Paul)|(Marc)) (Gasol)”, \2的内容是”(Paul)|(Marc)”, \3的内容是”Paul”, \4的内容是”Marc”, \5的内容是”Gasol”.

然后”(((Paul)|(Marc)) (Gasol)) comes from \5 family, \3 is the elder brother and \4 is the younger brother.”会生成”Paul Gasol comes from Gasol family, Paul is the elder brother and Marc is the younger brother”或者”Paul Gasol comes from Gasol family, Paul is the elder brother and Marc is the younger brother”然后进行匹配.

反向引用特性是分组匹配最重要的特性, 这个特性还会在正则表达式匹配之后发挥重要的作用, 本文档会在后续章节继续讲述.


用m表达式做匹配

Perl中使用正则表达式对一个字符串做匹配的标准格式是:

	if ($text =~ m/regexp/) {
		...
	}

“=~”是绑定操作符, “m/regexp/”就是m表达式, ‘/’是Perl正则表达式的默认定界符(delimiter), 定界符之间就是正则表达式的内容.

匹配表达式会首先返回一个真值, 如果为1表示匹配成功, 然后进行后续处理. 这也是基于正则表达式的文本处理的一般流程.

可能你在Perl代码中会更常见到:

	if (/regexp/) {...}
	
这种形式的代码是

	if ($_ =~ m/regexp/) {...}
	
的简写, 实际上你在使用的时候, 这种形式也是更常用(包括我们的后续章节)的.


模式定界符

之前我们提到过, Perl中的’/’是常规字符, 但是使用’/’作为模式定界符之后, 想要在模式中匹配’/’的话, 就需要写成’\/’的形式.

Perl中可以使用其他的符号作为正则表达式的定界符, 前提是不能使用简化形式, 只能使用m表达式.

可以使用单目符号:

	m!...!
	m,..., 
	m#...# 
	m|...| 
	
也可以使用括号:

	m{...} 
	m<...> 
	m[...] 
	m(...)


匹配选项

在m表达式的最后, 可以加入一些匹配选项. Perl中支持的匹配选项如下:

	选项	功能
	/i	忽略大小写
	/x	忽略空白, 添加注释支持
	/s	使.匹配换行符
	/m	扩展多行模式

/i跟/s选项的意义很明显了, 在/m模式下, 前面提到的‘^’, ‘$’和’\A’, ‘\Z’就出现了不同的行为.
这里重点介绍一下/x选项, 这是Perl为了正则表达式的可读性做出的可贵的努力.

	/-?[0-9]+\.?[0-9]*/
	/ -?[0-9]+ \.? [0-9]* /x
	
这两条正则表达式是等价的, 加了/x选项之后, 用空格把正则表达式分成几个部分, 可读性有了一点点的提升.

	/
	-?		# an optional minus sign
	[0-9]+	# one or more digits before the decimal point
	\.?		# an optional decimal point
	[0-9]*	# some optional digits after the decimal point
	/x
	
这个正则表达式跟上面的两条仍然等价, 用断行再加注释的方式, 这样的正则表达式的可读性就很强了. 建议大家在编写复杂正则表达式的时候可以尝试着用/x选项, 来进行可读性上的优化.

要注意/x模式下用’#’来进行后续的文本注释, 这个时候要匹配’#’的话要用”\#”.
匹配选项可以组合使用:

	if(m{
		Barney	# the little guy
		.*		# anything in between
		Fred		# the loud guy
	}six){	# all three of /s and /i and /x
		Print “That string mentions Fred after Barney!\n”;
	}
	
使这些选项功能同时生效.


匹配之后的特殊变量

这里介绍变量匹配结果变量$`, $&, $’和分组捕获结果变量$1, $2, ...$n(n取决于分组数量有多少). 这些变量将在正则表达式匹配之后的文本处理和分析中发挥重要的作用.

匹配完成之后, $&存储着整个正则表达式匹配到的文本字符串内容, $`为$&之前的文本字符串内容, $’为$&之后的文本字符串的内容. 比如, 使用正则表达式”bcd”对字符串”abcde”进行匹配, 匹配完成之后, $`的内容为”a”, $&的内容为”bcd”, $’的内容为”e”. 

《Learning Perl(Perl语言入门)》中介绍了一个用于测试正则表达式结果的程序:

	While(<>){                              # take one input line at a time
		chomp;
		if(/YOUR_PATTERN_GOES_HERE/){
			print “Matched: |$`<$&>$’|\n”;#the special match vars
		} else {
			print “No match: |$_|\n”;
		}
	}
	
这个程序结构值得好好分析, 这是Perl做文本处理的一个经典结构. 首先是while(<>)部分, “<>”在Perl里面叫做钻石符, 就是shell命令行里面输入重定向符’<’和输出重定向符’>’的结合. 在这个结构中, while(<>)会把每一行的STDIN(默认情况下是键盘输入, 如果有文件重定向的话那就是文件中的每一行文本内容)读取到$_中, print的内容会输出到STDOUT(默认就是console, 如果有文件重定向那就输出到文件).

chomp是Perl的内置函数, 作用是把参数中最后的”\n”去掉, 这里省略参数的情况下相当于是”$_ = chomp($_)”的操作.

后面的if(/YOUR_PATTERN_GOES_HERE/)前面提到过了, 是m表达式的简写操作. 在匹配成功分支, 会显示出|匹配前文本<匹配内容文本>匹配后文本|这段内容.

分组捕获变量的编号对应规则跟正则表达式中的反向引用编号规则一样.


用S表达式做替换

s表达式是Perl使用正则表达式做文本处理的最直接工具, 用s表达式做替换的标准格式是:

	$text =~ s/regex/replacement/modifiers

在运行完s表达式之后, $text中对regex匹配的部分会替换成replacement. 同样的, 简写形式:

	s/regex/replacement/modifiers

是更常用也更常见的形式. 


测试工具

同样, 在学习s表达式的过程中, 建议大家使用测试工具进行实时的联系. 如果没有网络环境, 可以使用命令行工具.

这次推荐大家直接在命令行使用Perl命令:

	perl -ple ‘s/regex/replacement/modifiers’

把具体的s表达式写进单引号内, 后面每输入一行, 下一行就会输出s表达式的替换结果,  如果没有匹配成功的话, 下一行会输出同样的文本内容.

	zcr@~ %perl -ple ‘s/barney/Fred/i’
	barney
	Fred
	Barney
	Fred
	banana
	banana
	He’s out bowling with Barney tonight.
	He’s out bowling with Fred tonight.
	
在上面的例子中, 4次输入分别是”barney”, “Barney”, “banana”, “He’s out bowling with Barney tonight”.

你可能会对选项-ple感到好奇, 不过这个是下一章【在命令行使用Perl】的内容, 这里就暂且不说明了.


模式定界符

s表达式也支持定义的定界符, 使用单目符号跟m表达式一样:

	s!...!...!
	s,...,...,
	s#...#...#
	s|...|...| 

也可以使用括号, 不过需要用2组:

	s{...}{...} 
	m<...><...>
	m[...][...]
	m(...)(...)


使用匹配特殊变量

在s表达式中的replacement部分可以直接使用前一节介绍过的特殊变量, 比如:

	s/\bJohn\b/$&son/

可以把”John”替换成”Johnson”,

	s/(\w+) (\w+)/$2 $1/

可以将用空格隔开的两个标识符交换一下顺序. 


模式选项

在m表达式中提到的匹配选项, s表达式中也可以全部使用, 这些选项也可以组合使用. Perl也专门为s表达式添加了额外的选项, 这里介绍/g选项和/e选项.

默认情况下, s表达式只会对文本中的第一个匹配进行替换操作, 如果使用了/g选项的话, s表达式就会对文本的中所有匹配进行替换.

	$_ = “Input  data\t may have    extra whitespace.”;
	s/\s+/ /g; #Now it says “Input data may have extra whitespace.”

这个例子里使用/g的特性, 把所有连续的多个空格(包括tab)替换成单个空格.

/e选项会将replacement的内容作为eval的参数调用eval, 用其结果进行替换. 也就是说, replacement可以是简单的文本, 加了/e选项之后, replacement是可执行的代码, 里面可以执行运算, 可以调用函数, 这是一个上限非常高的特性.

下面这个例子可以实现文本中rsv0, rsv1, ...这种字段的重新编号:

	s/(rsv)\d*/”$1”.$i++/ge

每次匹配, s表达式会对”$1”.$i++进行运行, 生成rsv0, rsv1, ...这个序列, 然后进行替换. 

下面这个例子:

	s/-time-/localtime/ge

对每个”-time-”匹配后调用localtime函数, 然后替换, 这个是一些根据模板配置生成文件的工具里的常用做法.

/e选项甚至可以多次使用:

	s/(\$[a-zA-Z_]\w*)/$1/gee

在这个例子中, 看正则表达式部分, 可以看出这个可以匹配一个Perl中的scalar变量(这是我们在【匹配字符限定符里】这一节里面提到过). 对$1进行一个eval求值, 会得到这个scalar本身, 再进行一次求值, 会得到这个scalar变量的具体的值, 然后对匹配的文本内容进行替换. 



四、在命令行使用Perl

Perl one-liner就是在命令行使用的单行命令, 这是命令行上, perl除了运行perl脚本之外的用法. 在你掌握了Perl基础语法和正则表达式之后, 再加上一点点Perl命令行选项的知识和一些特殊变量的知识, 你会发现Perl one-liner是非常强大的工具. 


基本命令行选项和特殊变量

我们会通过一些基本的例子来解释常用的命令行选项和特殊变量, 至于剩余的命令行选项和特殊变量, 请参考Perl doc.


-e

我们先来用”Hello World”来暖场吧:

	perl -e ‘print “Hello World!\n”’
	
这个命令可以再命令行打印出Hello World!, 还有一个换行符.

所以, -e的意思就是用perl执行-e选项后面跟着的文本表示的代码.


-l

如果想在使用print的时候进行换行, 但是又不想每次都加上\n, 你可以加上-l选项:

	perl -l -e ‘print “Hello World!”’

命令行的选项可以合并:

	perl -le ‘print “Hello World!”’


$\

$\变量叫做输出分隔(output record separator), 默认值是undef, 是默认加在print最后的内容. 所以上面的例子可以使用:

	perl -e ‘$\=”\n”; print “Hello World!”’

当然$\也可以是其他内容, 可以试试:

	perl -e ‘$\=”#\n”; foreach $i(1..10) {print $i;}’


-p

我们在s表达式中提到的测试工具:

	perl -ple ‘s/regex/replacement/modifiers’

这里的-p选项, 会展开为代码:

-e选项的代码会放在while循环当中, 所以, 这个例子里的实际代码展开来就是:

	LINE:
	While (<>){
		$\ = “\n”;
		s/regex/replacement/modifiers;
	} continue {
		Print or die “-p destination: $!\n”;
	}

这个选项已经可以指定STDIN和STDOUT了, 因此可以使用:

	perl -ple ‘s/regex/replacement/modifiers’ file

来对实际的file的文本进行s表达式替换操作. 使用:

	perl -ple ‘s/regex/replacement/modifiers’ file > outfile

把替换的文本内容输出的文件outfile中. 有了这个选项之后, 你就会发现你现在已经可以把Perl one-liner当做sed来用了.

下面的代码:

	perl -lpe ‘eval’

可以生成一个perl交互式解释器了, 不过比较简陋, 没有错误提示, 一次也只能解释一行代码. 大家可以考虑考虑怎么让它变得更强大.


-i

如果想直接在file文件里面进行文本替换, 可以加上-i选项:

	perl -iple ‘s/regex/replacement/modifiers’ file

由于这种操作比较危险, 可以用-i’.bak’这种形式:

	perl -i’.bak’ -ple ‘s/regex/replacement/modifiers’ file

生成一个带.bak后缀的备份文件(在这里就是file.bak了).


-n

-n选项扩展出来的代码是:

	LINE:
	While (<>){
		...				# yours program goes here
	}

结合一些正则表达式:

	perl -nle ‘print if /regex/’

你会发现Perl one-liner可以当做grep工具来用.


$.

$.可以实时记录while(<>)中当前的行号, 这个功能其实自已用一个变量实现也可以, 不过用$.的话更简单.

	perl -pe '$_ = "$. $_"'

上面的命令可以为文件进行行编号, 如果如要对编号与文本做对齐的话, 可以用命令:

	perl -ne 'printf "%-5d %s", $., $_'

BEGIN和END

在-p或者-n选项下, BEGIN{...}和END{...}生成:

	BEGIN {
		...
	}
	While(<>) {
		...
	}
	END {
		...
	}
	
这样的代码. 一般用BEGIN块来写一些初始化的配置, END块中写一些总结性的结果.

比如:

	perl -ple ‘BEGIN{$\ = “\n”}’

可以实现在每一行后面添加额外的空行.

	perl -nle ‘END{print $.}’ file

可以统计出文件有多少行内容.


-a, -F和@F

下面要讨论的是在Perl one-liner里进行类似awk的操作.

在-pe或-ne选项之外加入-a, 会在while循环中加入代码:

	While(<>){
		@F = split(‘ ’);
		...
	}

就是说用空格对每一行(也就是$_)进行域分割, 然后存进列表@F里, 后面就可以用@F来进行数据处理了.
比如:

	zcr@~ %perl -a -nle ‘print join “ ”, reverse @F’
	a b c d e 
	e d c b a 
	1 2 3 4 
	4 3 2 1
	Mon Tur Wed Thu Fri Sat Sun
	Sun Sat Fri Thu Wed Tur Mon

可以对空格隔开的文本进行倒序处理.

跟awk一样, Perl也支持自定义的分隔符, 用-F指定: 

	perl -a -F’pattern’ -pe ‘...’
	
-F指定的分隔符会成为上面while循环中split的参数, 因为split是支持用正则表达式做分隔符的, 所有这里的pattern也可以是正则表达式.


-M

加上-M选项可以使用Perl module中的代码, 比如:

	perl -MList::Util=max -alne 'print max @F'
	perl -MList::Util=min -alne 'print min @F'

可以调用List::Util中的max和min函数, 用来求出每一行数据中的最大值和最小值.


典型应用摘录

多看看别人写的Perl one-liner代码也是很有益的积累, 本节选择性的摘录一些《PERL ONE-LINERS》中的常用例子, 希望可以让大家得到启发. 另外这个项目在https://github.com/pkrumins/perl1line.txt上开源, 大家可以在这个链接上获取最新的更新.


文件 SPACING 

对一个文件的每行使用两个换行符:

	perl -pe '$\="\n"'
	perl -pe 'BEGIN { $\="\n" }'
	perl -pe '$_ .= "\n"'
	perl -pe 's/$/\n/'

除空行以外,对文件的每行使用两个换行符:

	perl -pe '$_ .= "\n" unless /^$/'
	perl -pe '$_ .= "\n" if /\S/'

去掉所有空行:

	perl -ne 'print unless /^$/'
	perl -lne 'print if length'
	perl -ne 'print if /\S/'

对一个文件的每 10 行,都使用 Tab 键分隔开:

	perl -lpe '$\ = $. % 10 ? "\t" : "\n"'


行号
给文件的每行都加上行号

	perl -pe '$_ = "$. $_"'

给文件的非空行加上行号:

	perl -pe '$_ = ++$a." $_" if /./'

给非空白行加上行号并打印(丢掉空行):

	perl -ne 'print ++$a." $_" if /./'

给所有行都加上行号,但只打印非空行的行号:

	perl -pe '$_ = "$. $_" if /./'

只给与某个正则匹配的行加上行号,打印其它未修改的:

	perl -pe '$_ = ++$a." $_" if /regex/'

打印只包含某个正则的行,并在它们行首顺序添加行号:

	perl -ne 'print ++$a." $_" if /regex/'

给与正则匹配的行加上行号并打印:

	perl -pe '$_ = "$. $_" if /regex/'

给所有行使用指定的格式添加行号(模拟 cat -n):

	perl -ne 'printf "%-5d %s", $., $_'

打印一个文件的总行数(模拟 wc -l):

	perl -lne 'END { print $. }'
	perl -le 'print $n=()=<>'
	perl -le 'print scalar(()=<>)'
	perl -le 'print scalar(@foo=<>)'
	perl -ne '}{print $.'

打印一个文件非空白行的总和:

	perl -le 'print scalar(grep{/./}<>)'
	perl -le 'print ~~grep{/./}<>'
	perl -le 'print~~grep/./,<>'

打印一个文件空白行的总和:

	perl -lne '$a++ if /^$/; END {print $a+0}'
	perl -le 'print scalar(grep{/^$/}<>)'
	perl -le 'print ~~grep{/^$/}<>'

打印一个文件里匹配某个正则的行的总数(模拟 grep -c):

	perl -lne '$a++ if /regex/; END {print $a+0}'


计算

判断一个数是否是质数:

	perl -lne '(1x$_) !~ /^1?$|^(11+?)\1+$/ && print "$_ is prime"'

对一行的所有字段求和:

	perl -MList::Util=sum -alne 'print sum @F'

对所有行的所有字段求和:

	perl -MList::Util=sum -alne 'push @S,@F; END { print sum @S }'
	perl -MList::Util=sum -alne '$s += sum @F; END { print $s }'

在每行行首前打印该行总的字段和:

	perl -alne 'print scalar @F, " $_"'

打印匹配某个正则的字段总个数:

	perl -alne 'map { /regex/ && $t++ } @F; END { print $t }'
	perl -alne '$t += /regex/ for @F; END { print $t }'
	perl -alne '$t += grep /regex/, @F; END { print $t }'

打印匹配某个正则的总行数:

	perl -lne '/regex/ && $t++; END { print $t }'

在每行的行首加上时间戳(格林威治时间，本地时间):

	perl -ne 'print scalar gmtime," ",$_'
	perl -ne 'print scalar localtime," ",$_'


文本转换和替换

将所有文本转换为大写格式:

	perl -nle 'print uc'
	perl -ple '$_=uc'
	perl -nle 'print "\U$_"'

将所有文本转换为小写格式:

	perl -nle 'print lc'
	perl -ple '$_=lc'
	perl -nle 'print "\L$_"'

对每一行的首字母大写:

	perl -nle 'print ucfirst lc'
	perl -nle 'print "\u\L$_"'

反转字母的大小写:

	perl -ple 'y/A-Za-z/a-zA-Z/'

使用骆驼规则处理每行:

	perl -ple 's/(\w+)/\u$1/g'
	perl -ple 's/(?<!['])(\w+)/\u\1/g'

丢掉行首的空白字符(空白符，制表符):

	perl -ple 's/^[ \t]+//'
	perl -ple 's/^\s+//'

丢掉行尾的空白字符(空白符，制表符):

	perl -ple 's/[ \t]+$//'

丢掉行首和行尾的空白符:

	perl -ple 's/^[ \t]+|[ \t]+$//g'

将 UNIX 新行转换成 DOS/Windows 格式新行:

	perl -pe 's|\n|\r\n|'

将 DOS/Windows 格式的新行转换成 UNIX 格式的新行:

	perl -pe 's|\r\n|\n|'

转换 UNIX 格式新行到 Mac 格式新行:

	perl -pe 's|\n|\r|'

当一行中出现 "baz" 时,使用 "foo" 替换(查找并替换)最开始的一个 "bar":

	perl -pe '/baz/ && s/foo/bar/'


选择性的打印和删除某些行

打印文件的第一行(模拟 head -1):

	perl -ne 'print; exit'

打印文件的前十行(模拟 head -10):

	perl -ne 'print if $. <= 10'
	perl -ne '$. <= 10 && print'
	perl -ne 'print if 1..10'

打印文件的最后一行(模拟 tail -1):

	perl -ne '$last = $_; END { print $last }'
	perl -ne 'print if eof'

打印文件的最后十行(模拟 tail -10):

	perl -ne 'push @a, $_; @a = @a[@a-10..$#a]; END { print @a }'

只打印匹配某个正则的行:

	perl -ne '/regex/ && print'

只打印不匹配某个正则的行:

	perl -ne '!/regex/ && print'

打印匹配某个正则的前一行:

	perl -ne '/regex/ && $last && print $last; $last = $_'

打印匹配某个正则的后一行:

	perl -ne 'if ($p) { print; $p = 0 } $p++ if /regex/'

打印同时包含 AAA 和 BBB 的行:

	perl -ne '/AAA/ && /BBB/ && print'

打印既不包含 AAA 也不包含 BBB 的行:

	perl -ne '!/AAA/ && !/BBB/ && print'

打印顺序包含 AAA, BBB, CCC 的行:

	perl -ne '/AAA.*BBB.*CCC/ && print'

打印长度不小于 80 个字符的行:

	perl -ne 'print if length >= 80'

打印长度小于 80 个字符的行:

	perl -ne 'print if length < 80'

只显示第 13 行:

	perl -ne '$. == 13 && print && exit'

打印除了第 27 行外的所有行:

	perl -ne '$. != 27 && print'
	perl -ne 'print if $. != 27'

只打印第 13,19,67 行:

	perl -ne 'print if $. == 13 || $. == 19 || $. == 67'
	perl -ne 'print if int($.) ~~ (13, 19, 67)' 

打印匹配两个正则间的所有行(包括匹配行本身):

	perl -ne 'print if /regex1/../regex2/'

打印第 17 到 30 行间的所有行:

	perl -ne 'print if $. >= 17 && $. <= 30'
	perl -ne 'print if int($.) ~~ (17..30)'
	perl -ne 'print if grep { $_ == $. } 17..30'

打印最长行:

	perl -ne '$l = $_ if length($_) > length($l); END { print $l }'

打印包含数字的行:

	perl -ne 'print if /\d/'

查找只包含数字的行:

	perl -ne 'print if /^\d+$/'

从文件首行开始,每两行打印一次:

	perl -ne 'print if $. % 2'

从第二行开始,每两行打印一次:

	perl -ne 'print if $. % 2 == 0'

打印重复出现的行:

	perl -ne 'print if ++$a{$_} == 2'

打印所有唯一的行:

	perl -ne 'print unless $a{$_}++'


管道应用

既然是在命令行的使用, Perl one-liner自然也是可以跟shell管道结合使用的. 比如:

	find ... | xargs perl ...

先用find命令查找出文件, 再跟着用perl命令对这些文件进行文本处理, 这是非常常见的用法.

此外, Perl one-liner虽然很强大, 很复杂的功能可以写到一行, 不过很多时候, 如果你把复杂的功能分解一下:

	perl ... | perl ... | perl ...

使用这种形式来操作, 一步一步的慢慢处理, 其实是更好的方案.

此外, 在gvim里面可以使用管道来使用Perl one-liner来进行文本处理. 比如, 前面章节我们提到过:

	s/(rsv)\d*/”$1”.$i++/ge

可以用来对rsv域进行重新编号. 现在我们用gvim打开的文件的内容如下:

	rsv
	rsv3rsv3 rsv3
	rsv1
	rsv10
	rsv3

我们使用选择模式选中这段文本.

然后敲入命令:

	:!perl -ple ‘s/(rsv)\d*/”$1”.$i++/ge’

然后回车, 这段文本就变成了:

	rsv0
	rsv1rsv2 rsv3
	rsv4
	rsv5
	rsv6



Reference

[1]. Learning Perl(Perl语言入门), Randal L. Schwartz, brian d foy & Tom Phoenix

[2]. Intermediate Perl(Perl进阶), Randal L. Schwartz, brian d foy & Tom Phoenix

[3]. Mastering Perl(精通Perl), Randal L. Schwartz, brian d foy & Tom Phoenix

[4]. Mastering Regular Expression, Jeffrey Freidl

[5]. PERL ONE-LINERS, Peteris Krumins

[6]. Perl doc, perldoc.perl.org

