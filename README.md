OSSP_sy   
======= 
</br>


**주제**

* 원거리 바코드 인식


</br>

**사용한 오픈소스**

* 외부링크 : <https://pyimagesearch.com/2018/05/21/an-opencv-barcode-and-qr-code-scanner-with-zbar/>

</br>

**준비물**

Raspberry Pi 4 Model B

Pi camera V2, 8MP

Python

***


</br>
</br>


_1/6_
> **Install OpenCV + Python in raspberry Pi**
>* link : <https://pyimagesearch.com/2017/09/04/raspbian-stretch-install-opencv-3-python-on-your-raspberry-pi/>
>* Installation complete 
>![image](https://user-images.githubusercontent.com/93849755/211145842-ce4754f8-9dfa-450e-a76f-2133bc90fcc1.png)

</br>

>**An OpenCV barcode scanner with ZBar**
>* Recognition complete 
>![image](https://user-images.githubusercontent.com/93849755/211146495-19bb06b9-59a4-4de8-8004-a6b538023c89.png)
>

</br>
</br>

***

_1/10_
> **Original**
>![ori_png](https://user-images.githubusercontent.com/93849755/212828403-261482f5-6bc2-4e54-a35c-3aba0f88b3a2.jpg)
> * 기존 코드에서 바코드 인식 되는 최대 거리 (약 20cm)
</br>

> _Increase resolution_ 
>
>![image](https://user-images.githubusercontent.com/93849755/211147347-9e026982-97fd-4c01-8d31-6d817b2869f7.png)
> - 기존 코드 해상도와 차이가 없다. 카메라 모듈 차이
</br>

>_Auto focus_
>
>![image](https://user-images.githubusercontent.com/93849755/212852982-4c50a4a8-ee27-4806-ac96-07f99f68f429.png)
> - 해상도는 압도적으로 좋지만 , 카메라가 한번 켜지면 꺼지지 않는다 (일회성)


</br>

>***Using OpenCV instead of Pi Camera***
> - 기존 소스에서는 OpenCV에서 라즈베리파이 카메라 모듈에 접근해 PiCamera로 바코드를 인식했었다.
> - PiCamera를 사용하지 않고 OpenCV 로만 바코드를 인식했을 시 기존 소스코드 보다 바코드를 인식할 수 있는 거리가 늘어난 것을 확인할 수 있었다.
> 
> _otherwise use OpenCV_
> 
> ![open_png](https://user-images.githubusercontent.com/93849755/212860611-746df443-cf0f-4731-9eba-6458f422f7ed.jpg)
> - 노랑색(기존 소스코드), 파란색(opencv instead of picamera)
