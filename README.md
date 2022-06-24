# The-longest-word
给定一组单词words，编写一个程序，找出其中的最长单词，且该单词由这组单词中的其他单词组合而成。若有多个长度相同的结果，返回其中字典序最小的一项，若没有符合要求的单词则返回空字符串。  来源：力扣（LeetCode

Arrays.sort(words, (a, b) -> (a.length() == b.length() ? (a + b).compareTo(b + a) : b.length() - a.length()));
1. Arrays.sort(a,b) : 将a 按照b的规则进行排序；
2. (a,b) ->  ：定义排序规则,整数交换b和a, 负数不变；
3. (a + b).compareTo(b + a);  ： 串联a+b 和 b+a 保证字符长度相等的时候比较ASC码，当a+b 的 ASC码 大于b+a的ASC码的时候返回正数，

Set<String> set = new HashSet<>(Arrays.asList(words));
Arrays.asList()  ：将输入转换为静态变量可以直接生成列表；

