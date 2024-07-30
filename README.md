# Module 19 Challenge - Neural Network Challenge 2

## Background
In the assignment, you are tasked with creating a neural network that HR can use to predict whether employees are likely to leave the company. Additionally, HR believes that some employees may be better suited to other departments, so you are also asked to predict the department that best fits each employee. These two columns should be predicted using a branched neural network.<br />
Files

## Code Source
The code location is: [Click Here to view](https://github.com/jaidevkler/neural-network-challenge-2)

## Files
attrition.ipynb [Click here to view](https://github.com/jaidevkler/neural-network-challenge-2/blob/main/attrition.ipynb)<br />

## How to run the program
Download the files and then use jupyter notebook or jupyter lab to open the attrition.ipynb file.<br />

## Instructions
* Part 1: Preprocessing
    * Import the data and view the first five rows.<br />
    * Determine the number of unique values in each column.<br />
    * Create y_df with the attrition and department columns.<br />
    * Create a list of at least 10 column names to use as X data. You can choose any 10 columns you’d like EXCEPT the attrition and department columns.<br />
    * Create X_df using your selected columns.<br />
    * Show the data types for X_df.<br />
    * Split the data into training and testing sets.<br /> 
    * Convert your X data to numeric data types however you see fit. Add new code cells as necessary. <br />
    * Make sure to fit any encoders to the training data, and then transform both the training and testing data.<br />
    * Create a StandardScaler, fit the scaler to the training data, and then transform both the training and testing data.<br />
    * Create a OneHotEncoder for the department column, then fit the encoder to the training data and use it to transform both the training and testing data.<br />
    * Create a OneHotEncoder for the attrition column, then fit the encoder to the training data and use it to transform both the training and testing data.<br />

* Part 2: Create, Compile, and Train the Model
    * Find the number of columns in the X training data.
    * Create the input layer. Do NOT use a sequential model, as there will be two branched output layers.
    * Create at least two shared layers.
    * Create a branch to predict the department target column. Use one hidden layer and one output layer.
    * Create a branch to predict the attrition target column. Use one hidden layer and one output layer.
    * Create the model.
    * Compile the model.
    * Summarize the model.
    * Train the model using the preprocessed data.
    * Evaluate the model with the testing data.
    * Print the accuracy for both department and attrition.

* Part 3: Summary
    * Is accuracy the best metric to use on this data? Why or why not?
        * Accuracy is not always the best way to measure how good the model is. If most employees stay and only a few leave, the model might just predict that everyone stays to get a high accuracy. Instead, we should look at how well the model predicts the employees who actually leave. Metrics like precision (how many predicted leavers actually leave) and recall (how many actual leavers were correctly predicted) are better for this.
    * What activation functions did you choose for your output layers, and why?
        * For predicting if an employee will leave (yes or no), I used the sigmoid function. This function gives a result between 0 and 1, which is perfect for yes/no questions. For predicting the best department for an employee, I used the softmax function. This function gives a probability for each department, showing which one is most likely the best fit.
    * Can you name a few ways that this model could be improved?
        * Few ways to improve the model: 
            * Add More Useful Data: Create new features from the existing data that might be more helpful for the predictions.
            * Fine-Tune Settings: Adjust the model's settings like the number of layers and neurons to find the best combination.
            * Prevent Overfitting: Use techniques like dropout (randomly turning off some neurons during training) or L2 regularization to make sure the model doesn't just memorize the training data.
            * Test More Thoroughly: Instead of just splitting the data once, use different parts of the data to train and test the model multiple times to get a better sense of its performance.
            * Combine Models: Use multiple models and combine their predictions to get better results than a single model.
            * Balance the Data: If some departments have a lot more employees than others, balance the data by either adding more samples for smaller departments or creating synthetic data to even things out.

## Reference
Columbia AI Bootcamp - Module 19 Challenge<br />
Data: https://static.bc-edx.com/ai/ail-v-1-0/m19/lms/datasets/attrition.csv


