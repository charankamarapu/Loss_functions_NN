# Loss_functions_NN
## Regression Loss Functions :
### Mean Squared Error Loss:
Squared Error loss for each training example, also known as L2 Loss, is the square of the difference between the actual and the predicted values.The corresponding cost function is the Mean of these Squared Errors (MSE).
- Use MSE when doing regression, believing that your target, conditioned on the input, is normally distributed, and want large errors to be significantly (quadratically) more penalized than small ones.
- L=(y-f(x))^2
### Mean Absolute Error Loss:
Absolute Error for each training example is the distance between the predicted and the actual values, irrespective of the sign. Absolute Error is also known as the L1 loss.As I mentioned before, the cost is the Mean of these Absolute Errors (MAE).
- The MAE cost is more robust to outliers as compared to MSE. However, handling the absolute or modulus operator in mathematical equations is not easy. I’m sure a lot of you must agree with this! We can consider this as a disadvantage of MAE.
- L=|y-f(x|
### Huber Loss:
The Huber loss combines the best properties of MSE and MAE. It is quadratic for smaller errors and is linear otherwise (and similarly for its gradient). It is identified by its delta parameter.
## Binary Classification Loss Functions :
### Binary Cross Entropy Loss:
- Let us start by understanding the term ‘entropy’. Generally, we use entropy to indicate disorder or uncertainty. It is measured for a random variable X with probability distribution p(X).
- A greater value of entropy for a probability distribution indicates a greater uncertainty in the distribution. Likewise, a smaller value indicates a more certain distribution.
- This makes binary cross-entropy suitable as a loss function – you want to minimize its value. We use binary cross-entropy loss for classification models which output a probability p.
- L = -log(p) if label==1
- L = -log(1-p) if label==0
- This is also called Log-Loss. To calculate the probability p, we can use the sigmoid function. 
### Hinge Loss:
Hinge loss is primarily used with Support Vector Machine (SVM) Classifiers with class labels -1 and 1.Hinge Loss not only penalizes the wrong predictions but also the right predictions that are not confident.
- L = max(0,1-y*f(x))
- Hinge Loss simplifies the mathematics for SVM while maximizing the loss (as compared to Log-Loss). It is used when we want to make real-time decisions with not a laser-sharp focus on accuracy.
## Multi-Class Classification Loss Functions:
### Multi-Class Cross Entropy Loss:
The multi-class cross-entropy loss is a generalization of the Binary Cross Entropy loss. The loss for input vector X_i and the corresponding one-hot encoded target vector Y_i.

