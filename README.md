# GUI-Based Paino Note Identification System using Matlab
Musical note identification is a process of recognizing the pitch and duration of a given sound signal, which is an essential step in music analysis, transcription, and composition. In MATLAB, the Fast Fourier Transform (FFT) is commonly used for analyzing the frequency content of a sound signal [3]. By applying FFT to a sound signal, we can convert the time-domain waveform into the frequency-domain spectrum, where each peak corresponds to a harmonic component of the sound. To identify the musical notes from the frequency spectrum, we can use the concept of the musical scale and tuning system. By dividing the frequency range into semitones and assigning them to the corresponding notes on the musical scale, we can map the frequency peaks to the musical notes. Without using machine learning, we can implement a note identification system in MATLAB by analysing the frequency spectrum of a sound signal using FFT and mapping the frequency peaks to the nearest musical note on the scale. 

![image](https://github.com/ParasPalli/GUI-Audio-Note-Identification/assets/115391909/2ace92dd-f560-4898-93bd-7d251fc28b85)

The process outlined involves analyzing an audio signal to identify the frequencies of individual musical notes present in the signal. The first step involves reading in the audio signal using the audioread() function and plotting the signal using the plot() function. 
The plot provides a visual representation of the waveform, which can help identify any noise or other anomalies in the signal. Next, the notewindows() function is used to identify the window for each note in the audio signal. Each note window is then extracted from the audio signal and plotted in the time domain using the plot () function. 

![Picture1](https://github.com/ParasPalli/GUI-Audio-Note-Identification/assets/115391909/7655f0e0-17f5-418a-867d-f9b6c356c4b8)

This provides a detailed view of each note and allows for the identification of any irregularities or noise. The FFT (Fast Fourier Transform) is then used to convert the current note from the time domain to the frequency domain. This provides a spectrum that shows the distribution of energy across different frequencies. The current note is then plotted in the frequency domain using the plot () function, which provides a visual representation of the frequency content of the note.

![image](https://github.com/ParasPalli/GUI-Audio-Note-Identification/assets/115391909/41b918d5-359f-4606-b1e5-cac17fdcb365)

The maximum peak in the frequency spectrum of the current note is identified, and its corresponding frequency is calculated. The bandpass () function is then used to filter out noise from the audio signal, retaining only frequencies within a narrow band centred on the fundamental frequency of each note. This helps to eliminate any unwanted frequencies that may be present in the signal.

![image](https://github.com/ParasPalli/GUI-Audio-Note-Identification/assets/115391909/28313b0e-5d37-4b6f-8f32-4a4da374567b)

The frequency of the note is then added to the freq array, which contains the frequency values of all notes present in the signal. Once all notes have been analyzed and their frequencies added to the freq array, the frequencies are printed using the print() function. Finally, the getNoteName() function is used to estimate the musical note name and octave from each frequency in the freq array. This information is printed using the print() function, providing a complete analysis of the audio signal in terms of the musical notes present. 
