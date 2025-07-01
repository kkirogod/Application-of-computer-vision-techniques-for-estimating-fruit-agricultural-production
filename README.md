# Application-of-computer-vision-techniques-for-estimating-fruit-agricultural-production

Accurate fruit load estimation is a key factor in planning and optimizing production in agricultural operations. 

This Bachelor’s Thesis proposes a solution based on computer vision and deep learning techniques to estimate the number of fruits (oranges) present in images of Midknight orange trees captured under real field conditions. 
Unlike traditional approaches that rely on manual counting or physical sensors, this work aims to automate the process using regression and object detection models, with the goal of exploring which paradigm yields better results in adverse scenarios in real agricultural environments.

The project develops two main experimental lines. First, deep regression models are trained on images labeled with the real total fruit count (both visible and non-visible). Second, object detection models are trained to individually locate visible fruits, followed by the application of an occlusion correction factor that is automatically optimized to improve the total estimation.

![image](https://github.com/user-attachments/assets/f75f4f8d-a646-4c2e-8b4d-60fdd35c1ee6)

Evaluation was performed on a carefully annotated dataset, where only the visible fruits of the central tree in each image are labeled. Additionally, the external CitDet dataset, which follows a different annotation strategy, was incorporated to analyze its impact on model performance.

![image](https://github.com/user-attachments/assets/c474dca9-9a3d-4aaa-ab2c-ec031a9ca4d9)

![image](https://github.com/user-attachments/assets/e142ef8d-7ec0-4678-9b42-8f8a10cfd70f)

Results show that the regression-based approach, particularly the EfficientNetB5 architecture, delivers the best performance in terms of mean absolute error (MAE = 31,68) and coefficient of determination (R2 = 0,53), clearly outperforming both detection-based methods and naive estimators such as the global mean. This suggests that in scenarios where global image-level labels are available and the goal is to estimate both visible and occluded fruits, well-tuned pretrained regression models offer superior potential. In contrast, detection models tend to overestimate or underestimate fruit load when the occlusion factor is not properly calibrated or when external data are used without proper alignment with the task’s objective.

![image](https://github.com/user-attachments/assets/5eb7a146-0fac-4e1b-8182-f2080f79b748)

In conclusion, this work demonstrates the feasibility of applying deep learning techniques to fruit counting in agricultural settings, through a rigorous comparison between regression and detection approaches, and lays the groundwork for the future development of automated precision agriculture systems.


**Keywords:** computer vision, fruit load, deep learning, regression, object detection, occlusion,
yield estimation, convolutional networks, EfficientNet, YOLO, RT-DETR.
