Part 1 Preparation:
	1.	Data Augmentation: We used random flips and rotations to help the model generalize better.
	2.	Data Inspection: We checked how many images each class has (to detect imbalances) and visualized a few random examples.
	3.	Class Distribution: A simple bar chart shows if some classes are underrepresented or if the data looks noisy.
	4.	DataLoaders: These help load and batch images efficiently, especially with shuffling for the training set.


Here’s a  plan for the next steps:
	•	Metrics:
	    •	Primary metric: Accuracy (how many images are classified correctly).
	    •	Additionally, consider Precision, Recall, and F1-score for each class if class imbalance becomes an issue.
	    •	A confusion matrix will help visualize where the model might be misclassifying.
	•	Neural Network Architecture:
	    •	Convolutional Layers: Use around 3-4 convolutional layers to capture different levels of features.
	    •	Activations: Stick with ReLU for most layers since it’s simple and effective.
	    •	Pooling Layers: Insert MaxPooling layers after some convolution blocks to reduce spatial dimensions and control overfitting.
	    •	Fully-connected Layers: Use 1-2 FC layers (e.g., one hidden dense layer before the final output layer) to combine the features.
	•	Dropout: Apply Dropout (e.g., 0.5 rate) in the FC layers (or even after convolution blocks) to help prevent overfitting.
	•	Optimizer:
	    •	Consider using the Adam optimizer with a learning rate around 0.001 (tweak as necessary based on experiments).
	    •	Optionally, you might experiment with SGD with momentum if you need more control over training dynamics.
