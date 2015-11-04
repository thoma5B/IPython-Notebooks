
#IPython Notebooks 

The IPython Notebooks for this Repo are available and nicely formatted here:

http://nbviewer.ipython.org/github/thoma5B/defaultdict-list-example-/tree/master/


### defaultdict-list-example

```
ipython-notebook file with the following code:

from collections import defaultdict
import numpy as p

##############################
# and then the miracle occurs:

def make_dict(): 
    return defaultdict(make_dict)

mydict = make_dict()

mydict['coords'] = [(1,2),(3,4)]
mydict['colors'] = ['blue', 'red']
mydict['labels'] = ['A', 'B']

type(mydict)
##############################


d = {1: [0], 2: [0,0], 3: [0,0,0]}
#d[1].append(1)  # AttributeError: 'int' object has no attribute 'append'

dd = defaultdict(list)
for k, v in d.iteritems(): 
    for i in v:
        dd[k].append(i)
dd[1].append(2)
dd[1].remove(2)
dd
```