
# **PID Control** 

## Writeup

---

**PID Control Project**


The below steps are involded in doing the project PID control.
1) Initially implemented the PID control as mentioned in the leactures.
2)Then Initialize the PID control with the initail values and also the corresponding co efficients.
3)Tried twiddle but not successful so switched to manual tunning.
4)Observered that tuned vales works okay in the stright path but fails in the deep curves.
5)So to fix this tried to implemented varying trottle value at the curves.

### 1.Included files 

* src/main.cpp PID usage and the speed control logic. 
* src/PID.cpp Implement the error calculationulation.
* src/PID.h PID Class and thier corresponding variable definations and some temporary varibles.


#### 2. Project implementation

The technique used to implement the control login is PID
* p term: This plays a major role during the turn, larger value leads to oscilations in the vehical. An appropriate value needed for the vehical to turn if not its out of the track.
* I term: This is to correct the sensor biased value and this does play a major role in this project.
* D Term:  This reduces the oscilations casued by the term P. Specially while driving stright the D has an negative impact leading to oscilations. 

Initally tried to implement twiddle, that was very unstable i.e the error value increases based on the track like in the corners/turns the errors are high and in the straight line it works better.

So I have shifted to manual tuning with the values from the twiddle implmentation as reference and additional to improve the performance changed the trottle value based on the steering angle and crosstrack error. 

Output [video](./output_video.mp4).

