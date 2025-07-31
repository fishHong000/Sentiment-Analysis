# Sentiment-Analysis

本次作業為情緒分析

有開設 Kaggle 非正式競賽供同學評估模型使用，Kaggle 分數不會列入作業成績

HW2 Kaggle 網址：https://www.kaggle.com/t/3d90c24a5d754706833a49b7842739a9


請先下載資料集 Reviews.csv：https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews

作業流程：

1.       資料前處理


         1.1      讀取 csv 檔後取前 1 萬筆資料，僅保留 "Text"、"Score" 兩個欄位


                  ●      將 "Score" 欄位內值大於等於 4 的轉成 1，其餘轉成 0 (1: positive 0: negative)

                  ●      將 "Text" 欄位內的文字利用分割符號切割

         1.2      去除停頓詞stop words ，可參考：
                  ●      sklearn.feature_extraction.text.CountVectorizer

                  ●      自訂stop words

         1.3      文字探勘前處理，將文字轉換成向量，請實作 tf-idf 及 word2vec 並進行比較，可參考：

                  ●      sklearn.feature_extraction.text.TfidfVectorizer

                  ●      Word2vec

2.          建模：使用 Random forest 進行分類

3.          評估模型：進行 k-fold cross-validation 並計算 k=4 的 Accuracy，上傳程式碼與報告
