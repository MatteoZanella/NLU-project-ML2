The models in this folder can be loaded with:
```
import tensorflow as tf


class Perplexity(tf.keras.metrics.Metric):
  ...
def sequence_sparse_categorical_crossentropy(y_true, y_pred):
  ...
 
custom_objects = {"Perplexity": Perplexity, "sequence_sparse_categorical_crossentropy": sequence_sparse_categorical_crossentropy}
model = tf.keras.models.load_model(MODEL_NAME, custom_objects=custom_objects)
```
