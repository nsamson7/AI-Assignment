# Load the Data and Data Wrangling

- Using this file, **`card_transdata.csv`**, import the following necessary libraries:  
  `pandas`, `seaborn`, `matplotlib.pyplot`, and `plotly.express`.

- Assign the file name into `file_path`.  

- Load the credit card fraud detection dataset using `pd.read_csv()` and assign it to `transaction_data_raw`.

- Display the first few rows of the dataset using `.head()` and general information such as the shape and using `.info()`.

- Check for missing values in the dataset, drop any rows with null values, and then display the first few rows of the cleaned dataframe.


---

# Visualize the Data

- Create a plot of the class distribution, making **`fraud`** as the x-axis and the title **“Fraud Class Distribution”**. Display the plot.

- Create a plot of the used pin number distribution, making **`used_pin_number`** as the x-axis and the title **“Used Pin Distribution”**. Display the plot.

- Create a plot of the repeat retailer distribution, making **`repeat_retailer`** as the x-axis and the title **“Repeat Retailer Distribution”**. Display the plot.

- Create a plot of the online order distribution, making **`online_order`** as the x-axis and the title **“Online Order Distribution”**. Display the plot.

- Create a histogram using seaborn to display the distribution of **`ratio_to_median_purchase_price`** with 30 bins and titled **“Ratio to Median Purchase Price Distribution”**. Display the plot.

- Create a histogram using seaborn to display the distribution of **`distance_from_home`** with 30 bins and titled **“Distance From Home Distribution”**. Display the plot.


---

# Bivariate Visualizations

### 1. Transactions with PIN vs. Fraudulent Transactions
- Create a plot using seaborn comparing the total number of fraudulent and non-fraudulent transactions with a used-pin or none used-pin with those transactions.  
- Make **`used_pin_number`** as the x-axis, **`fraud`** as the hue, and the palette being green and red.  
- Title this plot **“Transactions with PIN vs. Fraudulent Transactions”**.  
- Label the x-axis **“Used Pin”** and the y-axis **“Count”**.  
- Produce a legend for the plot titled **“Fraud”** and the labels being **“Non-Fraudulent”** and **“Fraudulent”**.  
- Display the plot.


### 2. Percentage of Fraudulent Transactions with PIN Usage
- Create a plot using seaborn to show the percentage of fraudulent transactions when a PIN was used or not.  
- Using the cleaned dataframe, group by **`used_pin_number`** and take the `value_counts()` of **`fraud`**, setting `normalize=True`.  
- Assign this computation to **`df_pin_fraud`**.  
- Plot **`df_pin_fraud`** and make it a stacked bar chart.  
- Set color to **green** and **red** and make the figure size **5 by 3**.  
- Title the plot **“Percentage of Fraudulent Transactions with PIN Usage”** and label the x-axis **“Used PIN”** and the y-axis **“Percentage”**.  
- Create a legend titled **“Fraud”** with the labels **“Non-Fraudulent”** and **“Fraudulent”**.  
- Display the plot.


### 3. Transactions with Chip vs. Fraudulent Transactions
- Create a countplot to show the number of transactions that were fraudulent vs. non-fraudulent when a chip was used or not.  
- Make the figure size **5 by 3**, set **`used_chip`** as the x-axis, **`fraud`** as the hue, and the palette **green** and **red**.  
- Title the plot **“Transactions with Chip vs Fraudulent Transactions”**, set the x-axis label to **“Used Chip”** and the y-axis label to **“Count”**.  
- Create a legend titled **“Fraud”** with the labels as **“Non-Fraudulent”** and **“Fraudulent”**.  
- Display the plot.


### 4. Percentage of Fraudulent Transactions with Chip Usage
- Create a percentage plot to show the percentage of fraudulent transactions when the chip was used or not.  
- Using the cleaned dataframe, group by **`used_chip`** and take the `value_counts()` of **`fraud`** setting `normalize=True`, then `unstack()` and multiply all values by 100.  
- Assign this computation to **`df_chip_fraud`**.  
- Plot **`df_chip_fraud`** as a stacked bar chart, with the colors **green** and **red** and figure size **5 by 3**.  
- Title the plot **“Percentage of Fraudulent Transactions with Chip Usage”**, label the x-axis **“Used Chip”**, and label the y-axis **“Percentage”**.  
- Create a legend titled **“Fraud”** with the labels **“Non-Fraudulent”** and **“Fraudulent”**.  
- Display the plot.


### 5. Transactions with Online Order vs. Fraudulent Transactions
- Create a countplot to show the number of transactions that were fraudulent vs. non-fraudulent when it was an online order or not.  
- Make the figure size **5 by 3**, set **`online_order`** as the x-axis, **`fraud`** as the hue, and the palette **green** and **red**.  
- Title the plot **“Transactions with Online Order vs Fraudulent Transactions”**, set the x-axis label to **“Online Order”** and the y-axis label to **“Count”**.  
- Create a legend titled **“Fraud”** with the labels as **“Non-Fraudulent”** and **“Fraudulent”**.  
- Display the plot.


### 6. Scatter Plot — Distance From Home vs. Ratio to Median Purchase Price
- Create a scatter plot using seaborn to show the breakdown of fraudulent and non-fraudulent transactions.  
- Make it a **10 by 6** figure, with the x-axis **`distance_from_home`** and the y-axis **`ratio_to_median_purchase_price`**.  
- Set the hue to **`fraud`** and the palette **green** and **red**, making `0` green and `1` red.  
- Title the plot **“Fraudulent vs Non-Fraudulent Transactions: Distance From Home vs Ratio to Median Purchase Price”**.  
- Label the x-axis **“Distance From Home”** and the y-axis **“Ratio to Median Purchase Price”**.  
- Display the plot.


### 7. Scatter Plot — Distance From Last Transaction vs. Ratio to Median Purchase Price
- Create a scatter plot using seaborn to show the breakdown of fraudulent and non-fraudulent transactions.  
- Make it a **10 by 6** figure, with the x-axis **`distance_from_last_transaction`** and the y-axis **`ratio_to_median_purchase_price`**.  
- Set the hue to **`fraud`** and the palette **green** and **red**, making `0` green and `1` red.  
- Title the plot **“Fraudulent vs Non-Fraudulent Transactions: Distance From Last Transaction vs Ratio to Median Purchase Price”**.  
- Label the x-axis **“Distance From Last Transaction”** and the y-axis **“Ratio to Median Purchase Price”**.  
- Display the plot.
