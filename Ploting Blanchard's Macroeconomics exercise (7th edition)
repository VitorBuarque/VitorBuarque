'''Chapter 1
3. Chinese economic growth is the outstanding feature of the world economic scene over the past two decades.
    a. In 2014, U.S. output was $17.4 trillion, and Chinese output was $10.4 trillion.
    Suppose that from now on, the output of China grows at an annual rate of 6.5% per year,
    whereas the output of the United States grows at an annual rate of 2.2% per year.
    These are the values in each country for the period 2010–2014 as stated in the text.
    Using these assumptions and a spreadsheet, calculate and plot U.S. and Chinese output from 2014 over the next 100 years.
    How many years will it take for China to have a total level of output equal to that of the United States?'''

import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
plt.style.use('seaborn-darkgrid')

vi = 10.4
i = 0.065
length = 101
pib_china = [vi * (1+i)**m for m in range(1, length + 1)]

vi2 = 17.4
i2 = 0.022
pib_eua = [vi2 * (1+i2)**n for n in range(1, length +1)]

lista = list(range(2014,2115))
pib = {'YEAR': lista, 'CHINA': pib_china, 'USA': pib_eua}
df = pd.DataFrame(pib)

plt.fill_between(df['YEAR'], df['CHINA'], color="skyblue", alpha=0.5, label='CHINA')
plt.fill_between(df['YEAR'], df['USA'], color="green", alpha=0.7, label='USA')
plt.ylabel('GDP in US$ trillion')
plt.xlabel('Years')
plt.title('GDP projection between 2014-2114, considering a constant GDP growth of 2,2% (USA) and 6,5% (CHINA)')
plt.xticks(np.arange(2014, 2115, 10))
plt.annotate("China overtakes\nUS GDP in 2026", xy=(2026, 22.8), xytext=(2024, 2200), arrowprops={"arrowstyle":"->", "color":"r"})
plt.legend(loc='upper left')
plt.show()
