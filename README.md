# zuihouyicishiyan
# 实验五 模拟学生作业处理
# 实验目的  
1.掌握字符串String及其方法的使用  
2.掌握文件的读取/写入方法  
3.掌握异常处理结构
# 实验要求
1.设计学生类（可利用之前的）；  
2.采用交互式方式实例化学生；  
3.利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能方法，实现如下功能：  
1.每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”  
2.允许提供输入参数，统计古诗中某个字或词出现的次数  
3.输入的文本来源于文本文件B读取，把处理好的结果写入到文本文件A  
4.考虑操作中可能出现的异常，在程序中设计异常处理程序  
5.设计程序完成上述的业务逻辑处理，并且把“古诗处理后的输出”结果存储到学生基本信息所在的文本文件A中。
# 实验过程  
1.先设计学生类，对姓名，性别，学号，年龄等变量初始化  

# 核心代码  
        File sourcefile = new File("D://实验1.txt");  
        File targetFile = new File("D://作业.txt");  
        char b[] = new char[100];  
        String original = null;  
        int n = -1;  
        StringBuffer sb = new StringBuffer(); 
        try {  
            File file = new File("D://实验1.txt");  
            InputStream c = new FileInputStream(file);  
            InputStreamReader in = new InputStreamReader(c, "GBK");  
            Writer out = new FileWriter(targetFile,true);  
            while ((n = in.read(b, 0, 100)) != -1) {  
                String s = new String(b,0,n);   
                if(original!=null)   
                    original = original+s;   
                else original =s;  
            }  
            in.close();  
        }  
# 实验总结






