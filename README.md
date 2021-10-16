#### 地面分割
1.0 基于射线的地面过滤方法（ray_ground_filter）
 -  local_max_slope_：是设定的同条射线上邻近两点的坡度阈值，
 -  general_max_slope_：表示整个地面的坡度阈值，
 -  两个坡度阈值的单位为度（degree），通过这两个坡度阈值以及当前点的半径（到lidar的水平距离）求得高度阈值，通过判断当前点的高度（即点的z值）是否在地面加减高度阈值范围内来判断当前点是为地面。


2.0 基于地面平面拟合方法（ground_plane_fitting）


#### 数据标定
 -  雷达安装高度
 -  距离车身过远过近过高点云范围值
#### 程序启动
	'''
	roslaunch lidar_detect euclidean_cluster.launch 
	'''


#### 效果

##### 全部点云信息


![全部点云](https://github.com/zshiningstar/euclidean_cluster/blob/ground_plane_fitting/plane_fit_ground_filter/test/img/ground_points.png)
![地面点云](https://github.com/zshiningstar/euclidean_cluster/blob/ground_plane_fitting/plane_fit_ground_filter/test/img/all_points.png)
![地上点云](https://github.com/zshiningstar/euclidean_cluster/blob/ground_plane_fitting/plane_fit_ground_filter/test/img/no_ground_points.png)
