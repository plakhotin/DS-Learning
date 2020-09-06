# DS-Learning
### Here I post all my learning notes

**SOME INFO ON DESCRIPTIVE ANALYSIS**

* Sql is always better than Pandas for pre-processing. Its syntaxis is more practical.
* NaNs should be handeled. Fill it with either of these: median, mean, boolean.
* Categorical data should be converted to numbers.
* Check data types (df.info, df.dtypes)
* Bring everything to 1 scale: standartize or normalize.
* In future data should be spilit in 3: train, validation and test sets.

### P — Values

* Set a Null-hypothesis H0 and an alternative one Ha.
* Then take a sample and check if a P-value is less than 5%
* If that’s the case — reject the H0, if not — there is no evidence that you should reject it.
* In other words P-Value is the following probability: “If we assume that H0 is true, what is the probability of us getting the sample we get?”
* We use p-values to make conclusions in significance testing. More specifically, we compare the p-value to a significance level (alpha) to make conclusions about our hypotheses.

### KNN BASICS

* Tell me who’s your friend and I’ll tell you who you are.
* Model has 2 main parameters: number of neighbors and distance to them.
* Distances: Euclidian, Manhattan, Cosine, Minkowski and others.
* Why KNN: intuitively easy, no need to build a model as your train data set already IS a model (practically), flexible, can work with unclassifiable data.
* Why not: very slow on big sets, need to store your training det as it is your model, curse of dimensionality.
* Errors: type 1 — False Positive (object is wrongly classified as being in a particular class), type 2 — False negative (wrongly NOT classified as being in a particular class).
* Accuracy = (TP+TN)/(TP+TN+FP+FN)
* *Интуитивно понятная, очевидная и почти неиспользуемая метрика. Её главная проблема в том, что она бесполезна в задачах с неравными классами. Например, пусть у нас есть 50 больных и 950 здоровых. Мы хотим научиться их различать. Пусть наш алгоритм предсказывает, что все здоровы. В этом случае доля правильных ответов составит 95%, но алгоритм окажется абсолютно бесполезным. Чтобы избежать таких эксцессов, а также учитывать, что разные типы ошибок могут иметь разную цену, строят другие две метрики: точность и полноту.*
* Precision = TP/TP+FP (важно не сделать ни 1 лишнего обследования)
* *Отражает то, насколько мы можем доверять алгоритму, если он спрогнозировал единичку.*
* Recall = TP/TP+FN (важно не пропустить ни 1 больного!)
* *Показывает, как много объектов первого класса наш алгоритм находит. Введение precision не позволяет нам записывать все объекты в один класс, так как в этом случае мы получаем рост уровня False Positive. Recall демонстрирует способность алгоритма обнаруживать данный класс вообще, а precision — способность отличать этот класс от других классов.*
* from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score
* MAGIC FUNCTION of turning 2 classes to either 1 or 0:
* data[‘class’] = data[‘class’].apply(lambda x: 1 if x==’<write here 1 of 2 class names>’ else 0)

======


