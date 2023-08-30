# deep-learning-challenge 
by Andrea Monnerie

## Purpose
  This project is to create a model, with machine learning and neural networks, to predict the success of the nonprofit foundation Alphabet Soup's ventures. The (hypothetical) company wants to select the right ventures and have confidence of the ventures' success. Given, is a CSV file containing more than 34,000 organizations that have received funding from the company with specific details such as "APPLICATION_TYPE", "ORGANIZATION (type)", "ASK_AMT", etc..

## Process and Results

  ### Data Preprocessing

  * target variable(s): 'IS_SUCCESSFUL'
  * features: 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', 'ASK_AMT'
  * variable(s) removed: 'EIN' and 'NAME'

  ### Compiling, Training, and Evaluating the Model

  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
      * hidden layer 1: 80 neurons with "relu" activation function
      * hidden layer 2: 50 neurons with "relu" activation function
      * output layer: 1 neuron with "sigmoid" activation function
      * Epochs: 100
  * Were you able to achieve the target model performance?
      * Accuracy: 0.7261
      * Loss: 0.5571
     
      ![alphabetmodel](https://github.com/amonnerie/deep-learning-challenge/assets/127140876/ae786bf8-6e77-4045-8adf-1101bd5582cd)
  * Attempt to optimization: There were three attempts to make the model accurate at least by 0.75

      Changes in the Data Preprocessing for all three attempts:
      * target variable(s): 'IS_SUCCESSFUL'
      * features: 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'ASK_AMT'
      * variable(s) removed: 'EIN', 'NAME', 'STATUS', 'SPECIAL_CONSIDERATIONS', and 'INCOME_AMT'

      Attempt 1:
      * How many neurons, layers, and activation functions did you select for your neural network model, and why?
          * hidden layer 1: 400 neurons with "relu" activation function
          * hidden layer 2: 300 neurons with "relu" activation function
          * hidden layer 3: 200 neurons with "relu" activation function
          * hidden layer 4: 100 neurons with "relu" activation function
          * hidden layer 5: 50 neurons with "relu" activation function
          * output layer: 1 neuron with "sigmoid" activation function
          * Epochs: 200

      * Were you able to achieve the target model performance?
          * Accuracy: 0.7271 (+0.001)
          * Loss: 0.6120 (+0.0639)
         
          ![optimized1](https://github.com/amonnerie/deep-learning-challenge/assets/127140876/0545bd5f-947f-4a81-a6ec-6dee7f32dbfb)
      
      Attempt 2:
      * How many neurons, layers, and activation functions did you select for your neural network model, and why?
          * hidden layer 1: 200 neurons with "relu" activation function
          * hidden layer 2: 120 neurons with "sigmoid" activation function
          * hidden layer 3: 50 neurons with "relu" activation function
          * output layer: 1 neuron with "sigmoid" activation function
          * Epochs: 200

      * Were you able to achieve the target model performance?
          * Accuracy: 0.7289 (+0.0028)
          * Loss: 0.5585 (+0.0014)
          
          ![optimized2](https://github.com/amonnerie/deep-learning-challenge/assets/127140876/2f2a02e3-5e6a-4150-82d6-29b60ec18887)
      
      Attempt 3:
      * How many neurons, layers, and activation functions did you select for your neural network model, and why?
          * hidden layer 1: 400 neurons with "sigmoid" activation function
          * hidden layer 2: 300 neurons with "relu" activation function
          * hidden layer 3: 200 neurons with "sigmoid" activation function
          * hidden layer 3: 80 neurons with "relu" activation function
          * output layer: 1 neuron with "sigmoid" activation function
          * Epochs: 300
          
      * Were you able to achieve the target model performance?
          * Accuracy: 0.7272 (+0.0011)
          * Loss: 0.5672 (+0.0101)
          
          ![optimized3](https://github.com/amonnerie/deep-learning-challenge/assets/127140876/8d95fd88-ad67-4231-bfff-c22946005b65)

## Conclusion (different model?)
Overall, all the attempts to create the accurate model (including the original one) are all an accuracy of about 0.72 and the loss around 0.55. Opimizating the model was surprising difficult as there are many factors that could be modified. Therefore it is difficult to pin point which modification is improving or worsening the accuracy of the model. Supervised machine learning might be a better method to create an accurate model since supervised learning is good for precision since there is human intervention and this project has enough data to train the model.
