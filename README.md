Firstly i downloaded this well log data from the open source data of the official norwigean website **equinor - VOLVE**

Data Understanding and Units

**DEPTH:** Measured in meters or feet, indicating the depth of the well.

**Compressional Slowness:** Typically measured in microseconds per foot (µs/ft), indicating the time it takes for a compressional wave to travel through the formation.

**GR (Gamma Ray):** Measured in API units, indicating the natural radioactivity of the formation, used to identify shales.

**Neutron Porosity:** Measured as a fraction or percentage, indicating the hydrogen content and indirectly the porosity.

**Bulk Density:** Measured in grams per cubic centimeter (g/cm³), indicating the density of the formation.

**Bulk Volume Water:** Measured as a fraction or percentage, indicating the volume of water in the formation.

**Horizontal Permeability:** Measured in millidarcies (mD), indicating the ability of the formation to transmit fluids.

**Effective Porosity:** Measured as a fraction or percentage, indicating the interconnected pore volume.

**SW (Water Saturation):** Measured as a fraction or percentage, indicating the proportion of pore space filled with water.

**VSH (Volume of Shale):** Measured as a fraction or percentage, indicating the volume of shale in the formation.


The Steps of model creating

**Step 1: Handling Outliers with Domain Knowledge**

Outliers in well log data can result from various factors such as tool malfunctions or abrupt changes in lithology. We should carefully consider these factors and possibly retain some outliers that are geologically meaningful.

**Step 2: Normalize the Data**

Normalization should be done considering the ranges and units of the data. For example, porosity and saturation values are already in the range of 0 to 1, while others like compressional slowness and gamma ray might have different scales.

**Step 3: Feature Selection Based on Domain Knowledge**

Certain features might have stronger relationships with permeability. For instance, effective porosity and bulk density are likely to be more directly related to permeability than gamma ray.

**Step 4: Model Training and Evaluation**

We should use appropriate metrics and visualize the results in a manner that reflects domain-specific insights.

Here are the results and visualizations for predicting permeability using various machine learning models:

**Linear Regression**

MAE: 0.0182

MSE: 0.0011

**Decision Tree**

MAE: 0.0170

MSE: 0.0010

**Random Forest**

MAE: 0.0113

MSE: 0.0005

**Gradient Boosting**

MAE: 0.0126

MSE: 0.0006

**SVR**

MAE: 0.0185

MSE: 0.0011

**Neural Network**

MAE: 0.0148

MSE: 0.0008

**Conclusion**

The Random Forest Regressor performed the best with the lowest MAE (0.0113) and MSE (0.0005), indicating it predicted permeability most accurately among the models tested.

Gradient Boosting and Neural Network also performed well, but Random Forest had a slight edge in terms of accuracy.

Decision Tree showed reasonable performance, but simpler models like Linear Regression and SVR were less accurate in comparison.

These results suggest that ensemble methods like Random Forest and Gradient Boosting are effective for predicting permeability from well log data.
