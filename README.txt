Model Selection via Cross-Validation (CV)**

1. **Objective**

   * Learn how to perform **model selection** using **cross-validation (CV)**.
   * Compare different models and hyperparameters based on **validation performance**, not test performance.
   * Reinforce the idea that **test data should only be used for final evaluation**, not for tuning.

2. **Key Concepts**

   * The goal is to simulate the process of selecting a model in real-world scenarios, where test data is not available during training.
   * Use **Q-Fold Cross-Validation** to:

     * Tune hyperparameters (e.g., K in KNN, λ in RLS/KRLS)
     * Compare different models (e.g., linear vs. non-linear kernels)
   * Select the best configuration based on **average validation error**.

3. **Models to Compare**

   * You may include comparisons between:

     * K-NN
     * RLS (with linear kernel)
     * KRLS (with Gaussian kernel)
   * Analyze how the best model and hyperparameters vary across datasets with different:

     * Sizes
     * Noise levels
     * Dimensions

4. **Workflow Steps**

   * For each model:

     * Define a range of hyperparameters
     * Perform **Q-fold CV** for each value
     * Record:

       * Average training error
       * Average validation error
   * Select the hyperparameter that minimizes **validation error**
   * Report:

     * Final training error on full data
     * (Later: test error if test set is provided)

5. **Analysis Requirements**

   * Create **plots** of error vs. hyperparameter values
   * Include **tables** comparing all models
   * Reflect on:

     * How hyperparameters affect fit/stability
     * How model complexity relates to dataset characteristics
