- Van Dyke, M. C. C., Teixeira, M. M., & Barker, B. M. (2019). 
"Fantastic yeasts and where to find them: the hidden diversity of dimorphic fungal pathogens. Current opinion in microbiology, 52, 55-63."

- Harvey, J. T., Culvenor, J., Payne, W., Cowley, S., Lawrance, M., Stuart, D., & Williams, R. (2002). 
"An analysis of the forces required to drag sheep over various surfaces." 
Applied Ergonomics, 33(6), 523-531.

- Zeigler, D. W., Wang, C. C., Yoast, R. A., Dickinson, B. D., McCaffree, M. A., Robinowitz, C. B., & Sterling, M. L. (2005). 
"The neurocognitive effects of alcohol on adolescents and college students."
Preventive medicine, 40(1), 23-32.


The following python code allows for the generation of the plot below:

```(python)
import pandas as pd
from matplotlib import pyplot as plt
import scipy.integrate
import pylab 

correl = pd.read_csv("istherecorrelation.csv", sep=';')


cons = plt.figure()
ax1 = cons.add_subplot(111)
pylab.plot(correl.iloc[:,0], correl.iloc[:,2],'o',linestyle='dashed',label='NL consumption')
ax1.set_ylabel('NL Beer Consumption (x1000 hectolitres)')
pylab.legend(loc='lower right')
ax2 = ax1.twinx()
pylab.plot(correl.iloc[:,0], [205.9,208.6,212.7,220.5,233.2,242.4,245.4,241.4,250.2,255.7,261.2,267.9,280.1],'o',color='r',linestyle='dashed',label='WO consumption')
ax2.set_ylabel('WO beer consumption (x1000 hectolitres)')
plt.title('Beer Consumption in the Netherlands')
pylab.legend(loc='center left')
plt.grid()
plt.savefig('YearsCons.png', dpi = 600)
```

![](https://github.com/PNicolau96/CS_Assignment/blob/master/YearsCons.png?raw=true)

