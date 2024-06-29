# 인공지능 실습 ic-pbl

## Model

[YOLO v5](https://github.com/ultralytics/yolov5)

## Classes

40 sign / 80 sign / green / yellow / red / stop / start / person

## Train images

traffic_images > images

클래스별로 50장씩

## Labels

traffic_images > labels     

## Weights

weights > best_exp11.pt

<br/>     
<br/>      
<br/>

# 실습 보고서

## AI Practice (A조)

송재현, 김진원, 신진호, 이채헌

## 데이터 수집

기존 이미지 200장으로는 정확도가 부족할 것이라고 생각하여 새 이미지 200장을 추가하기로 했습니다. 40sign, 80sign, start, stop 등의 표지판 이미지 중 일부는 기존 이미지 데이터를 만들 때 사용했던 표지판을 다양한 각도에서 촬영하여 새 이미지를 얻었으며, 신호등, 사람, 그리고 표지판 이미지의 일부는 인터넷에서 가져오는 방법을 사용했습니다.

## 라벨링

라벨링은 일정한 규칙을 가지고 수행했습니다. 40sign, 80sign은 연구원님의 조언에 따라 전체 표지판의 모양 보다 안에 있는 숫자에 집중하여 라벨링을 진행하였고, start, stop 이미지는 가운데에 있는 글자에 집중하였습니다. 신호등의 경우에는 신호등 전체가 아닌 불이 들어온 곳에만 라벨을 지정했습니다.

## 모델 학습

라벨링이 완료된 400개의 이미지를 epoch 값을 100, batch-size 값을 16으로 설정하여 총 7번 학습을 진행하였습니다.

![스크린샷 2024-06-22 165305](https://github.com/mongsam2/YOLO-traffic_object_detection/assets/121383589/5a9dca1b-bada-4079-be44-5bd6c9a74314)


## 테스트

![yellow](https://github.com/mongsam2/YOLO-traffic_object_detection/assets/121383589/97256adb-3f9b-438c-9ec3-5ce901019107)

![stop](https://github.com/mongsam2/YOLO-traffic_object_detection/assets/121383589/6cdc67c5-f010-4bc9-a09e-695377dfbb6c)

![red](https://github.com/mongsam2/YOLO-traffic_object_detection/assets/121383589/61dcf5c7-4253-4fe9-a73d-dc67f9605372)

![person](https://github.com/mongsam2/YOLO-traffic_object_detection/assets/121383589/66980d63-d477-42d0-a063-d4be16b98016)

![green](https://github.com/mongsam2/YOLO-traffic_object_detection/assets/121383589/cb33354a-1866-41c8-ac2f-ce0e14575450)

![80](https://github.com/mongsam2/YOLO-traffic_object_detection/assets/121383589/110468e9-a42a-400c-a105-998afd16852b)

![40](https://github.com/mongsam2/YOLO-traffic_object_detection/assets/121383589/86d2eb8c-24d8-4401-8073-831c8aeeba54)
