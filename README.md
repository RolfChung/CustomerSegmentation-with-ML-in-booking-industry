# CustomerSegmentation-with-ML-in-booking-industry
Full project on: https://drive.google.com/drive/folders/1lEWgIKNPYTTLPyivwRB9YWVMZsD-Whw2?usp=sharing

<p>
This is only the README file. The full project including notebooks and files is accessed by the hyperlink above.
</p>
<h1>Summary</h1>


<p>
Customer segmentation and profiles provide valuable insights into distinct customer groups and their needs.<br>
Utilising these segments allows for targeted marketing campaigns and personalised incentive programs.<br>
This project aims to create customer segments and assign incentives to the customer groups<br>
for the online booking company Travel Tide.<br>
A company similar to booking.com.
</p>
<p>
The number of incentives assigned to a customer segment can easily be reduced to one.<br>
It is essentially the task of deleting some strings, 
if the Travel Tide Marketing wants only one incentive per customer group.<br>
This question and other need to be discussed,<br>
when creating a Machine Learning pipeline to bring the selected model into marketing production.<br>
More on this below at the end.
</p>

<p>
The benefits of customer segmentation and assignment of incentives are:
</p>

<ul>
<li>Increased customer loyalty and customer satisfaction.</li>
<li>Enhanced sales and revenue</li>
<li>Acquiring new customer groups</li>
<li>Optimised marketing operations and resource allocation</li>
<li>Generate competitive advantage</li>
</ul>

<h2>Methodology</h2>

<p>
In general this data analytics research on Travel Tide customers adapts the CRISP-DM ( Cross-Industry Standard Process for Data Mining) <br>
to structure the project and reduce the complexity. <br>
The coding tools used are Python, Pandas, Scikit, SQL in Google Colab notebooks.
</p>

<p>
The logic of the project structure is aligned with the numbering of the Colab notebooks and goes as follow:
</p>


<h3>Data import and preparation</h3>

<ul>
<li>01_Inspect_Import_Travel:<br>
importing the data and first check</li>
<li>02_Building_Elenas_SQL_base_tables:<br> 
creating a subset of the full Travel Tide dataseta according to the requirements of the 
marketing chief of Travel Tide Elena requirements</li>
<li>03_data_preparation_Travel:<br> 
data cleaning by imputing missing values, removing outliers and duplicates, correcting anomalities and others.</li>

</ul>

<h3>Data exploration</h3>

<ul>
<li>04_data_exploration_Travel:<br>
data exploration and developing insights by reasoning about the data using tables, aggregates and visualizations. </li>
</ul>

<h3>Data modelling preparation</h3>

<p>
The data modelling uses Machine Learning Clusterin algorithms (K-Means, DBSCAN).<br>
These algoritms need numerical data for processing.<br> 
The preparation uses concept like feature extraction, feature matrix and “variance inflation factor” method to reduce to reduce the "Curse of dimensionality".
</p>

<ul>
<li>05_Feature Engineering_Selection_Travel:<br>
creating features and metrics from variables to reduce the "Curse of dimensionality".<br> 
The goals are also to get a higher information value and create variables aligned with numerical modelling algorithms. </li>
<li>06_PCA_Travel:<br>This notebook applies Principal Component Analysis to reduce the complexity of the data set.<br> 
The PCA data sets are inputs to the modelling algorithms. </li>
<li>03_data_preparation_Travel:<br> data cleaning by imputing missing values, removing outliers and duplicates, correcting anomalities and others.</li>
</ul>

<h3>Data modelling</h3>

<p>
Testing out different combinations of input data (PCA's etc) and clustering<br>
This is the most time consuming process in terms of calculation power.<br>
Modern AI applications try to increase the performance trough hardware graphic processors.<br>
The models are evaluated with the Silhouette Score.<br>
According to this score the K-Means model produces the best result performance.
This model is therefore selected.
</p>


<ul>
<li>07a_ULearning_Clustering_KMeans_VIF_Travel: discared model</li>
<li> 07b_Clustering_DBSCAN_Travel: discarded model<br> 
<li>07c_Clustering_KMeans_PCA_Travel: selected model.<br> 
</ul>

<h3>Customer Segmentation and assignment</h3>

<p>
The data set aligned with the final model is selected for the customer segmentation. <br>
The customer segments are based on the identified clusters by K-Means.<br>
Several data wrangling operations were necessary to turn the cluster into segments.<br>
In the next step incentives were assigned to customer segments.<br>
A final data set was then created including segments and incentives.
</p>

<p>
The number of incentives assigned to a customer segment can easily be reduced to one.<br>
It is essentially the task of deleting some strings.<br>
Further discussions with the Travel Tide marketing are necessary to refine the customer segmentation with regard to this.<br>
AS model development is an ongoing communication process with the internal marketing customer this is a normal process.<br>
Anyway it will be necessary to adapt the model further to the emerging marketing requirements, <br>
especially when moving the model from development to production.
</p>


<h2>Explaining the structure of the directory on Google Drive.<h2>

<p>
The main files and Colab notebooks are in the first level<br>
There are several sub folders.<br>
Mostly are self explanatory.
The folder Reporting includes the report and presentation.<br>
In the csv folder is a sub folder with the final_csv.
</p>
