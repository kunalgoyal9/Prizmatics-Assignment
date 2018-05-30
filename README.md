# Prizmatics-Assignment

## Steps
1. Clone darknet framework
2. Annoate the images using following tool "https://github.com/puzzledqs/BBox-Label-Tool"
3. Now our images have boxes UX,UY,LX,LY but for yolo we need to convert it in centerX, centerY, ObjX, ObjY. For this we will use this script https://github.com/Guanghan/darknet/blob/master/scripts/convert.py.
4. We now have to split our data in traing and test set using process.py script that I mentioned in repo.
5. Now we create configuration files as obj.data, obj.names, yolo-obj.cfg.
6. Yolo-obj.cfg has network as of yolov2 in cfg folder but updated accordingly .
7. Now we downloaded pre-trained weights from "https://pjreddie.com/media/files/darknet19_448.conv.23"
8. We train darknet using "./darknet detector train cfg/obj.data cfg/yolo-obj.cfg darknet19_448.conv.23" upto 1000 iterations for about 1 hour.
9. Test our obtained weigths in backup folder using command "./darknet detector test cfg/obj.data cfg/yolo-obj.cfg yolo-obj1000.weights data/testimage.jpg"
