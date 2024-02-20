# SAG-Net
SAG-Net is the official repository of the paper "Using Segment-Level Attention to Guide Breast Ultrasound Video Classification".

The code are coming soon.

## WHBUS Dataset
Please download our dataset at https://drive.google.com/drive/folders/13oBWsRzKooeZBD6eRMHs6Mpf7ZeiPQHo?usp=sharing. Then set the dataset path in the code to where you put the dataset.

## Model
The model weights trained on BUV and WHBUS can be found at .

## Environment
python==3.9.7  
torch==1.12.1+cu113  
torchvision==0.13.1+cu113  
timm==0.3.2  
Please see 'requirements.txt' for details.

## Test
1. Test on BUV dataset
```python
python main.py \
    --batch_size 1 \
    --num_segs 6 --num_frames 3 \
    --resume ./pretrained_models/BUVweight/checkpoint-best067-mvauc0.9.pth \
    --eval True
```

2. Test on WHBUS dataset
```python
python main.py \
    --dataset 'WHBUS' \
    --traintxt '/mnt/data1/ZYDdata/data/WHBUS/tsm_train.txt' \
    --valtxt '/mnt/data1/ZYDdata/data/WHBUS/tsm_val.txt' \
    --batch_size 1 \
    --num_segs 8 --num_frames 7 \
    --resume ./pretrained_models/WHBUSweight/checkpoint-best085-mvauc0.9.pth \
    --eval True
```

