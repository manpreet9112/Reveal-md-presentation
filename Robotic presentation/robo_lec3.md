<link rel="stylesheet" href="beige.css" id="theme">


![image](screenshots/lec3.gif)

---

#Histogram

---

<section data-background="screenshots/m3.png"></section>

---

<section data-background="screenshots/m4.png"></section>

---

<section data-background="screenshots/m4x.png"></section>

---

<section data-background="screenshots/m5.png"></section>

---

<section data-background="screenshots/m5x.png"></section>

---

#some slides here

---

<section data-background="screenshots/m10.png"></section>
<span style="background-color:rgb(1,1,1);display:block;opacity:0.6;color:white">Its a grey color image.</span>

---


#Monadic Operations

---

<h2 style="text-align:left;"><span style="color:rgb(220,54,54);">Monadic</span> processing </h2>
<img style="border:none;" src="screenshots/monodic.png"/>
<ul>
<li> Each output pixel is a function of corresponding input pixel.</li>
<li> The function is <span style="color:rgb(220,54,54)">the same</span> for all pixels.</li>
</ul>

---

<h2 style="text-align:left;"><span style="color:rgb(220,54,54);">Monadic</span> image processing </h2>
<section>![image](screenshots/image2.png)</section>

---

<h2 style="text-align:left;"><span style="color:rgb(220,54,54);">Monadic</span> image processing </h2>
<section>![image](screenshots/image.png)</section>

<section>![image](screenshots/image.png)</section>

---

<h2><span style="color:rgb(220,54,54)">Monodic image</span> processing</h2>
<ul><li><span style="color:rgb(220,54,54)">what is f(x)?</span>
<ul>
<li class="fragment">changing the datatype</li>
<li class="fragment">changing the brightness and contrast</li>
<li class="fragment">histogram normalisation</li>
<li  class="fragment">threshloding</li>
<li class="fragment">posterisation</li>
</ul></li></ul>

---

<section data-background="screenshots/o9.png"></section>

---

<h2><span style="color:rgb(220,54,54)">Changing</span> brightness</h2>
![brightness](screenshots/Brightness.png)

---

<h2><span style="color:rgb(220,54,54)">Code </span>for brightness</h2>

```
import cv2
#bright image
def bright(img,n):
	cc,rr,dd =img.shape
	n=input(" enter no. in range 0-255 ")
	imgB=img+n
	for a in range(cc):
		for b in range(rr):
				if (imgB[a][b][0]<n or imgB[a][b][1]<n or
                                   imgB[a][b][2]<n ):
					imgB[a][b]=255
	return imgB

```


---

<h2><span style="color:rgb(220,54,54)">Changing</span> contrast</h2>
![contrast](screenshots/contrast.png)

---

<h2><span style="color:rgb(220,54,54)">Code </span>for contrast</h2>
```
#contrasting image.
def contrast(img,n):
	img=img.astype('float32')
	imgB=img*n
	for a in range(cc):
		for b in range(rr):
			if(imgB[a][b][0]>255 or imgB[a][b][1]>255 or 
			imgB[a][b][2]>255):			
				imgB[a][b]=255
	return imgB
```

---

<h2><span style="color:rgb(220,54,54)">negative</span> image</h2>
![Negative](screenshots/Negative.png)

---

<h2><span style="color:rgb(220,54,54)">Code </span>for negative</h2>

```
#negative image
def negative(img):
	imgB=1-img
	cv2.imwrite('negative.png',imgB)

```

---

<h2><span style="color:rgb(220,54,54)">Posterisation</span></h2>
![bright](screenshots/posterization.png)

---

<h2><span style="color:rgb(220,54,54)">Code </span>for posterisation</h2>

```
#posterisation image
def posterisation(img):
	n=int(input('posterisation level'))
	imgB=n*floor(img/n)
	imgB=imgB.astype('uint8')
	return imgB

```

---

#Histogram Normalisation

---

<section data-background="screenshots/p6.png"></section>

---

<section data-background="screenshots/p7.png"></section>

---

<section data-background="screenshots/p8.png"></section>

---

<section data-background="screenshots/q2.png"></section>

---

#Gamma Correction

---

<section data-background="screenshots/q5.png"></section>

---

<section data-background="screenshots/q6.png"></section>

---

<section data-background="screenshots/q7.png"></section>

---

<section data-background="screenshots/q8.png"></section>

---

<section data-background="screenshots/q9.png"></section>

---

<section data-background="screenshots/r1.png"></section>

---

<h2><span style="color:rgb(220,54,54)">monadic</span> function</h2>

---


#Vectorisation

---

<h2><span style="color:rgb(220,54,54)">Matrix</span> Operation</h2>
<section>![image](screenshots/r2.png)</section>

---

<h2><span style="color:rgb(220,54,54)">Matrix</span> Operation</h2>
<section>![image](screenshots/r3.png)</section>

---

##2 slides here

---

#Thresholding

---

<h2><span style="color:rgb(220,54,54)">Thresholding</span> </h2>
<ul>
<li><span style="color:rgb(220,54,54)">The resulting image has only two values:</span>
<ul>
<li class="fragment">false (black) if x<T</li>
<li class="fragment">true (white) if x>=T </li>
</ul></li></ul>
<img style="border:none;" src="screenshots/thresh.gif"/>


---

#Diadic Operations

---

<h2><span style="color:rgb(220,54,54)">diadic</span> operation</h2>
![image](screenshots/t1.png)
<ul>
<li> Each output pixel is a function of corresponding input pixel.</li>
<li> The function is <span style="color:rgb(220,54,54)">the same</span> for all pixels.</li>
</ul>

---

<section data-background="screenshots/t2.png"></section>

---

<section data-background="screenshots/u6.png"></section>

---

<section data-background="screenshots/u7.png"></section>

---

<section data-background="screenshots/v1.png"></section>

---

<section data-background="screenshots/v2.png"></section>

---

<section data-background="screenshots/v3.png"></section>

---

<section data-background="screenshots/v4.png"></section>


