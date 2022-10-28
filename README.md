# vLoong-competion
## 竞赛第7名技术方案
微雨梦寒的团队  A 榜 score: 0.8641

## 比赛描述
> 本赛题旨在更好地检验电池安全问题，促进智慧能源领域技术发展，比赛募集到的优秀异常检测方案，将应用于车辆预警、故障模式识别等多种场景。

## 关键词：
时序特征，集成模型, automl

## 项目结构

```
-|1. 特征构建.ipynb              构建时序特征文件
-|2. 使用automl模型.ipynb   使用automl模型对构建的特征进行学习
-|3. 模型结果融合.ipynb        对多种模型得到的结果加权融合
-|总程序.ipynb                      去除废弃方案后的精简总程序，看这个就行
-|extracted_train_features.pkl  提取的train数据时序特征
-|extracted_test_features.pkl    提取的test数据时序特征
-README.MD
```
 (所有模型文件数据均在云盘中：https://share.weiyun.com/vj56LU5c ，精简后的： https://share.weiyun.com/ZHDBXlrk）
## 使用方式
> 请提前准备package: lightgbm,xgboost,sklearn,numpy,tsfresh ( 时序特征提取工具），imblearn( 不均衡数据处理），mljar-supervised (automl算法，https://github.com/mljar/mljar-supervised)

### 实验tips
- [ ] GRU, GRU-FCN等深度学习模型尝试效果一般。
- [ ] lightgbm模型效果最好，单一使用不调参就可以达到0.86。
- [ ] 对不均衡数据使用imblearn的random oversampling 效果会有好的提升。
- [ ] 对多种模型得到的结果加权融合效果提升很有限。
- [ ] automl工具提升效果有限，直接lightgbm 就行。
