# Cancer-Molecular-Classification
A study of various ML methods to classify Leukemia from gene expression monitoring.

This study is based on a proof of concept study published in 1999 by Golub et al.<sup>1</sup>  
The dataset is available at Kaggle : https://www.kaggle.com/crawford/gene-expression#data_set_ALL_AML_independent.csv

Machine learning (ML) has been gaining a lot of popularity in medicine where it helps predict or classify various medical conditions in patients. Leukemia classification has been studied in 1999 by Golub et al. It uses an approach called SOM (self organising maps) which classifies patients having leukemia into acute myeloid leukemia (AML) and acute lymphoblastic leukemia (ALL), based on gene expression monitoring by DNA microarrays. 

The attached notebook provides work that helps to answers a question about what type of results we could obtain by using modern ML algorithms. The ML algorithms come from the scikit-learn library to classify the dataset. An alternative method proposed by McClintick and Edenberg<sup>2</sup> is also studied and compared to the ML solutions.

The rsults show that the Random Forest ML algorithm provides the highest ML score. For this reason it was selected as the ML algorithm to complement other, such PCA, Golup et al., etc. The Golup et al. method provides the highest overall score. PCA with random forest gives the fastest time and a lesser score than random forest alone, which is expected. 
<br><br>

| Method | Score (%) | Execution Time |
|---|:---:|---|
| Golup et al., Random Forest	|  70.6	| 11.4 ms ± 5.32 ms per loop (mean ± std. dev. of 7 runs, 10 loops each) |
| Extra Tree	                |  67.6	| 160 ms ± 29.4 ms per loop (mean ± std. dev. of 7 runs, 1 loop each) |
| Random Forest	              |  67.6	| 183 ms ± 63.1 ms per loop (mean ± std. dev. of 7 runs, 1 loop each) |
| PCA, Random Forest	        |  64.7	| 10.2 ms ± 1.17 ms per loop (mean ± std. dev. of 7 runs, 10 loops each) |
| kNN	                        |  64.7	| 66.6 ms ± 9.43 ms per loop (mean ± std. dev. of 7 runs, 10 loops each) |
| 50% Present, Random Forest	|  61.8	| 57.3 ms ± 23.6 ms per loop (mean ± std. dev. of 7 runs, 1 loop each) |
| AddaBoost	                  |  61.8	| 137 ms ± 55.2 ms per loop (mean ± std. dev. of 7 runs, 1 loop each) | 
| Decision Tree	              |  61.8	| 121 ms ± 40.7 ms per loop (mean ± std. dev. of 7 runs, 10 loops each) |
| Logistic	                  |  58.8	| 299 ms ± 172 ms per loop (mean ± std. dev. of 7 runs, 1 loop each) |
| KMeans	                    |  55.9	| 189 ms ± 19.6 ms per loop (mean ± std. dev. of 7 runs, 1 loop each) |

<br><br>
<sup>1</sup> Golub T. R., Slonim D. K., Tamayo P., et al. Molecular classification of cancer: class discovery and class prediction by gene expression monitoring. Science. 1999;286(5439):531–537. doi: 10.1126/science.286.5439.531

<sup>2</sup> McClintick JN, Edenberg HJ. Effects of filtering by Present call on analysis of microarray experiments. BMC Bioinformatics. 2006;7:49. Published 2006 Jan 31. doi: 10.1186/1471-2105-7-49
