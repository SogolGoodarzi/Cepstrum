# Cepstrum
<p align="justify"> In Fourier analysis, Cepstrum is the result of applying the inverse Fourier transform to the logarithm of the Fourier transform. In fact, during the Fourier transform process, the logarithm of the signal magnitude is taken in the same frequency domain before being converted back to the time domain. This operation has many advantages, including that if two signals are convoluted, according to the properties of the logarithm, they can be added together before Fourier inversion, and for this reason, it has many applications in signal processing and especially in sound processing. It is worth noting that the independent variable, after Cepstrum conversion, is "quefrency" and its unit, like time, is seconds, although its interpretation is completely different from the interpretation of time. You can see the block diagram of the Cepstrum transform in the following figure. </p>

![image](https://github.com/SogolGoodarzi/Cepstrum/assets/125180530/62a1dad0-a713-463b-af06-c66e0c6fd094)

<p align="justify"> Also, the first part of the word cepstrum, that is, ceps, is actually the opposite of spec, and thus a semantic connection has been established in the names cepstrum and spectrum. </p>
In this section, we want to get acquainted with the term "quefrency".

* <p align="justify"> We have implemented a function step by step based on the given block diagram to implement Cepstrum transform. The input of this function is the desired signal, and its output gives the Cepstrum of the input signal. The requested function named Cepstrum() can be seen in the code section. </p>

* <p align="justify"> With the use of this function we have chosen three signals from data file and plotted the Cepstrum transform of these three signals. We adjust the quefrency axis based on the number of samples and give the three signals selected from the previous section to the function of the previous section and plotted the output of the cepstrum as shown below. </p>

![image](https://github.com/SogolGoodarzi/Cepstrum/assets/125180530/cc2d6e35-e841-4a8b-92cb-fdfcd6bd553e)

![image](https://github.com/SogolGoodarzi/Cepstrum/assets/125180530/7130f44a-18a2-423c-9ca8-269571c3f186)

* For the figures of the previous part, we have specified the quefrency ranges in which we see the peak:

![image](https://github.com/SogolGoodarzi/Cepstrum/assets/125180530/1ecb9191-b142-45b5-92a8-7e1a21f41a2b)

![image](https://github.com/SogolGoodarzi/Cepstrum/assets/125180530/b13ce2ba-7c1a-41b0-be0f-d0f10c2dbe4c)

![image](https://github.com/SogolGoodarzi/Cepstrum/assets/125180530/9c64df12-d4d0-4bc3-b3b2-4973932b2d88)

* <p align="justify"> If we see peaks in the graphs of the plotted Cepstrum output, we expect to see peaks corresponding to them in the Fourier transform of the signals, because the Fourier transform actually provides a frequency interpretation of the signal and its peaks as well. It expresses the meaning and concept or a feature of the signal in the frequency domain, so correspondingly, we expect these peaks to be the temporal interpretation of the same feature of the signal in question. </p>

<p align="justify"> In the figures below, we have plotted the Fourier transform and Cepstrum diagrams of the three signals side by side, and in each case, we have specified the intervals in which the peaks of the diagrams are located. </p>

<p align="justify"> According to the observations made in the previous figures, the following relationship can be expressed for the location of the peaks in the Fourier and Cepstrum transforms: </p>

![image](https://github.com/SogolGoodarzi/Cepstrum/assets/125180530/ce7b793b-ac1d-4435-b50d-d2f33f715dc6)

<p align="justify"> In fact, according to the above relationship, we can say that if we want to find the frequency of the peaks in the Fourier transform of the signal, we must divide the sampling frequency by the index of the sample in which the peak of the signal occurred. Now, according to Cepstrum, we have the first signal and its Fourier transform. </p>

![image](https://github.com/SogolGoodarzi/Cepstrum/assets/125180530/7a25b105-1ef4-470d-ae85-470d1f96ce6c)

![image](https://github.com/SogolGoodarzi/Cepstrum/assets/125180530/f3ea8ba9-1183-455e-a2a2-b5378a4bbebd)

<p align="justify"> According to the above relationship, for the mentioned interval, we see that we see peaks in the Fourier transform diagram of the signal in the frequency range of 0.16 to 0.267Hz. (Actually, at a very short distance from zero frequency, Fourier transform peaks have appeared). </p>

Now we will check for example 5 and 1585:

![image](https://github.com/SogolGoodarzi/Cepstrum/assets/125180530/7f0f88e5-7b52-491b-a1f4-faee312c72af)

<p align="justify"> We can see that in the Fourier transform diagram of the first signal, we have peaks at frequencies of 10 and -10. According to the above calculations, these two values ​​were obtained. For the sample of 1585, the value obtained is very close to the origin, where all the peaks of the graph are clear. For the other two signals, we can see that the written relation is correct. </p>

* <p align="justify"> In fact, the interpretation that can be given of quefrency is that it is a measure for measuring time, although as said, its unit is the same as the unit of time, i.e. second, but its interpretation is completely different from time. In fact, this parameter is used to measure in the time domain and compare the time domain with the frequency domain. When we plot the Fourier transform of a signal (that is, its spectrum), if a specific feature occurs at a specific frequency, we can correspondingly state the time of its occurrence in the Capstrom chart, or in other words In the domain, quefrency in how much this feature occurred. In the previous section, we also stated the relationship between frequency and quefrency. </p>
