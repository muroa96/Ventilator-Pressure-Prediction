## Kaggle Competition - Google Brain - Ventilator Pressure Prediction

--------------------

#### Description

> Ventilator란 인공호흡기로서 호흡 곤란 등의 환자들에게 사용되는 의료 기구이다. 허나 Ventilator은 의료진들의 지속적인 모니터링이 필요한 기구이다. 현재 코로나로 인한 의료진 인력 부족은 Ventilator에 있어서 큰 단점으로 작용한다. 
>
> 본 대회는 Ventilator의 압력을 예측하는 대회이다. 이로 인해 Ventilator에 해당되는 의료진의 시간소모가 줄어들 것으로 사료된다. 더하여, Ventilator의 정확도에도 긍정적인 영향을 끼칠 것으로 보여진다.



#### Team

* Hanjong Son
* Hunsoo Jung
* Gahyun Son
* Eunsu Na
* Jinsoo Yoon



#### Files

* train.csv - the training set
* test.csv - the test set
* sample_submission.csv - a sample submission file in the correct format



#### Columns

* id
* breath_id
* R
* C
* time_step
* u_in
* u_out
* pressure



#### Result

#### ![image-20220119165013227](C:/Users/thsgs/AppData/Roaming/Typora/typora-user-images/image-20220119165013227.png)

1358/2605



#### Discussion

----

한 달 정도 진행한 프로젝트는 머신러닝을 배운 뒤 첫 프로젝트였던 만큼 그 의미가 컸다. 당시 배우지 않았던 LSTM 을 활용한 이번 프로젝트는 실력 향상에 큰 도움이 되었다고 생각한다. 하지만 그럼에도 높은 점수를 획득하지 못한 점은 상당히 아쉬웠다. 부족한 부분 및 고찰은 다음과 같다.

1. Lack of Medical Knowledge(feature tuning)

   Kaggle 대회의 특징상 Feature Tuning이 매우 중요하다. 특히나 해당 대회의 경우 부가적인 feature이 많지 않았다. 하지만 의료적인 주제의 대회인 만큼, 해당 분야의 지식이 모자랐다. 이로 인해 조금 더 효과적인 feature tuning에 어려움을 겪게 되었다.

2. Time Shortage(hyper parameter tuning, modeling)

   Kaggle Data의 경우 전처리가 거의 필요하지 않다. 그럼에도 시간 부족을 느낀 가장 큰 원인은 모델을 돌리는 시간이다. 당시 XG Boost, Light GBM 등 다양한 모델을 돌려보았다. 그 결과 LSTM으로 모델 선정을 한 뒤에도, 파라미터 튜닝 및 모델링을 하는 데 있어 많은 시간이 소요되었다. 특히 LSTM의 경우 한 모델을 돌리는 데 10시간이 소요되기도 하였다. 

