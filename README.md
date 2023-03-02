# DONORS-CHOOSE-LSTM
1. Preprocess all the Data we have in DonorsChoose Dataset use train.csv
2. Combine 4 essay's into one column named - 'preprocessed_essays'. 
3. After step 2 you have to train 3 types of models as discussed below. 
4. For all the model use 'auc' as a metric. check this for using auc as a metric 
5. You are free to choose any number of layers/hiddden units but you have to use same type of architectures shown below. 
6. You can use any one of the optimizers and choice of Learning rate and momentum, resources: cs231n class notes, cs231n class video. 
7. For all the model's use TensorBoard and plot the Metric value and Loss with epoch. While submitting, take a screenshot of plots and include those images in .ipynb notebook and PDF. 
8. Use Categorical Cross Entropy as Loss to minimize.
Model-1
Build and Train deep neural network as shown below
![alt text](https://i.imgur.com/w395Yk9.png)
Input_seq_total_text_data --- You have to give Total text data columns. After this use the Embedding layer to get word vectors. Use given predefined glove word vectors, don't train any word vectors. After this use LSTM and get the LSTM output and Flatten that output.
Input_school_state --- Give 'school_state' column as input to embedding layer and Train the Keras Embedding layer.
Project_grade_category --- Give 'project_grade_category' column as input to embedding layer and Train the Keras Embedding layer.
Input_clean_categories --- Give 'input_clean_categories' column as input to embedding layer and Train the Keras Embedding layer.
Input_clean_subcategories --- Give 'input_clean_subcategories' column as input to embedding layer and Train the Keras Embedding layer.
Input_teacher_prefix --- Give 'input_teacher_prefix' column as input to embedding layer and Train the Keras Embedding layer.
Input_remaining_teacher_number_of_previously_posted_projects._resource_summary_contains_numerical_digits._price._quantity ---concatenate remaining columns and add a Dense layer after that.
For LSTM, you can choose your sequence padding methods on your own or you can train your LSTM without padding, there is no restriction on that.
