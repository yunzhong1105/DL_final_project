# DL final project
## 蘭花種類辨識及分類

模型分別存於兩個資料夾：(一)Swin Transformer(二)Other Networks

VGG-16、EfficientNet-B4、Bilinear VGG-16、ResNet皆存於(二)中

使用方式：

Swin Transformer採用的預訓練模型為swin_tiny_patch4_window7_224(下載連結：https://github.com/SwinTransformer/storage/releases/download/v1.0.0/swin_tiny_patch4_window7_224.pth)

主程式為main.py，執行請輸入以下指令：

```Bash
python -m torch.distributed.launch --nproc_per_node 1 --master_port 12345  main.py \
--cfg configs/swin_tiny_patch4_window7_224.yaml  --batch-size 8
```

****

VGG-16、EfficientNet-B4、Bilinear VGG-16、ResNet可使用other_networks.ipynb實現，只需執行.ipynb內的cell即可

****

更多詳細內容請參閱final report.pdf
