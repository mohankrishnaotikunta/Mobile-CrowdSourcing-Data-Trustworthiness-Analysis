Mobile CrowdSourcing – Data Trustworthiness Analysis

This project focuses on identifying trusted and malicious users in Mobile CrowdSourcing (MCS) systems using a hybrid machine learning approach. MCS platforms rely on data collected from users’ smartphones—such as GPS and sensor readings—but the presence of unreliable or malicious contributors can significantly degrade system performance. The goal of this project is to assess data trustworthiness before it is utilized by the system.

Problem Statement: 

In Mobile CrowdSourcing (MCS) environments, data is collected from a large number of users whose identities, intentions, and behaviors are often unknown and uncontrolled. Since participation is open, the system cannot inherently guarantee that all contributors act honestly or provide high-quality data.

Some users may deliberately manipulate sensor readings, submit fabricated or low-effort data, or consume system resources without making meaningful contributions. These behaviors introduce noise and bias into the collected dataset, negatively impacting the reliability of the system.

As a result, Mobile CrowdSourcing platforms may suffer from reduced data quality, inaccurate analytical outcomes, and an overall loss of trust in the system’s outputs. Ensuring the trustworthiness of user-generated data is therefore a critical challenge.

The objective of this project is to automatically classify users as Trusted (1) or Malicious (0) based on their data contributions, enabling the system to filter unreliable inputs before they are used for decision-making or analysis.


Core Approach:

This project implements a hybrid machine learning model that integrates:
1. Generative Adversarial Networks (GANs)
   1) Generate realistic synthetic data samples
   2) Increase dataset diversity
   3) Help the model learn more robust and generalized patterns

2. Random Forest Classifier
   1) Classifies users as trusted or malicious
   2) Efficiently handles high-dimensional feature spaces
   3) Provides strong accuracy, stability, and robustness

The GAN component is used to augment the dataset by generating high-quality synthetic samples, which helps address data imbalance and improves generalization. The Random Forest classifier then leverages both real and synthetic data to perform user classification. By combining GAN-based data augmentation with ensemble learning, the hybrid approach achieves highly reliable and accurate classification results.

Dataset Overview:

The dataset used in this project was generated using the CrowdSenSim simulation tool and consists of approximately 14,000 records. It contains 13 features that capture multiple dimensions of user behavior and contextual information within a Mobile CrowdSourcing environment. These features include spatial attributes such as latitude and longitude, temporal attributes such as day, hour, and minute, as well as device-related metrics like battery requirements and sensing duration.

In addition, coverage and grid-based information is included to represent sensing area characteristics. The target variable is binary, where a value of 1 represents a trusted user and a value of 0 represents a malicious user. By incorporating both spatial and temporal characteristics along with device-level attributes, the dataset enables the model to distinguish between trustworthy and malicious contributors based on behavioral patterns rather than relying on a single indicator.

Results Summary Logistic Regression Accuracy: ~72% Random Forest Accuracy: ~99.8% Hybrid GAN + Random Forest Accuracy: ~99.4%

The results show that synthetic data generation significantly improves model performance and robustness.

Technologies Used Python Jupyter Notebook Pandas, NumPy Scikit-learn TensorFlow / Keras Matplotlib

How to Run '''bash git clone https://github.com/chakrinee/MobileCrowdSourcing.git cd MobileCrowdSourcing pip install -r requirements.txt jupyter notebook

Author(s)  Mohan Krishna Otikunta & Chakrinee Ayalasomayajula
