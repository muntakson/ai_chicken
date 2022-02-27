
# *** 인공지능 닭장 캠프 ***
![alt text](https://github.com/joyinstech/ai_chcien/blob/main/ai_chicken_coop_photo_night.jpg)
## - 장소: 포항 제철 공업 고등학교, 2021.5
## - 주최: Joy Institute of Technology 적정기술 연구소, 경주시, 한국

  
  

## - 취지
     
   닭의 일일 평균 행동량을 자동으로 계산해서  농부들에게 전송해주자!

   빈곤국 청년들이 인공지능을 재미있게 배울 수 있게 하자!
   
   
   
 
## - 캠프 내용 

시간: 1:30분씩 이틀간

대상: 고등학생

내용: 닭사진에 주석달기 -> 신경망 훈련시키기 -> 닭 동영상을 신경망에 넣어 닭을 검출하기


### -- 사용된 사진 출처

돼지사진: 경주 남산 제노드 농장

닭사진 제공:  Mr. Biplop Das 

유튜브 채널의 운영자 - https://www.youtube.com/channel/UCuuzjdPwvZV065hFItHQ1jQ

![alt text](https://github.com/muntakson/ai_chicken/blob/main/chicken_coop_sideview.png)


![alt text](https://github.com/muntakson/ai_chicken/blob/main/ai_chicken_coop_photo_ceiling.jpg)


![alt text](https://github.com/muntakson/ai_chicken/blob/main/mychicken_boundingbox.png)


### -- 캠프보조장비: 인공지능 닭 검출기와 IoT전광판, IoT릴레이 키트

![alt text](https://github.com/muntakson/ai_chicken/blob/main/chicken_activity_board_r1.png)


## - 캠프 일정

1일차: 주석 달기

닭사진: 100장, 90장은 train, 10장은 평가용

주석달기: makesense.ai 이용

2일차: 신경망 추론

신경망훈련: colab.research.google.com 이용

검출시험용 동영상으로 신경망 평가: mychicken.mp4  


## - 캠프 진행 과정

![alt text](https://github.com/muntakson/ai_chicken/blob/main/flowchart_1.png)


## - 준비할 데이터 구조 및 훈련용과 검증용 사진

![alt text](https://github.com/muntakson/ai_chicken/blob/main/dataset_structure.png)

## - labeling 작업 결과로 만들어진 주석파일 내용의 의미

![alt text](https://github.com/muntakson/ai_chicken/blob/main/anotation_file_inside.png)

## - 사용할 신경망 파일: YOLO 개발자가 80개의 물제를 인식할 수 있도록 이미 훈련시켜 놓은 신경망. 이 신경망 위에 우리가 인식시키고자 하는 물체를 추가적으로 인식할 수 있도록 훈련시킬 것임

![alt text](https://github.com/muntakson/ai_chicken/blob/main/yolov5s_pt.png)


# 참조: 신경망이란 무엇인가?

https://playground.tensorflow.org/


# 참조: YOLO는 무엇인가?

https://www.youtube.com/watch?v=Cgxsv1riJhI


## - YOLO는  빠르고 정확하게 이미지 속의 객체를 검출한다

https://www.youtube.com/watch?v=XS2UWYuh5u0


## - YOLO를 사용하면 인공지능 닭장을 만들 수 있다

https://www.youtube.com/watch?v=GRtgLlwxpc4


# 사례: 음베일 마을 '나지리니'의 옥수수 해충 검출기 

![alt text](https://github.com/muntakson/ai_chicken/blob/main/nanzirini.png)

http://www.sciengineer.or.kr/board_Tqqc07/24029


# I. 주석달기 작업

1. 조를 편성.
2. 각조에 100장의 사진을 나누어준다
3. 90장과 10장으로 분류
4. 90장을 images폴더 아래 train폴더에 넣어줌
5. 10장을 images폴더 밑에 val폴더에 넣어줌
6. makesense.ai 사이트로 가서 시작하기 버튼
7. 90장의 사진을 모두 선택하여 makesense.ai의 드롭박스에 던져주라
8. 라벨을 새로 만들어 chicken이라고 이름을 붙이고
9. 90장의 사진에 대해 바운딩박스를 그려서 주석작업을 하라
10. actions메뉴를 클릭하고 export 를 선택. 
11. 주석화일 포맷은 YOLO로 지정
12. export를 마치면 90장개의 주석화일(화일이름.txt)가 압축되어 내려온다
13. 이 압축파일을 labels 폴더 밑에 train폴더에 풀어라
14. 7,8,9,10,11,12 단계를 10장의 사진에 대해 반복하라
15. 이 화일을 labels 폴더밑에 val폴더에 풀어라
16. images와 labels를 한데 묶어 압축화일로 만들어라
17. 이 압축화일의 이름을 chicken_dataset.zip이라고 변경하라

18. 참고1: 돼지 데이터셋(경주시 농장에서 촬영) 다운로드:    https://drive.google.com/file/d/1mgEfOKjcXaj944KVOdklCgZT--x9cOP4/view?usp=sharing
19. 참고2: 돼지 동영상:  https://drive.google.com/file/d/15Yn-l9vvWSkJFP9izG4BcHhhutoztX8y/view?usp=sharing
20. 참고3: 닭 (인터넷에서 모은 사진)데이터셋 다운로드: https://drive.google.com/file/d/1d55WE2YX6b4RE3kyGFobKdq0t1kBoQAs/view?usp=sharing
21. 참고4: 닭 동영상 (경주시 소재 닭장에서 촬영): https://drive.google.com/file/d/1rVEdty5c63avIwa6G3M9jVCx-Un8ej7r/view?usp=sharing
22. 참고5. 돼지 검출 동영상: https://github.com/muntakson/ai_chicken/blob/main/pig_zenod_detected_low_res.mp4

# II. 신경망 훈련

<준비사항> 구글크롬 브라우저 상에서 구글콜랩과 구글드라이브를 연동하여 사용할 것이므로 먼저 구글크롬 브라우저를 설치하고 크롬에서 자신의 구글 계정으로 로그인한 상태로 만들어서 다음 과정을 진행해야 한다.

1. 각 조마다 colab.research.google.com 에 로그인하라
2. 이 깃헙의 aicamp의 콜랩 노트북을 클릭하여 노트북을 열어라
3. 파일 메뉴에 가서 내 구글드라이브에 사본만들기를 하라
4. 그 사본을 열고 원본 노트북은 닫아라
5. 1단계 YOLO 다운로드 버튼을 클릭
6. 전 단계에서 만든 chicken_dataset.zip을 PC에서 콜랩으로 업로드하라 (드랙앤드롭으로)
7. 2단계 압축데이터를 풀기 버튼을 클릭
8. yolov5의 data폴더에 있는 coco128.yaml 파일을 업데이트하고 이름을 chicken.yaml로 변경하라
9. 3단계  신경망 훈련 버튼을 클릭
10. 신경망이 자동으로 훈련되기 시작한다
11. 10분정도 시간이 흐르면 훈련이 완료된다 (mAP값이 얼마인지 확인 0.9이상이 되어야 함)
12. runs폴더에 가서 훈련 결과를 확인
13. 평가용사진을 클릭하면 신경망이 원본사진에 닭의 위치에 바운딩박스를 그려준것이 확인됨 

# III. 신경망 추론

1. mychicken.mp4화일을 콜랩의 업로드 (드랙앤드롭)
2.4단계 추론버튼을 누른다
3. 신경망이 닭의 동영상 화일을 열어 매 프레임마다 닭을 검출하여 바운딩 박스를 그려준다
4. 이 결과화일을 PC로 다운로드
5. PC에서 이 화일을 플레이해본다

# IV. 토론 및 종료

1. 다음주제에 대해 토론해본다
2. 신경망이 정확하게 추론하려면 어떤점을 보완해야 할까?
3. 신경망이 생성한 정보를 일상생활에성 용하게 사용하려면 어떤 기술이 더 추가되어야 할까?
4. 캠프에서 배운 지식을 응용하여 발명하고 싶은 장치나 서비스는 무엇인가?


# 사진폴더, 주석폴더 만들때 주의할점

   닭사진 화일과 주석 화일은 다음과 같이 배치하라. 
   작업폴더에 images와 labels폴더를 만들고
     
     images 폴더 아래 train과 val폴더를 만들라
        train 폴더에 90장의 닭사진 화일을
        val 폴더 밑에 10장의 닭사진 화일을 넣어라
      labels 폴더 아래 train과 val폴더를 만들라
        train폴더에 90장의 주석처리된 닭사진 화일을
        val 폴더 밑에 10장의 주석처리된 닰사진 화일을 넣어라





# [주석작업 절차]

## 1. 닭 사진을 준비하고 폴더를 만들어 사진을 해당 폴더로 이동시켜라

![alt text](https://github.com/muntakson/ai_chicken/blob/main/1000_chicken_image.png)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/image_separation.png)


![alt text](https://github.com/muntakson/ai_chicken/blob/main/90-10_images.png)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/train_folder.jpg)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/val_folder.jpg)

## 2. 브라우저를 띄우고 makesense.ai 를 주소창에 입력하여 이동하라

![alt text](https://github.com/muntakson/ai_chicken/blob/main/makesensor_click.png)

## 3. 준비된 닭 사진을 makesense.ai로 업로드하라

![alt text](https://github.com/muntakson/ai_chicken/blob/main/drag_n_drop_90_photos.png)

## 4. 'object detection(물체 인식)' 에 이어서 'your label list is empty(레이블이 비었다)'라고 쓰여있는 아이콘을 클릭하면 label을 만들라는 메뉴가 나온다

![alt text](https://github.com/muntakson/ai_chicken/blob/main/click_label_list.png)

## 5. 'chicken' 혹은 원하는 label을 만든 후 'start project(프로젝트 시작)' 메뉴를 클릭하면 labeling 작업을 시작하게 된다

![alt text](https://github.com/muntakson/ai_chicken/blob/main/create_chicken_label.png)

## 6. 마우스를 드래그하여 물체 주위에 바운딩 박스를 그리고 그에 해당하는 label을 선택한다

![alt text](https://github.com/muntakson/ai_chicken/blob/main/labeling.png)

## 7. 화면에 있는 해당 물체들에 모두 label을 붙여준다

![alt text](https://github.com/muntakson/ai_chicken/blob/main/labeling_multi_chicken.png)

## 8. 'actions' 메뉴를 선택하여 결과를 export 한다

![alt text](https://github.com/muntakson/ai_chicken/blob/main/export_annotation.png)

## 9. 이때 YOLO 포맷으로 export 해야한다

![alt text](https://github.com/muntakson/ai_chicken/blob/main/select_yolo_format.png)

## 10. export를 클릭하면 결과 파일이 압축되어 다운로드된다

![alt text](https://github.com/muntakson/ai_chicken/blob/main/download_annotation.png)

# [신경망 훈련 절차]

## 구글의 드라이브와 콜랩(Colab)을 활용하여 신경망을 훈련시키는 과정.
## <준비사항> 구글크롬 브라우저 상에서 구글콜랩과 구글드라이브를 연동하여 사용해야 하므로, 먼저 구글크롬 브라우저를 설치하고 크롬에서 자신의 구글 계정으로 로그인한 상태로 만든 후 다음 과정을 진행해야 한다.

## 1. 크롬 브라우저에서 github.com/aicamp로 이동하기

![alt text](https://github.com/muntakson/ai_chicken/blob/main/github_aicamp.jpg)


## 2. 'YOLO_닭_제철공고.ipynb' 파일을 클릭하여 (주피터노트북으로) 열기

![alt text](https://github.com/muntakson/ai_chicken/blob/main/open_nb.png)

## 3. 'open in colab' 버튼을 클릭하여 colab으로 이동하기

![alt text](https://github.com/muntakson/ai_chicken/blob/main/from_githun_to_colab.png)

## 4. 노트북의 사본을 구글드라이브에 복사하기

![alt text](https://github.com/muntakson/ai_chicken/blob/main/copytodrive.png)

## 5. 원본 노트북 닫고 사본 노트북을 열기

![alt text](https://github.com/muntakson/ai_chicken/blob/main/opennotebook.png)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/opennotebook_2ndstep.png)



## 6. 파일매니저 열기

![alt text](https://github.com/muntakson/ai_chicken/blob/main/open_file_manager.png)


## 7. 자신의 노트북에 준비되어 있는 데이터를 콜랩으로 업로드하기. (데이터는 사진이 들어있는 images와 labels 두 개의 폴더를 하나의 zip파일로 준비)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/drag_n_drop.png)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/dataset_upload.png)


## 8. 1단계 YOLO 다운로드 받기 (마우스를 클릭할 동그라미 위로 옮기면 동그라미가 검게 변하고 안에 삼각 화살표가 나타남)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/yolo_download.jpg)


## 9. 2단계 데이터셋 압축 풀기
![alt text](https://github.com/muntakson/ai_chicken/blob/main/unzip.png)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/refresh.png)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/check_images_labels.png)


## 10. coco128.yaml 파일로 들어가서 데이터셋의 경로 화일 등을 아래의 그림과 같이 수정하고 난 후, coco128.yaml의 파일이름을 chicken.yaml로 바꾸기

![alt text](https://github.com/muntakson/ai_chicken/blob/main/open_coco218.png)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/erase_coco128.png)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/edit_coco128.png)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/change_name.png)



## 11. 드디어 신경망을 훈련시키자

![alt text](https://github.com/muntakson/ai_chicken/blob/main/train.png)

![alt text](https://github.com/muntakson/ai_chicken/blob/main/check_train.png)

## 12. 신경망 훈련 결과를 살펴보자

![alt text](https://github.com/muntakson/ai_chicken/blob/main/train_result_folder.png)


![alt text](https://github.com/muntakson/ai_chicken/blob/main/train_result.png)








## 13. 닭장에 가서 동영상을 촬영하고 그 비디오를 신경망에 넣어보자

![alt text](https://github.com/muntakson/ai_chicken/blob/main/mychickens.png)

https://www.youtube.com/watch?v=oBG4-dMmNts

https://github.com/muntakson/ai_chicken/blob/main/mychicken_short.mp4

## 14. 동영상을 콜랩에 업로드 하라

![alt text](https://github.com/muntakson/ai_chicken/blob/main/upload_chicken_video.png)


## 15. 동영상의 경로를 클립보드로 복사

![alt text](https://github.com/muntakson/ai_chicken/blob/main/copy_chicken_video_path.png)


## 16. 신경망의 경로를 클립보드로 복사

![alt text](https://github.com/muntakson/ai_chicken/blob/main/copy_model_path.png)


## 17. 신경망의 경로, 동영상의 경로를 붙여 넣어라

![alt text](https://github.com/muntakson/ai_chicken/blob/main/paste_model_and_video.png)



## 18. 두둥,, 진실의 순간 ... 검출기를 실행하라!

![alt text](https://github.com/muntakson/ai_chicken/blob/main/prediction.png)


![alt text](https://github.com/muntakson/ai_chicken/blob/main/prediction_result.png)


## 19. 검출 결과가 담긴 동영상을 다운받자

![alt text](https://github.com/muntakson/ai_chicken/blob/main/down_prediction_video.png)



## 20. 닭 검출기의 성능을 확인하라

https://youtu.be/JMpAo1GysWc


### 설문지

https://forms.gle/QMfxgMMTPNwEMpem8
