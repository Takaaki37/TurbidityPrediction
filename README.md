# TurbidityPrediction

残留塩素濃度予測モデルに使用します．

## 説明
### CNN.ipynb
CNNモデルを学習するコードです。<br>
mode：2値分類の場合は'binary、'多クラス分類の場合は'categorical'、回帰の場合は'raw'<br>
class_label：教師データが含まれる列の名前<br>
img_size：画像をのサイズ<br>
batch_size：バッチサイズ<br>
worker：使用するワーカーの数（PCによって異なる）<br>
dataLoad：画像のpath、教師データが含まれるcsvを読み込む、順番に学習、検証、テスト<br>
generateGen：学習、検証、テストデータの画像が含まれる列をpathにする<br>
model = ml.MCresnet50()：モデルを指定（モデルの種類は以下3つ）<br>
resnet50：ResNet-50<br>
MCresnet50：モンテカルロドロップアウトを使用したResNet-50<br>
vgg16：VGG16<br>

### image_process.ipynb
画像の前処理に使用するコードです。