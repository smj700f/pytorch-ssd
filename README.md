# 訓練物件辨識
把物件辨識資料集dataset資料夾放在data資料夾

切換路徑
 >cd C:\Users\使用者名稱\pytorch-ssd\data

使用程式去分類資料集
 >python createData.py

切換路徑
 >cd ..

開始訓練
 >python train_ssd.py --dataset-type=voc --data=data/dataset --model-dir=models/dataset --num-workers=0 --batch-size=8 --epochs=50

將模型轉成onnx檔案
 >python onnx_export.py --model-dir=models/dataset

※ 使用者名稱是自己的資料夾路徑

※ cd .. 是返回上一個資料夾路徑

※ --num-workers 是工作進程(設置CPU核心數)

※ --batch-size=8 是批次大小，每一次計算8筆資料

※ --epochs=50 是時期，計算50次時期

# 訓練道路跟隨
把道路辨識資料集dataset_steering資料夾放在road_steering資料夾

切換路徑
 >cd C:\Users\使用者名稱\pytorch-ssd\road_steering

開始訓練
 >python train_steering.py

※ 使用者名稱是自己的資料夾路徑
