# Satellite Image Mismatch

## Project Overview
This project aims to develop a low-cost terrain monitoring and infrastructure assessment technique using satellite imagery. The main objective is to identify and classify various objects present in satellite images and provide a comparative mismatch analysis of objects found in different images.

## Dataset
The project uses the Dstl Satellite Imagery Feature Detection dataset, which contains labeled images for 10 different classes:

1. Buildings (large building, residential, non-residential, fuel storage facility, fortified building)
2. Misc. Manmade structures
3. Road
4. Track (poor/dirt/cart track, footpath/trail)
5. Trees (woodland, hedgerows, groups of trees, standalone trees)
6. Crops (contour ploughing/cropland, grain crops, row crops)
7. Waterway
8. Standing water
9. Vehicle Large (lorry, truck, bus, logistics vehicle)
10. Vehicle Small (car, van, motorbike)

The dataset includes 1km x 1km satellite images in both 3-band (RGB) and 16-band formats. The 16-band images contain additional spectral information from the multispectral (400-1040nm) and short-wave infrared (SWIR) (1195-2365nm) range.

## Methodology
1. Data Pre-processing: Mapping ground truth data to original images
2. Model Architecture: UNET with Inception
   - Encoder: 16 - 32 - 64 - 128 - 256 filters
   - Decoder: 128 - 64 - 32 - 16 filters
   - Max pooling and up-sampling operations

## Model Training
- Optimizer: Adam
- Loss Function: Binary Cross-entropy
- Middle Activation Function: ReLU
- Output Activation Function: Sigmoid
- Evaluation Metric: Jaccard Similarity

## Results
The model was trained to identify four main categories:
1. Buildings and Manmade structures
2. Roads and dirt tracks
3. Trees
4. Crops

Jaccard Similarity scores were calculated for each category to evaluate the model's performance.

## Future Work
- Improve model accuracy for all object classes
- Implement object detection for vehicles (large and small)
- Develop a user interface for easy comparison of satellite images
- Integrate with GIS systems for broader applications

## To know more:-
https://drive.google.com/file/d/1p2mN9sIIqjUde-24gSEW_j1JlBS1e6A6/view?usp=sharing

