## How to train ?

CUDA_VISIBLE_DEVICES=0 python train_segmentation.py --model espnetv2 --s 2.0 --dataset sample --data_path ~/EdgeNet/vision_datasets/sample_dataset/ --batch-size 1 --crop_size 512 256 --model espnetv2 --s 1.5 --lr 0.009 --scheduler hybrid --clr-max 61 --epochs 100

- Input: vision_datasets/sample_dataset/images
- Target: vision_datasets/sample_dataset/annotations
- First run the convert_to_gray.py file which will convert all the annotations into grayscale images
- Then add the image names and respective grayscale annotations pair in vision_datasets/sample_dataset/train.txt file
- Do the same for val.txt file
- Start running the training process
