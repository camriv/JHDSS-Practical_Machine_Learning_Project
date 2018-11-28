# JHDSS-Practical_Machine_Learning_Project
Predicting Qualitative Activity Using Supervised Machine Learning Models

This study presents a supervised machine learning model that predicts the manner in which subjects performed a *unilateral dumbbell biceps curl* according to the measurement methods used and data acquired by Velloso, E. et al (2013) in their study [Qualitative Activity Recognition of Weight Lifting Exercises](http://groupware.les.inf.puc-rio.br/public/papers/2013.Velloso.QAR-WLE.pdf). Measurements from accelerometers on the belt, forearm, arm, and dumbell of six male participants aged 20-28 were recorded while they perform barbell lifts correctly and incorrectly in 5 different ways. Class A corresponds to the specified execution of the exercise, while the other 4 classes correspond to common mistakes.
        
Class| Description
---- | ----------------------------------------
  A  | Exactly according to the specification
  B  | Throwing the elbows to the front
  C  | Lifting the dumbbell only halfway
  D  | Lowering the dumbbell only halfway
  E  | Throwing the hips to the front
        
Machine learning algorithms from the `caret` package in R were used for classification. Models were built initially on a training set, the best performing models stacked using predictions on a validation set, and finally evaluated for generalization (out of sample) accuracies on a testing set.
        
Results showed that model stacking on validation predictions was unnecessary as a **random forest model built on the training data** could already achieve an out of sample accuracy of **99.4%**. This is already equal to the highest accuracy attained by the stacked models. Nonetheless, this study showed that stacking could increase the generalization accuracy for bagging, boosting, and significantly so in linear discriminant analysis (+42.2%).
        
The model was also used to predict 20 different test cases whose classes are unknown.
