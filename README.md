# The King, the Queen, and the all-seeing Fish
## Problem Statement
---
**Goal:** The goal of this assignment is to evaluate a chessboard given in Forsyth-Edwards Notation (FEN). One is expected to assign a numerical score to the given chessboard, correlating with how useful the current state will be in winning. The assignment consists of both a **Non-Competitive** and a **Competitive** part.  

### Description  

Descriptions of the **Competitive** and **Non-Competitive** Portions are given below:  

#### Non-Competitive Part  

1. **Data Pre-processing**  
    - Create a function that re-writes the data in a simpler format.  

2. **Exploratory Data Analysis (EDA)**  
    - Identify and remove outlier values for the evaluated scores.  
    - Check the distribution of the evaluated scores.  
    - Plot graphs for different possible features of the board in comparison to the evaluated scores (e.g., the number of pieces on the board vs. the evaluated score).  

3. **Feature Engineering**  
    - Try various encoding methods for the chess boards.  
    - Convert the given chessboard into a format that can be best fed into a neural network.  
    - Compare the results for different formats (at least two) without the addition of more features.  

4. **Neural Network Training and Analysis**  
    - Train a baseline neural network with the above feature-engineered data (only the FEN format is encoded, no new feature columns are added).  
    - Explore different optimizers and select the best one for this case.  
    - Perform hyperparameter tuning.  
    - Analyze and compare accuracies when:  
      - The number of training epochs is varied.  
      - The amount of training data is varied.  
    - Determine whether it is better to train with limited data on multiple epochs or with more data on fewer epochs.  

> **Note:** Document your observations in the report for each section.  

---

#### Competitive Part  

- Based on EDA, find **two unique new features** that can improve accuracy.  
- Train the neural network with each of these features added to show improvement in accuracy.  
- Try using other techniques for the prediction of evaluation scores (excluding pre-trained engines and models) and compare their accuracies.  

Ensure that all enhancements and modifications attempted in this section are **thoroughly documented** in the report.  

---

### Evaluation  

- A certain (as yet undisclosed) weightage will be given to both the **competitive** (based on position on the leaderboard) and **non-competitive** parts.  
- Reports will also be graded individually.  

The CSV submitted for the leaderboard should contain the following two columns:  

- **'ID'** - which contains the FEN format for the instance.  
- **'Evaluation'** - which contains the evaluated score corresponding to the chessboard position.  
---

## Our Implementation  

- We've provided the **sliced_datasets** on which we do most of our testing. The final training dataset can be obtained from [Kaggle - Chess Evaluations](https://www.kaggle.com/datasets/ronakbadhe/chess-evaluations/) (this needs to be pre-processed and cleaned).  
- Feel free to try our model @ [mtl782-chessapp on Streamlit](https://mtl782-chessapp.streamlit.app).  
  The model file is available @ [GitHub - chessapp](https://github.com/harshit1912003/chessapp).
