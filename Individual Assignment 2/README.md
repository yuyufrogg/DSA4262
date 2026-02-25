# About The Project
A key challenge in AI for mental health is to quantify subjective and “invisible” experiences. While clinical settings provide structured data, much of our modern mental health discourse happens in informal digital spaces. In this second Individual Assignment, I develop a predictive model to detect stress signals in social media text using the [Dreaddit dataset](https://aclanthology.org/D19-6213.pdf). Specifically, the project implements a binary text classification model to distinguish between “Stressed” and “Non-stressed” posts across multiple Reddit communities.

# Getting Started
## Prerequisites
The following Python packages are required to run the notebooks. Please ensure they are installed before execution:   

```python
pip install torch
pip install pandas numpy matplotlib seaborn
pip install transformers
pip install scikit-learn
pip install wordcloud
pip install captum
pip install scipy
```
If you are running the notebooks on a CUDA-capable system, please install the appropriate CUDA-enabled version of PyTorch for your machine. Detailed installation instructions can be found on the [official PyTorch website](https://pytorch.org/get-started/locally/).

## Downloading Required Files
There is no need to re-run the Model Training and Validation notebook, as the trained model has been saved as a .pkl file. However, due to GitHub’s file size limitations, the model.pkl file has been uploaded externally on my OneDrive [here](https://nusu-my.sharepoint.com/:u:/g/personal/e0970506_u_nus_edu/IQB8o5vpF0lOT7wsWtDwRNylAfdRbrpPKSSvfhZb6nLYHT8?e=y00mjI) for downloading. Do note that you have to be signed in to your NUS organizational account to be able to access the file. In case the link above fails, you can also find the file [here](https://drive.google.com/file/d/1WGUQidzypyy95irjXzyE2YvNTbbRd-Oh/view?usp=sharing) as well. Please download the model file before running the Model Testing and Analysis notebook.

For ease of execution, it is recommended that the notebooks, dataset files, and model.pkl file are placed within the same directory. This will allow the code to run without requiring modifications to file paths.  

# Brief Overview 
This project builds and evaluates a BERT-based stress classification model trained on Reddit posts from the Dreaddit dataset. Beyond predictive performance, the project also explores linguistic features and analyses to better understand how stress manifests in online discourse, and the limitations of the model. Specifically, the contents in the 2 notebooks will cover:
1. Model Training and Validation (data preparation, tokenization, hyperparameter tuning)
2. Model Testing
3. Analysis
  - Stress Expression - Which words contribute the most to stress prediction?
    - Top words that contribute towards predicting stress (overall)
    - Comparing top stress-predictive words between each subreddit
  - Investigating Cases of Wrong Predictions
    - False negatives ('stress' posts predicted wrongly to be 'non-stress')
    - False positives ('non-stress' posts predicted wrongly to be 'stress')
    - Diving further into false negative cases by comparing them with true positives (rightly predicted 'stress' posts)
  - Ease of Prediction - Which subreddits are easier to predict?
4. Potential Real-World Applications of the Model
5. Risks
6. Conclusion
