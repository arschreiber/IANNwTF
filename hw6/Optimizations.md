# Without Optimization
```
Epoch 24: loss: 0.5693933367729187
Epoch 24: categorical_accuracy: 0.8008400201797485
Epoch 24: val_loss: 0.7264575362205505
Epoch 24: val_categorical_accuracy: 0.7523999810218811
```

It is clearly visible that after 25 epochs, the model is overfitting, as the training loss is quite a bit smaller than the validation loss.

# 1. Early Stopping
As can be seen, in our model without optimization, in the last epoch the validation loss did rather increase than decrease. Therefore, if the model weights are stored every iteration (every iteration, admittedly is a bit excessive) it has the following results.
```
Epoch 23: loss: 0.5760889053344727
Epoch 23: categorical_accuracy: 0.799340009689331
Epoch 23: val_loss: 0.6896076798439026
Epoch 23: val_categorical_accuracy: 0.7638999819755554
```

# 2. L1 Regularization
L1 regularization works by introducing a loss, penalizing the absolute value of weights. This leads to a model, where more parameters are close to zero, which leads to a simpler model.
```
Epoch 24: loss: 0.5764498114585876
Epoch 24: categorical_accuracy: 0.8006200194358826
Epoch 24: val_loss: 0.7099658250808716
Epoch 24: val_categorical_accuracy: 0.7573999762535095
```

# 3. L2 Regularization
L2 regularization is like L1 regularization, but penalizing the square of the weights instead.
```
Epoch 24: loss: 0.5678015947341919
Epoch 24: categorical_accuracy: 0.8010200262069702
Epoch 24: val_loss: 0.7048450708389282
Epoch 24: val_categorical_accuracy: 0.7597000002861023
```

# 4. Dropout
Dropout works by randomly dropping neurons during training. This leads to a model, that should generalize better, as it cannot rely on every single neuron output.
```
Epoch 24: loss: 0.6575191020965576
Epoch 24: categorical_accuracy: 0.769819974899292
Epoch 24: val_loss: 0.7402209639549255
Epoch 24: val_categorical_accuracy: 0.7473000288009644
```

# 5. Label Smoothing
Label smoothing works by penalizing overconfident decisions from the model, leading to better generalization of the model.
```
Epoch 24: loss: 0.993206262588501
Epoch 24: categorical_accuracy: 0.8141199946403503
Epoch 24: val_loss: 1.069048523902893
Epoch 24: val_categorical_accuracy: 0.7724000215530396
```

# Results
As can be seen, none of the techniques really helped with the overfitting problem individually.