# 第三课 t检验

**Z-test works when we konw the μ and the σ.**



### t 分布（t-distribution）

在概率论和统计学中，学生**t-分布**（*t*-distribution），可简称为*t*分布，用于根据小样本来估计呈正态分布且**方差未知**的总体的均值。如果总体方差已知（例如在样本数量足够多时），则应该用正态分布来估计总体均值.

t分布曲线形态与n（确切地说与自由度df）大小有关。与标准正态分布曲线相比，自由度df越小，t分布曲线愈平坦，曲线中间愈低，曲线双侧尾部翘得愈高；自由度df愈大，t分布曲线愈接近正态分布曲线，当自由度df=∞时，t分布曲线为标准正态分布曲线。



### 自由度（Degrees of freedom）

在统计学中，**自由度**(degree of freedom, df)指的是计算某一统计量时，取值不受限制的变量个数。通常df=n-k。其中n为样本数量，k为被限制的条件数或变量个数，或计算某一统计量时用到其它独立统计量的个数。自由度通常用于抽样分布中。



### t 分数（t-value）

### 单样本t检验（One-sample t-test）


$$
t = \frac{\bar{x}- μ_0}{s/\sqrt{n}}
$$


### P 值（p-value）

P值是用来判定假设检验结果的一个参数，也可以根据不同的分布使用分布的拒绝域进行比较。由R·A·Fisher首先提出。

P值（P value）就是当原假设为真时所得到的样本观察结果或更极端结果出现的概率。如果P值很小，说明原假设情况的发生的概率很小，而如果出现了，根据[小概率原理](https://baike.baidu.com/item/%E5%B0%8F%E6%A6%82%E7%8E%87%E5%8E%9F%E7%90%86)，我们就有理由拒绝原假设，P值越小，我们拒绝原假设的理由越充分。总之，P值越小，表明结果越显著。但是检验的结果究竟是“显著的”、“中度显著的”还是“高度显著的”需要我们自己根据P值的大小和实际问题来解决。



**Reject the null when the p-value is less than the σ-level.**



### Coren‘s D

**Cohen's d** is an [effect size](https://en.wikiversity.org/wiki/Effect_size) used to indicate the standardised difference between two means. It can be used, for example, to accompany reporting of [*t*-test](https://en.wikiversity.org/wiki/T-test) and [ANOVA](https://en.wikiversity.org/wiki/ANOVA) results. It is also widely used in [meta-analysis](https://en.wikiversity.org/wiki/Meta-analysis).



### 边界误差（Margin of error）

The margin of error for a particular statistic of interest is usually defined as the radius (or half the width) of the confidence interval for that statistic. The term can also be used to mean sampling error in general. In media reports of poll results, the term usually refers to the maximum margin of error for any percentage from that poll.



Margin of error = Coren's D * Standard Error





### 效应量（Effect Size）

效应量是指由于因素引起的差别，是衡量处理效应大小的指标。与显著性检验不同，**这些指标不受样本容量影响**。它表示不同处理下的总体均值之间差异的大小，可以在不同研究之间进行比较。平均值差异、方差分析解释比例、回归分析解释比例需要用效应量描述。效应量不受样本容量的影响。**当样本容量大得到显著时，有必要报告效应量大小。**



**常见的几种ES：**

a) 两个平均数间的标准差异；

b) 分组[自变量](https://baike.baidu.com/item/%E8%87%AA%E5%8F%98%E9%87%8F/6895256)与个体[因变量](https://baike.baidu.com/item/%E5%9B%A0%E5%8F%98%E9%87%8F/5872908)分数间的相关--相关效应大小。

c) [方差分析](https://baike.baidu.com/item/%E6%96%B9%E5%B7%AE%E5%88%86%E6%9E%90/1502206)中处理效应的效应大小





### 效应量的测量类型（Types of Effect Size Measures）

**Group 1: Differences measures**

- mean difference
- Standardised differences
- Cohen's d - SD units



**Group 2: Correlation measures**

- *r2* (r-squared) - proportion (%) of variation in one variable that is related (explained by) to another variable.



### 对比：统计的显著性（statictical siganificance）

it means：

- reject the null
- results are not likely due to chance ( sampling error )



it does not mean:

- important
- large or sizeable
- meaningful





### 怎么判定结果是否有意义

### （Meaningfulness of Results）

1、 What was measured?

Variables - practical, social, or theoretical importance



2、Effect Size



3、Can we rule out random chance？



4、Can we rule out alternative explanation? (lurking variables)





### Coren‘s D

**Cohen's d** is an [effect size](https://en.wikiversity.org/wiki/Effect_size) used to indicate the standardised difference between two means. It can be used, for example, to accompany reporting of [*t*-test](https://en.wikiversity.org/wiki/T-test) and [ANOVA](https://en.wikiversity.org/wiki/ANOVA) results. It is also widely used in [meta-analysis](https://en.wikiversity.org/wiki/Meta-analysis).



Standardized mean difference.
$$
d = \frac{\bar{x}-μ}{s}
$$


### Correlation measures: r-squared

R-squared - coefficient of determination

Range: [0.00, 1.00]
$$
r^2=\frac{t^2}{t^2+df}
$$


### （报告结果）Results Sections

**1、Descriptive Statistics（Mean、STD.）**

- in text
- in graphs
- in tables



**2、inferential statistics**

Hypothesis test (α)

- kind of test - one sample t test
- test statistic
- df
- p-value
- direction of test (one-tailed or two-tailed)



using APA style to write inferential statics, for example:

t(df) = x.xx, p = xx, direction



### one-sample t test(单一样本t检验)

- **variables**
- **treatment**
- **Null** hypothesis一般情况下都是变化前后的变量保持一致
- **Alternative** hypothesis一般情况下都是我们希望看到的情况
- **Types and directions** of the test单尾还是双尾检验；正向还是反向
- compute the **degree of freedom**
- compute the **t-critical** in a certain α. e.g α=0.05
- compute the **SEM** (standard error of the mean)
- compute the **mean difference**
- compute the **t statistics**
- Draw the **t-distribution**; Place t-critical on distribution; Shade the **critical region**; Place  t on t distribution;
- compute the **p-value**
- are these results **statistically siganificant?** - according to the p-value
- are these results **meaningful**?
- compute the **cohen's d**
- compute the **r-squared**
- compute the **margin of error** for XX% CI. e.g. for 95% CI
- compute the **confidence interval (CI)**







## 以上的总结(相互依赖样本)

**Dependent samples (Repeated measures and within-subject designs)**

- Two conditions
- Longitudinal
- Pre-test, post-test



its advantages:

- controls for individual differences
  - use fewer subjects
  - Cost-effective
  - less time-consuming
  - less expensive



its disadvantages:

- carry-over effects: second measurement can be affected by first treatment
- order may influence the results



## 接下来的讨论（独立样本）

**Independent samples(Between-subject designs)**

- Experimental
- Observational 



两个符合正态分布的数据集相差得到新的数据集依然符合正态分布：
$$
N（μ_1, σ_1）-N(μ_2, σ_2)=N（μ_1-μ_2, \sqrt{σ_1^2+σ_2^2}）
$$


Subtract two normally distributed samples:
$$
SD = \sqrt{S_1^2+S_2^2}
$$

$$
SE = \frac{S}{\sqrt{n}}=\frac{\sqrt{S_1^2+S_2^2}}{\sqrt{n}}=\sqrt{\frac{S_1^2+S_2^2}{n}}=\sqrt{\frac{S_1^2}{n_1}+\frac{S_2^2}{n_2}}
$$

$$
df=n_1+n_2-2
$$

$$
t-statistic = \frac{\bar{x}_1-\bar{x}_2}{SE}
$$



### Independent samples t-test assumptions

1、X and Y should be random samples from two independent populations.

2、Populations should be approximately normal.

3、Sample data can estimate population variances.

4、Population variances are roughly equal.



### 检验的类型

| 检验          |           目的           | 示例                                       |
| :---------- | :--------------------: | :--------------------------------------- |
| 单样本 t       |    检验单个总体的均值是否等于目标值    | 女大学生的平均身高是否大于 5.5 英尺？                    |
| 双样本 t       |  检验两个独立总体的均值之差是否等于目标值  | 女大学生的平均身高是否显著不同于男大学生的平均身高？               |
| 配对 t        | 检验相关或配对观测值之差的均值是否等于目标值 | 如果在每名男大学生服下减肥药前后测量受试对象的体重，平均体重减少量是否显著到足以断定减肥药起作用？ |
| 回归输出中的 t 检验 |  检验回归等式中的系数值是否显著不同于零   | 高中 SAT 考试分数是否是大学 GPA 的显著预测变量？            |

T 检验的一个重要属性是它对于总体正态性的假设十分可靠。换句话说，对于大样本，t 检验通常有效，即使违反了正态性假设也是如此。此属性使 t 检验成为就总体均值进行推断的最有用过程之一。

但是，对于样本数量较小的非正态且高度偏斜的分布，可能更适合使用非参数检验。



## Recap

### **Hypothesis Testing Basics**

**Statistical hypothesis tests are based a statement called the null hypothesis that assumes nothing interesting is going on between whatever variables you are testing. **The exact form of the null hypothesis varies from one type test to another: if you are testing whether groups differ, the null hypothesis states that the groups are the same. For instance, if you wanted to test whether the average age of voters in your home state differs from the national average, the null hypothesis would be that there is no difference between the average ages.

**The purpose of a hypothesis test is to determine whether the null hypothesis is likely to be true given sample data.** If there is little evidence against the null hypothesis given the data, you accept the null hypothesis. If the null hypothesis is unlikely given the data, you might reject the null in favor of the alternative hypothesis: that something interesting is going on. The exact form of the alternative hypothesis will depend on the specific test you are carrying out. 

Once you have the null and alternative hypothesis in hand, you choose a significance level (often denoted by the Greek letter α.). The significance level is a probability threshold that determines when you reject the null hypothesis. After carrying out a test, if the probability of getting a result as extreme as the one you observe due to chance is lower than the significance level, you reject the null hypothesis in favor of the alternative. This probability of seeing a result as extreme or more extreme than the one observed is known as the p-value.

The T-test is a statistical test used to determine whether a numeric data sample of differs significantly from the population or whether two samples differ from one another.



### One-Sample T-Test

A one-sample t-test checks **whether a sample mean differs from the population mean. **Let's create some dummy age data for the population of voters in the entire country and a sample of voters in Minnesota and test the whether the average age of voters Minnesota differs from the population.



### Two-Sample T-Test

A two-sample t-test investigates **whether the means of two independent data samples differ from one another. **In a two-sample test, the null hypothesis is that the means of both groups are the same. Unlike the one sample-test where we test against a known population parameter, the two sample test only involves sample means. You can conduct a two-sample t-test by passing with the stats.ttest_ind() function.



### Paired T-Test

The basic two sample t-test is designed for testing differences between independent groups. In some cases, you might be interested in **testing differences between samples of the same group at different points in time. **For instance, a hospital might want to test whether a weight-loss drug works by checking the weights of the same group patients before and after treatment. A paired t-test lets you check whether the means of samples from the same group differ.

[Reference][https://www.statsdirect.com/help/parametric_methods/paired_t.htm]



### Type I and Type II Error

The result of a statistical hypothesis test and the corresponding decision of whether to reject or accept the null hypothesis is not infallible. A test provides evidence for or against the null hypothesis and then you decide whether to accept or reject it based on that evidence, but the evidence may lack the strength to arrive at the correct conclusion. Incorrect conclusions made from hypothesis tests fall in one of two categories: [type I error and type II error](https://en.wikipedia.org/wiki/Type_I_and_type_II_errors).

**Type I error describes a situation where you reject the null hypothesis when it is actually true. **This type of error is also known as a "false positive" or "false hit". The type 1 error rate is equal to the significance level α, so setting a higher confidence level (and therefore lower alpha) reduces the chances of getting a false positive.

**Type II error describes a situation where you fail to reject the null hypothesis when it is actually false. **Type II error is also known as a "false negative" or "miss". The higher your confidence level, the more likely you are to make a type II error.



### Wrap Up

The t-test is a powerful tool for investigating the differences between sample and population means. **T-tests operate on numeric variables.**



### Index

[T-test using Python and Numpy][https://towardsdatascience.com/inferential-statistics-series-t-test-using-numpy-2718f8f9bf2f]

[Python for Data Analysis Part 24: Hypothesis Testing and the T-Test][https://hamelg.blogspot.jp/2015/11/python-for-data-analysis-part-24.html?view=sidebar]



