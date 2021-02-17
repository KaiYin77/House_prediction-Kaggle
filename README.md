# House prediction - R

目標：預測印第安納州房價

### 步驟： ###
  1.瀏覽dataset的各個變數並且製作了幾張圖。
  2.整理需要的data與變數。
  3.建立預測模組。

### ㄧ. ###
  1.先用read.csv讀取 train.csv test.csv。
  2.瀏覽data的時候：我們製作了三張圖。
    1.房子的月銷售長方圖以及房子年銷售長方圖。
    2.建造年份的數量圖。
    3.correlation圖，我們可以看出哪些變數與因素與房價之間的相關性。
### 二. ###
  1.首先，原資料裡面有兩種型態的變數integer以及character，我們先將character轉為factor以便建模使用。
    並將NA值以“None”取代。
  2.利用mice函數配合randomforest的方式將剩下的缺失值進行填補。
  3.資料準備好囉！
### 三. ###
   1.我們利用SVM(support vector machine)來預測房價。
  
  >svm簡介：library(e1071)package中。SVM的概念是讓資料區分成兩類，所以又被稱為二元分類器(binaryclassifier)。svm()中，有幾個參數需要注意，像是C(cost)。C愈小愈好。
   
   2.將預測結果輸出成team01.csv。
   3.上傳kaggle得知erro的rms為0.12089。

### 心得： ###
> 我們其實做了很多種prediction model，包括了linear model、random forest、嘗試去用xgboost但最後誤差太大，所以沒有採用。最後，我們用的是support vector machine，誤差相對小很多。經過這次的project後，我了解到團隊合作的重要，還有上網自學，查詢一些有用的function以及library，像是我們這次自己學了support vector machine，以及使用mice這個library。雖然做project很累，但這樣能檢視我們這一學期的所學和不足的地方。
