# Title: User Profiling on Twitter

## Abstract
In the original paper, the postulated sampling method was applied to generate a random sample of Twitter users which was then used to replicate 10 different propositions. Making use of this random sample, we propose to answer additional questions regarding the users of Twitter – in particular we aim to detect clusters of users based on their profiles and behaviour. We define profiles using features that are transformed from information such as `followers_count`, `friends_count` or from aggregated information from the individual's tweets. The behaviour is then limited to the activity of a user, computing the number of tweets, retweets or URLs used. Therefore, in order to improve the learning, we will apply encodings on various selected features, then proceed to clustering. Once we have obtained the clusters, we will attempt to  interpret the clusters and also study the typical user behaviour over time for each group, focusing on the neighbours of the centroids. Visualisations of the clusters in a projected feature space will also be considered. 

## Research questions
1. After detecting groups of users with similar profiles, can these be linked to the category of users (e.g. influencer, spammer, news…)?
2. Within these groups, how does the typical user behaviour change over time, i.e. since their first Tweet?
Do they tweet less or more? Do they get more retweets? 
Does the style change (e.g. more hashtags, URLs, mentions…)? 

## Proposed datasets
`EgoTimelines` and `EgoAlterProfiles` from the paper: these provide a random sample of users together with their networks and tweets. If necessary, the Twitter API can be queried to extract further information on the users.

## Methods
- Data preparation: Since the data is already available from the paper, we will mainly focus on the preparation and selection of the features for clustering. This may require further preprocessing needed (e.g. missing values handling) and the formulation of additional features that can be useful for the similarity computation – these might include average number of hashtags/URLs/mentions per user, fraction of retweets/replies etc. Then we normalize these values for better algorithm application.
- Group detection: We will explore various unsupervised learning algorithms to form the clusters, including K-means and DBSCAN. We expect that the interpretation of the clusters will be difficult and require some prior research. If it turns out to be unsuccessful, the subsequent analysis still provides an interesting insight.
- Visualisation of groups: We will use methods such as PCA and t-SNE to display the user groups in a low-dimensional space. (using their profiles)
- Data analysis: The goal is to uncover user clusters – we want to find out how many types of users can be detected and how well represented each group is. From the clustering we will analyse the evolution of the behaviour based on tweets of users in each group, focusing on the activity and the writing style (use of URLs). In order to account for discrepancies regarding the different account creation dates, we will use the offset from the creation date instead. We will need to find a solution for how to deal with different lengths of user account periods, such as including confidence intervals.

## Proposed timeline
- Week 1: create extra features to help clustering; implement the clustering algorithms and explore the semantic meaning of clusters. Read some literature about existing behaviours to justify the labelling of these clustering, the mentioned extra features could also be derived from these papers for comparability sake. 
- Week 2: visualization of the results; analysis of behavioural (number of tweets, urls usage, retweets per day) evolution for each group
- Week 3: finish whatever is left to do from the analysis; prepare the data story and video

## Organization within the team
- Week 1:
Michael will focus on preparing and cleaning the data for clustering (write code to calculate additional features and perform feature selection). 
Once the data is ready, Marie and Polina will write code to do clustering, each using different methods. 
We will all do some brief research on what types of users are common on social media and what their characteristics are, so as to define exactly what behaviour means. 
- Week 2:
Marie will make visualizations of the clusters
Polina will prepare the data for the behavioural evolution analysis (i.e. for each tweet, create a feature that indicates how many days after the user created the profile the tweet was posted)
Michael and Marie will perform the  behavioural evolution analyses and create visualisation for them (they will split work on different analyses among them)
Polina will set up a platform for the data story
- Week 3:
Marie will start writing the data story
Michael will focus on formatting the blog post and including all visualisations
Polina will work on editing the short video

## Contributions


## Questions for TAs
As mentioned previously, we are concerned about the clustering not producing useful results for the subsequent analyses. If this is indeed the case, what should we do? Should we still conduct the analysis as planned? Or change the questions?
If we decide to add other questions or datasets while working on the project, should we report it back to you or simply proceed and mention it when showing results?




