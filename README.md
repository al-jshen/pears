pears
=====

Make pairs plots!

```bash
pip install pears
```

Example
-------

```python

import numpy as np
import matplotlib.pyplot as plt
import pears

# generate some data
covx = np.random.normal(size=(4, 4))
covx = covx.T @ covx
covy = np.random.normal(size=(4, 4)) + np.diag([0.1, 0.2, 0.3, 4])
covy = covy.T @ covy
x = np.random.multivariate_normal(mean=np.zeros(4), cov=covx, size=1000)
y = np.random.multivariate_normal(mean=np.zeros(4), cov=covy, size=1000)

# make the pairs plot!
fig, ax = pears.pears(x.T)
# can also add more data to the plot
fig, ax = pears.pears(y.T, fig=fig, ax=ax)

plt.show()
```

![example](example.png)


