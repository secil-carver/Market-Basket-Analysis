# Market-Basket-Analysis
[![](https://img.shields.io/badge/Python-blue?style=for-the-badge)](https://github.com/hamzamohdzubair/redant)
[![](https://img.shields.io/badge/ML-MBA-blueviolet?style=for-the-badge)](https://hamzamohdzubair.github.io/redant/)
[![](https://img.shields.io/badge/Library-Mlxtend-yellow?style=for-the-badge)](https://docs.rs/crate/redant/latest)
[![](https://img.shields.io/badge/Algorithm-Apriori-orange?style=for-the-badge)](https://crates.io/crates/redant)
[![](https://img.shields.io/badge/Preprocessing-TransactionEncoder-green?style=for-the-badge)](https://crates.io/crates/redant)
[![](https://img.shields.io/badge/Mining-AssociationRules-red?style=for-the-badge)](https://crates.io/crates/redant)

![](https://img.shields.io/static/v1?label=&message=Seaborn&color=green)
![](https://img.shields.io/static/v1?label=&message=HeatMap&color=blue)


Identifying the frequency of item pair purchases.

### Research Question

Can we make recommendations to customers based on their purchase habits using market basket analysis? 

### Goal of data analysis

The goal is to use market basket analysis to identify items customers buy together and their frequency. In doing so we can make more efficient offers to customers such as promotions, and discounts on item pairs resulting in more customer satisfaction, more sales for the company, and less churn. 

### How market basket analyzes the selected dataset

Market basket analysis is an unsupervised learning method used in the identification of item sets frequently occurring together using a set of criteria. The Apriori algorithm used in market basket analysis first identifies items based on the frequency set by the user. Then the algorithm keeps on expanding the items to item sets until no more pairs can be matched. The association rules can be applied to this determined set of items to highlight general trends in the dataset.

### Summarize one assumption of market basket analysis

One assumption of market basket analysis is that all transactions are in one row and one hot encoded.

### Metrics and their significance

The primary metrics for evaluating the quality of rules for association analysis are Support, Confidence, and Lift. 

<p style="text-align: center;">Support (X->Y) = $\frac{Frequency(XandY)}{N}$</p>

<p style="text-align: center;">Confidence (X->Y) =  $\frac{Support(X->Y)}{Support(X)}$ </p>

<p style="text-align: center;">Lift (X->Y) = $\frac{Support(X->Y)}{Support(X)Support(Y)}$</p>

The significance of Support is the frequency of occurrences of items and itemsets in the transactions. The higher the Support is, the higher the occurrences were. The higher occurrences are of most interest since if items are bought with little frequency, they would be of no interest.

Confidence shows the probability of item combinations occurring together in the same transaction. "Confidence is the conditional probability of the consequent given the antecedent". If this number is low then the probability of the second item being in the same transaction is low.

Lift shows the likelihood of a customer buying both itemsets. Lift > 1 is a positive correlation-increased likelihood, Lift <1 negative correlation-decreased likelihood, Lift = 0 no correlation-no likelihood.
