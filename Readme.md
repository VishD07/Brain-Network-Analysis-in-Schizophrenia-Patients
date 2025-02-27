**Brain Network Analysis in Schizophrenia Patients**

In this project, I tried to explore brain connectivity patterns in schizophrenia patients using functional MRI (Fmri) data from COBRE dataset. The main goal of this project is building a brain networks, analyse how different regions of the brain communicate and what is difference between brain networks of healthy patients and schizophrenia patients.  By comparing this network, I trying to identify patterns link to schizophrenia.

**Dataset**:
I have used *COBRE preprocessed with NIAK 0.17 - lightweight release*. It includes preprocessed resting-state functional magnetic resonance images for 72 patients diagnosed with schizophrenia (58 males, age range = 18-65 yrs) and 74 healthy controls (51 males, age range = 18-65 yrs).  [1]
Methods:
1.	Data is pre-processed data so I directly loaded the dataset.  Brain regions were defined using Harvard-Oxford Altas.
2.	Using Brain regions time-series signal is extracted to see brain regions activity.
3.	Then I calculated Pearson correlation between these signals to measure how strongly different brain regions are connected.
4.	Separated Correlation matrix into patient and controls. And calculate mean correlation matrices for both groups and plotted that for better understanding.
5.	Each correlation matrix was transformed into a “graph-based network”:
Where – **Nodes**: represent brain regions. & **Edges**: represent strong functional connections.

**Used *NetworkX* to construct functional brain networks for patient and control which were used to identify the differences.**

6.	To understand key differences in brain connectivity, I compute various graph-theoretical metrics for both groups: - 
    •	Density measures how interconnected the network is. 
    •	Clustering Coefficient quantifies local connectivity between regions.
    •	Characteristic Path Length determines the efficiency of communication within the brain. 
    •	Betweenness Centrality identifies critical hubs that facilitate information flow

**By comparing these metrics, we can identify connectivity alterations in schizophrenia patients.**

7.	 **Brain regions with the highest centrality measures play crucial roles in information processing**.
    •	Identified top 10 most connected regions in both groups.
    •	Compared Degree Centrality, Betweenness, and Eigenvector Centrality.

8.	 **Global efficiency reflects how effectively different brain regions communicate. A decrease in global efficiency in schizophrenia patients may indicate disrupted functional integration, potentially linked to cognitive impairments**.

9.	By comparing global efficiency between groups, we assess whether schizophrenia is associated with weakened network communication compared to healthy individuals.


Requirements 
To run this project, install the required Python libraries: 
*```bash pip install numpy pandas nibabel nilearn matplotlib seaborn network*

Future Work
Applying deep learning 

References:
Bellec, Pierre; Bellec, Pierre (2016). COBRE preprocessed with NIAK 0.17 - lightweight release. figshare. Dataset. https://doi.org/10.6084/m9.figshare.4197885.v1

https://nilearn.github.io/dev/index.html

https://networkx.org/documentation/stable/tutorial.html




 


