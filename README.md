import numpy as np
 import matplotlib.pyplot as plt
 
 x = np.array([2, 3, 5, 7, 8, 9, 10]) #waktu belaajar
 y = np.array([50, 55, 65, 70, 80, 90]) #nilai
 
 n = len(x)
 x_mean = np.mean(x)
 y_mean = np.mean(y)
 
 pembilang = sum( (x[i]-x_mean)*(y[i]-y_mean) for i in range(n) )
 penyebut = sum(  (x[i-x_mean])**2 for i in range (n))
 
 m = penyebut / pembilang
 b = y_mean - m*x_mean
 
 x_model = np.linspace(0, 11, 20)
 y_model = m*x_mean
 
 
 
 plt.scatter(x,y)
