# Notes on Python Data Science Handbook

[Python Data Science Handbook](https://github.com/yaxing0zhao/PythonDataScienceHandbook/tree/master/notebooks)

## ipython

### 01:00
ipython, jupyter

### 01:01
`sum?`

### 01:02
shortcuts: ctrl+l:Clear terminal screen

### 01:03
**magic commands**: `%paste, %run pyscirpt.py, %timeit, %lsmagic `

### 01:04
`%history`

### 01:05
`!`

### 01:06
`%xmode, %debug, %pdb`

### 01:07

- `%time`: Time the execution of a single statement

- `%timeit`: Time repeated execution of a single statement for more accuracy

- `%prun`: Run code with the profiler

- `%lprun`: Run code with the line-by-line profiler

- `%memit`: Measure the memory use of a single statement

- `%mprun`: Run code with the line-by-line memory profiler

  

## NumPy

### 02:01
批量创建**array**

### 02:02
 array操作，子集，`copy，reshape，concatenate (cbind, rbind, append), splitting: vsplit, hsplit.`

### 02:03
NumPy 中向量化操作，各种数学运算，减少使用functions和loop。

### 02:04
统计运算，NumPy中函数比python自带函数要快！array上的统计运算。

### 02:05
array向量间操作。

### 02:06
array逻辑操作，是否，比较

### 02:07
fancy index: 批量选取子集 `list[idx], array[row_idx, col_idx]`, 各种选取方法……

### 02:08
sorting array：排序及部分排序

### 02:09
structured array: similar to dataframe in pandas



## Pandas

### 03:01 
**series and dataframe** 创建, index, `df1.shape()`(dim(df1))

### 03:02
series and dataframe 子集选取`df1.iloc[:nrow, :ncol], df1[colname]`

### 03:03
dataframe 数学运算，自动对齐或产生NA, `a.add(b, fill_value=fill)` 。

### 03:04
missing value: `np.nan(),df1.isnull(),df1.notnull(), df1.ffill(), df1.bfill(),df1.droupna(axis = 'colums')`

### 03:05
multi-index: dataframe 🔛series by `stack()`, multi-index dataframe 取子集时index must be sorted. `reset_index() `相当于melt: multi-index to index, `reverse is set_index()`.

### 03:06
df combination: np.concatenate( see 02:02), `pd.concat(df1, df2)`: 参数选项类似mySQL。`df1.append(df2)`类似rbind()

### 03:07
merge and join: `pd.merge(df1,df2, left_on='keyword1', right_on='keyword2', on='keyword3', suffixes=["_L", "_R"])'), df1.join(df2)` 相当于SQL中的join。

### 03:08
groupby: `df1.mean(axis='columns')`, `df1.describe() `,`df1.groupby('key').sum(), df1.groupby('key').aggregate(['min', np.median, max]), df1.groupby('key').apply(fun),`,  `filter(), transform() and apply()`:类似apply in R. `df1.groupby(mapping).sum()`: replace a_idx with b_idx.

### 03:09
pivot table: 多变量groupby 的简化版。`df1.pivot_table(data, values=None, index=None, columns=None, aggfunc={'survived':sum, 'fare':'mean'}, fill_value=None, margins=False, dropna=True, margins_name='All')` `pivot_table(), pd.cut()`, ***应用实例***。

### 03:10
string：文本操作和R类似功能，`mystr.str.len()` ***应用实例***。

### 03:11
time; pd.datatime and pd.datautil, pd.tseries.offsets module. Np.array(), ***应用实例***。

### 03:12
**high-performance**: numexpr.evaluate() for compound expression, `pd.eval()` is faster. `Query()` for filter operation.



## Matplotlib

### 04:01
matplotlib: style, `put.show() `只在末尾一次就好。`fig.save fig(filename.png).` 多图布局。

### 04:02
lineplot: 坐标轴，图例

### 04:03
scatter plot: 大数据首选`plt.plot()`.

### 04:04
error bar: 包括连续error。

### 04:05
密度图和轮廓图。

### 04:10
修改坐标轴

### 04:14
**seaborn** 主题画图更美观，用它！



## ML

### 05:02
array: sample * feature. Target col is the predicted class/feature. **ML的基本步骤**：import/instantiate/fit/predict. Linear regression, GaussianNB, across-validation, PCA, GMM cluster, hand-written digits, Isomap (dimensionality reduction) 实例。

### 05:03
**cross-validation**， validation-curve, learning_curve

### 05:04
feature engineering: categorical, text, image, derived features, missing value imputation.

### 05:05
naive bayes: multi-NB

### 05:06
linear regression, regularization

### 05:07
SVA

### 05:08
RF

### 05:09
PCA: tends to be highly affected by outliers, `RandomizedPCA` and `SparsePCA`

### 05:10
manifold learning: multidimensional scaling (MDS), locally linear embedding (LLE), and isometric mapping (IsoMap).

### 05:11
k-means

### 05:12
gaussian mixtures

### 05:13
kernel density estimation

### 05:14
image features
