# BurgerExam
简易测验系统，利用 JSON 来存储测验数据，简单修改即可制作自己的小测验。
# 主要功能
- [x] 自动从 JSON 获取测验数据
- [x] 测验时间限制（倒计时）
- [x] 每次切换题目，即时记录对错
- [x] 输入序号可直接跳转到相应题目
- [x] 提交后立即计算得分，并给出错题分析
- [x] 可切换日间/夜间模式，在浏览器本地存储此设置
- [x] 每次测验结束后记录结果数据
- [x] 可在页面中嵌入自定义代码
# 使用方法  
简单了解 JSON 语法，克隆本仓库并修改其中的 exam.json：
![exam.json 示例](https://bgexam.netlify.app/Screenshot_20230604_172110_bin.mt.plus.jpg)
- title：测验标题
- description：测验描述，在答题前显示
- time：测验限时（单位：秒）
- questions[n].question：一道题的题目
- questions[n].answer：一道题的正确解答（若有多个正确解答，把它编辑为数组即可，如 ["答案1", "答案2"]）
- questions[n].resolve：一道题的答案解析
- customer：页面中的自定义 HTML 代码，显示在卡片下方
- 若要添加/移除题目，只需添加/移除 questions 数组中的对象。此数组中对象的顺序即为答题时题目的顺序。
- 除 time 外，每个对象的值都可包含 HTML 代码，但注意不要与其外的半角双引号产生冲突。
- 将修改后的代码部署到服务器，访问索引页即可看到效果。