### A-basic-noise-reduction-function-in-R-for-logRatio-signal

## Analysis of Data
1. chr is given as num value but due to insufficient information about “chr” I am assuming it as a factor value. It is level number assigned for every test.
![testsample1](https://user-images.githubusercontent.com/21276147/36691289-d1bf5b5e-1b5a-11e8-957b-06711a4e82b7.png)
![testsample2](https://user-images.githubusercontent.com/21276147/36691321-f017eff8-1b5a-11e8-811a-9fdb75fc4483.png)
This indicates that we are having different range values for two different values of “chr” in every test sample.
2. end and start depicts the grouping of data.
3. For a certain level and a certain group we are given testSamole1 and testSample2 values.
```
Example: 
              chr	start	    end	    	  testSample1		testSample2
Row 1:		1	   0	    29999	  0.17215987314604	0.931841373631194
Row 7452: 	2	   0	    29999	  0.170749928253841	0.563014312697292
  ```
4. Variance of both samples
```
var(testSample1)
[1] 0.0265392
var(testSample2)
[1] 0.02372361
```
5. Covariance of both samples
```
cov(testSample1, testSample2)
[1] -0.01660213
```
6. Boxplot of both test samples
![boxplot](https://user-images.githubusercontent.com/21276147/36692012-eba9b33c-1b5c-11e8-90e8-d91b2c923913.png)
There are many outliers. In other words, there is so much noise in this data.


## LogRatio Signal
![logratio](https://user-images.githubusercontent.com/21276147/36692092-1e51af38-1b5d-11e8-9073-6944ebe81006.png)
```
var(logratio.data$logratio)
[1] 3.167599
```
## Filtered LogRatio Signal
![logratio filtered](https://user-images.githubusercontent.com/21276147/36692124-3b377bdc-1b5d-11e8-9eec-dec9ab1d3a8a.png)
```
var(logratio.filter.data$logratio.filter)
[1] 0.5292195
```
