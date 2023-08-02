# get-infomation-of-database-from-colmap
[colmap](https://github.com/colmap/colmap)是目前最主流的增量式SfM框架  

其重建结果的数据格式通常为3个.bin文件和1个.db文件  
* cameras.bin  
* images.bin
* points3D.bin
* out.db

.bin文件提供重建后的3D点云信息(坐标,rgb,3D和2D对应索引)以及标定后的相机内外参数(images.bin, cameras.bin)详见https://colmap.github.io/index.html

.db文件提供以下信息:  
* cameras
* images
* keypoints
* descriptors
* matches
* two_view_geometries

为了更好地呈现重建的可视化效果在此提供`visualize_model.py`脚本  
可视化结果如下  

![visualization1](https://github.com/VG-TechCenter/scripts-for-colmap/assets/130300209/9e310d59-9eeb-4372-a37e-b1a26674fa50)
![visualization](https://github.com/VG-TechCenter/scripts-for-colmap/assets/130300209/02ae7164-9007-4e9f-ac57-7ee595e53773)
![visualization2](https://github.com/VG-TechCenter/scripts-for-colmap/assets/130300209/534bb946-c459-46ba-8272-39b70f52f0a4)
同时为了从database文件中读取匹配数量提供`database.py`脚本，其中以几何验证后的匹配信息为例运行  

