# Speech-Processing
This repository contains all the projects related to Speech Processing and Technology

## Project 1:
To run this project:
1. git clone https://github.com/kacperlsky/Speech-Processing.git
2. locate the folder Project 1 in this repository locally
3. Double click file VoiceChanger.pd


### Description
The aim of this assignment is to implement a range of speech processing algorithms for
real-time voice manipulation. The final outcome will be a ‘Voice Changer’ that can be
configured to perform a variety of different manipulations on your own voice. Part-I
involves creating the core components in Pd, and Part-II brings them together into a
single [VoiceChanger] application.


### Part1:
In this part of the project multiple separate audio processing modules were created. Each of these modules can be run separately after the input module connection. Their full list and explanation is listed below. 

#### Continuous Speech Input
Pd patch that can provide a continuous stream of real-time
speech that can be fed into the various manipulation techniques which follow

#### Filtering in the Time-Domain
One of the most basic manipulations in Voice FX is to ‘filter’ a signal in order to increase or
decrease energy at particular frequencies. The simplest types of filter are ‘low-pass’, ‘highpass’ and ‘band-pass’, and these may be implemented in Pd using the [lop∼], [hip∼]
and [bp∼] objects respectively.

#### Filtering in the Frequency-Domain
An alternative to time-domain
processing is to process signals in the ‘frequency-domain’, i.e. by modifying the spectrum
rather than the waveform.
A classic example of filtering in the frequency-domain is a ‘graphic equaliser’. This is a
common component of a high-fidelity (HiFi) audio system, and it allows the spectrum to
be shaped by setting gains across a range of frequencies.


#### Low Frequency Oscillator
LFOs typically have two controls: speed (which is specified
by the frequency in Hertz) and depth (which specifies the magnitude of the effect). 


#### Amplitude Modulation: Tremolo
‘Tremolo’ is one of the most basic voice manipulations that makes use of an LFO. In
this effect, the amplitude of a speech signal is modulated, i.e. the speech waveform is
multiplied by a variable gain that ranges between 0 and 1. LFO outputs an audio
signal between -depth and +depth. So, in order to modulate the amplitude of the speech
correctly, the output of the LFO has to be scaled appropriately - in this case, by adding
depth (e.g. using the audio math object [+∼] connected to the depth output of
LFO) and dividing the result by 2 (e.g. using the audio math object [*∼ 0.5]).

#### Ring Modulation
Another basic effect is to multiply the speech signal by the output of an LFO. This is
known as ‘ring modulation’.


#### Frequency Shifting
Many Vocal FX are the result of altering the frequencies present, e.g. changing the pitch
of a voice. There are many algorithms for frequency shifting.

#### Frequency Modulation: Vibrato
Implementation of ‘vibrato’ was achieved by connecting an LFO to your frequency shifter, and
experimenting with different values for speed and depth. The LFO output will
be scaled to provide an appropriate frequency shift range and then added to the
output of the frequency shift slider.


#### Time Delay Effects: Echo, Comb Filtering and Flanger
Many interesting voice FX can be achieved by delaying the signal and recombining it
with itself. You can notice these effects implemented in final version of this project.


#### Feedback: Reverberation
A simple method for achieving
such an effect is to feed a proportion of the output signal back to the input. This is known
as ‘feedback’ and has been implemented in this project.

### Part 2: Real-Time Voice Changer
The final part of this project was the compilation of the different components developed in Part-I into a single [VoiceChanger] application. The application allows
‘live’ speech input in addition to the ability to select a particular prerecorded file (i.e. no
longer hard-wired for speech.wav). 

## Project 2
On each stage of the project 1 there were multiple questions asked, which resulted in document creation covering both practical and theoretical aspects of signal processing and speech technology. This report is not published here but can be requested contacting me(ktlodzinski@gmail.com)

Both projects have been submitted as the partial requirement for the COM3502 Speech Processing at the University of Sheffield.

