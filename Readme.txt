使用OpenCV實現攝像頭測距 [Find distance from camera to object/marker using Python and OpenCV]  (GOOGLE:OPENCV 測距)

資料來源:
https://zhuanlan.zhihu.com/p/63149294
https://www.pyimagesearch.com/2015/01/19/find-distance-camera-objectmarker-using-python-opencv/
https://github.com/zxdefying/OpenCV_project/tree/master/distance_to_camera

使用相似三角形計算物體到相機的距離

假設物體的寬度為W，將其放到離相機距離為D 的位置，然後對物體進行拍照。在照片上量出物體的像素寬度P，於是可以得出計算相機焦距F 的公式：

F =（P x D）/ W

比如我在相機前24 英寸距離（D=24 inches）的位置橫著放了一張8.5 x 11 英寸（W=11 inches）的紙，拍照後通過圖像處理得出照片上紙的像素寬度P=248 pixels。

所以焦距F 等於：

F =（248px x 24in）/ 11in = 543.45

此時移動相機離物體更近或者更遠，我們可以應用相似三角形得到計算物體到相機的距離的公式：

D'=（寬x F）/ P

