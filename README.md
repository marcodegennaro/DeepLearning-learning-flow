## My Approach to Studying Deep Learning and PyTorch

**My Goal:** I do not want to just learn the mathematical theory. I want to understand how Deep Learning works in practice through code. For this reason, my approach is practical, iterative, and focused on model architecture.

Since I have already built the basic PyTorch pipeline from scratch (data loading, training loop, validation, and model structure), I will focus on these pillars:

* **No Data Cleaning (To Save Time):** I will use ready-made, clean datasets. This allows me to skip the boring part of cleaning raw data and focus 100% on how the models perform.

* **Two Separate Test Benches, Matched to Data Structure:** Comparing all architectures on one single dataset is misleading, since each architecture is designed for a specific data structure. So I will split the comparison in two:
  - **Bench 1 (spatial structure): MLP vs CNN**, using **MNIST** or **FashionMNIST**. I will feed the same flattened image to the MLP and the raw image to the CNN, to directly observe the effect of ignoring vs exploiting spatial structure.
  - **Bench 2 (sequential structure): RNN/LSTM vs Transformer**, using a text classification dataset (e.g. **IMDB reviews**) or, closer to my thesis work, a small public dataset of **DNA/protein sequences** with known classes (Kaggle or UCI ML Repository). This also doubles as direct practice for my thesis problem.

* **Same Pipeline, Swap Only the Model:** I will keep my existing pipeline as the test bench and change only the model inside, for both benches above. This will help me see how each model handles tensors and how each new model addresses the limits of the previous one.

* **Predict Before Running:** Before training each new model, I will write down what I expect to happen (accuracy, training speed, number of parameters) compared to the previous model. This turns each comparison into an actual test of my theoretical understanding, not just passive observation of results.

* **AI as a Code Reviewer, Not a Code Writer:** I will use AI assistants in Google Colab for peer-review: finding bugs, checking tensor shapes, and learning industry best practices (e.g. GPU memory management, Mixed Precision Training). For tensor/shape debugging this is reliable. For conceptual explanations, I will keep asking "why" and verifying the answer myself, rather than accepting a plausible-sounding explanation at face value.
