导入熊猫作为PD
从集合导入计数器

# 加载数据
文件的路径，使用值=【'期号'，'前区1', '前区2', '前区3', '前区4', '前区5'])['期号', '前区1', '前区2', '前区3', '前区4', '前区5'])

# 提取前区号码并计算每个号码的出现次数
front_numbers = df[['前区1', '前区2', '前区3', '前区4', '前区5']stack_reset_index_文件的格式['前区1', '前区2', '前区3', '前区4', '前区5']stack_reset_index_文件的格式
front_numbers.columns = ['期号', '号码']
number_counts=前面的数字['号码'].数值计数（）

# 计算每个号码的遗漏期数（这里简化处理，仅计算从最后一期到当前的遗漏）
最后一次抽奖=df.iloc[-1]['期号']
current_period = last_draw  # 假设当前是最后一期的下一期，即第81期
缺失_周期=（当前_周期-前面_数字）['期号']）替换（0：浮点数）

# 选择出现次数最多和遗漏期数较少的号码
top_numbers=数字的数量.head（5）
低_缺失_数字=缺失_句点[缺失_周期<5].索引目录（）

# 综合考虑出现次数和遗漏期数，选择5组号码
推荐的_组合=【】
对于_在范围（5）:
组合=
对于_在范围（5）:
        # 优先选择出现次数多且遗漏期数少的号码
数字=顶部数字[0]如果top_numbers其他低_missing_numbers[0]
附件（数量）
        # 从候选列表中移除已选择的号码
top_numbers.pop（0）如果是top_numbers中的数字，则为low_missing_numbers.pop（0）
recommended_combinations.append（组合）

# 打印5组推荐号码
对于i，枚举中的组合（recommended_combinations）:
打印（f"组合：组合”)(f"组合：组合”)
