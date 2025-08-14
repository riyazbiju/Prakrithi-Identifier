**Prakriti Prediction using Artificial Neural Networks**

This was my first experiment with neural networks back in 2021.
Prakriti, in Ayurveda, describes a person’s natural constitution -> Vata (air & space), Pitta (fire & water), or Kapha (earth & water).
This project uses an MLPClassifier to analyze responses from a questionnaire about physical and mental traits, predict the dominant prakriti type (or combination), and display the results with percentage breakdowns and a pie chart visualization.

**Overview**

The implementation predicts the Ayurvedic constitution (Vata, Pitta, Kapha) by:
 * Training an ANN model (`MLPClassifier`) using physical and mental trait data
 * Accepting questionnaire-based user input for multiple features
 * Calculating percentages for Vata, Pitta, and Kapha
 * Displaying results both as text and in a pie chart

**Prerequisites**

Install the required Python libraries:

```bash
pip install pandas matplotlib scikit-learn
```

**File Structure**

* `prakriti_prediction.py` - Contains the complete ANN code and questionnaire logic
* `prakriti_fnal_number_data.csv` - Dataset with labeled prakriti values

**Key Components**

1. **Data Loading and Preprocessing**
   * Reads CSV dataset using pandas
   * Splits features and labels (`prakriti` column)

2. **Model Training**
   * Uses `MLPClassifier` with 2 hidden layers (100 neurons each)
   * Activation function: ReLU
   * Optimizer: Adam

3. **Questionnaire Input System**
   * Prompts user for 1, 2, or 3 for each physical/mental characteristic
   * Maps numeric values to descriptive options

4. **Prediction Logic**
   * Counts majority trait category (Vata, Pitta, Kapha)
   * Handles single or dual prakriti predictions
   * Calculates percentage distribution

5. **Visualization**
   * Generates a pie chart showing the prakriti percentages

**Example Output**

```
The predicted prakrithi is: vata
Percentage Vata: 60.0 %
Percentage Pitta: 30.0 %
Percentage Kapha: 10.0 %
```
_A pie chart will also be displayed._

**Acknowledgment**

This project is inspired by the traditional Ayurvedic prakriti assessment method and implemented as part of a learning exercise in machine learning.
