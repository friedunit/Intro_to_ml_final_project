## Introduction

#### This notebook is for the final project of 5509 Intro to Machine Learning. I decided to do a classification problem that determines if a mushroom is edible or poisonous based on its characteristics. I perform some preprocessing on the data such as Label Encoding, dropping an irrelevant feature, renaming the target variable and changing 'e' and 'p' to 1 and 0. I then build a Statsmodels Generalized Linear Model (GLM) with formula and used back selection to remove insignificant variables with high p-values. I also used the Statsmodels Logit function to build a seperate model for comparison. I then used a few Sklearn models including a Random Forect Classifier and Decision Tree Classifier. Both achieved perfect test accuracy of 1.0. FInally, I built a logistic regression model from Sklearn using their scaling pipeline. This model achieved a test accuracy of 0.952.

#### The data is in .csv format and was retrieved from https://www.kaggle.com/datasets/uciml/mushroom-classification?resource=download&select=mushrooms.csv .

### Attribute Information: (classes: edible=e, poisonous=p)

cap-shape: bell=b,conical=c,convex=x,flat=f, knobbed=k,sunken=s

cap-surface: fibrous=f,grooves=g,scaly=y,smooth=s

cap-color: brown=n,buff=b,cinnamon=c,gray=g,green=r,pink=p,purple=u,red=e,white=w,yellow=y

bruises: bruises=t,no=f

odor: almond=a,anise=l,creosote=c,fishy=y,foul=f,musty=m,none=n,pungent=p,spicy=s

gill-attachment: attached=a,descending=d,free=f,notched=n

gill-spacing: close=c,crowded=w,distant=d

gill-size: broad=b,narrow=n

gill-color: black=k,brown=n,buff=b,chocolate=h,gray=g, green=r,orange=o,pink=p,purple=u,red=e,white=w,yellow=y

stalk-shape: enlarging=e,tapering=t

stalk-root: bulbous=b,club=c,cup=u,equal=e,rhizomorphs=z,rooted=r,missing=?

stalk-surface-above-ring: fibrous=f,scaly=y,silky=k,smooth=s

stalk-surface-below-ring: fibrous=f,scaly=y,silky=k,smooth=s

stalk-color-above-ring: brown=n,buff=b,cinnamon=c,gray=g,orange=o,pink=p,red=e,white=w,yellow=y

stalk-color-below-ring: brown=n,buff=b,cinnamon=c,gray=g,orange=o,pink=p,red=e,white=w,yellow=y

veil-type: partial=p,universal=u

veil-color: brown=n,orange=o,white=w,yellow=y

ring-number: none=n,one=o,two=t

ring-type: cobwebby=c,evanescent=e,flaring=f,large=l,none=n,pendant=p,sheathing=s,zone=z

spore-print-color: black=k,brown=n,buff=b,chocolate=h,green=r,orange=o,purple=u,white=w,yellow=y

population: abundant=a,clustered=c,numerous=n,scattered=s,several=v,solitary=y

habitat: grasses=g,leaves=l,meadows=m,paths=p,urban=u,waste=w,woods=d
