### Spread of COVID-19 from Patient Zero

![](https://cdn-images-1.medium.com/max/800/1*UimKySbctrAdEbx1QoeGDg.png)

### Introduction

Coronavirus or COVID-19 is highly, highly infectious. According to the New York Times Influenza has an R0 (R naught) value of about 1.3.

In mathematical term R0 indicates contagiousness of an infectious disease.

R0 > 1 : Infection grows
R0 < 1 : Infection “is likely to die out"

According to research published in Oxford Journal of Travel Medicine. COVID-19 has a R0 value mean of 3.28 and median of 2.79.

So if we take an R0 of 3 we can extrapolate that Patient Zero infects 3 people, those 3 people infect 3 more people and so on and on and on....within just 10 exponents Patient Zero has infected 59,049 people!


```import matplotlib.pyplot as plt
import networkx as nx
G = nx.balanced_tree(3, 10)
pos = graphviz_layout(G, prog='twopi')
plt.figure(figsize=(10, 10))
nx.draw(G, pos, node_size=20, alpha=0.5, node_color="red", with_labels=False)
plt.axis('equal')
plt.show() 

