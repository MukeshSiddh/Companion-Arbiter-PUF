# Companion-Arbiter-PUF
A CAR-PUF uses 2 arbiter PUFs – a working PUF and a reference PUF, as well as a secret threshold value τ > 0. 
Given a challenge, it is fed into both the working PUF and reference PUF and the timings for the upper and lower signals for both PUFs are measured. 
Let ∆w, ∆r be the difference in timings experienced for the two PUFs on the same challenge. 
The response to this challenge is 0 if |∆w − ∆r| ≤ τ and the response is 1 if |∆w − ∆r| > τ where τ > 0 is the secret threshold value.

Now our job is to build a linear machine learning model to predict the responses if given a few thousand challenge-response pairs (CRPs). 
**Given Data**: We have provided you with data from a CAR-PUF with 32-bit challenges. The training set consists of 40000 CRPs and the test set consists of 10000 CRPs.
