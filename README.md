# Craigslist Housing Price Analysis

## Project Overview
This project aims to model and predict housing prices from Craigslist listings using multiple linear regression models. By analyzing various features such as the type of listing, square footage, number of bedrooms and bathrooms, and amenities like parking options and pet policies, the project seeks to identify the factors that have the most significant impact on housing prices.

## Dataset
The dataset contains Craigslist housing listings and includes the following features:

- **price**: Price of the listing.
- **type**: Type of housing (e.g., apartment, house, etc.).
- **sqfeet**: Square footage of the property.
- **beds**: Number of bedrooms.
- **baths**: Number of bathrooms.
- **comes_furnished**: Whether the listing is furnished or not.
- **laundry_options**: Laundry options available.
- **parking_options**: Parking options available.
- **smoking_allowed**: Whether smoking is allowed.
- **cats_allowed**: Whether cats are allowed.
- **dogs_allowed**: Whether dogs are allowed.

## Methodology
### 1. Data Preprocessing
- Data cleaning and preparation, including handling missing values and encoding categorical variables.

### 2. Model Building
Three models were built incrementally:
1. **Model 1**: Basic model with `type`, `sqfeet`, `beds`, and `baths`.
2. **Model 2**: Added features like `comes_furnished`, `laundry_options`, `parking_options`, and `smoking_allowed`.
3. **Model 3**: Added `cats_allowed` and `dogs_allowed` features.

### 3. Model Evaluation
- **R-squared and Adjusted R-squared**: To evaluate the goodness-of-fit for each model.
- **AIC and BIC**: For model comparison and selection.
- **ANOVA F-Test**: To compare the nested models.
- **Predictive RMSE**: To assess the model's predictive performance on the test dataset.

## Results
- **Model 3** was found to be the best model with an R-squared of `0.2838` and an adjusted R-squared of `0.2777`.
- The ANOVA test indicated that Model 3 significantly improves over Model 2, particularly with the inclusion of pet policies.
- The predictive RMSE for Model 3 was lower than for Model 2, indicating better predictive performance.

## Visualizations
Visualizations are included in the notebook to illustrate the relationships between features and the predicted prices, as well as the distribution of residuals.

## Conclusion
The analysis demonstrates that while adding additional features like pet policies improves the model, the overall explanatory power remains modest. This suggests other factors not captured in this dataset may be more influential in determining housing prices.

## Repository Structure
 
## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/craigslist-housing-analysis.git
    ```
2. Navigate to the project directory:
    ```bash
    cd craigslist-housing-analysis
    ```
3. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```
4. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. Run the Jupyter notebook `housing_analysis.ipynb` to see the complete analysis.
2. Alternatively, run the `analysis.py` script in the `src` folder to execute the core analysis.

## Requirements
- Python 3.7+
- pandas
- numpy
- statsmodels
- matplotlib (for visualizations)

## Future Work
- Explore additional features such as neighborhood and proximity to amenities.
- Apply machine learning algorithms like Random Forest and XGBoost for improved predictive performance.
- Perform hyperparameter tuning to optimize the models.

## Author
**Your Name** - [pcpetty](https://github.com/pcpetty)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
