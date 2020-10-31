### Performance comparison 

Classifiers might achieve varied performance on different datasets. To assess the fitness between the 6 reader binding site datasets and the two deep learning classifiers, models were built on full transcripts and their performance were analyzed. Similarly, different size of full transcripts was encoded with One-hot method. As shown in Figure 3(A), models using CNN classifier achieved theoretically good performance with overall AUROC larger than 0.8. It seems that the CNN classifier fit the YTHDF1 binding datasets better than other reader binding sites, with overall AUROC exceeding 0.9 and highest AUROC of 0.93. In addition, CNN model achieves good performance with YTHDF2 binding datasets as well, with highest AUROC of 0.929. It is noticeable that the performance of CNN models with EIF3a varied dramatically along with the size of transcript, from 0.96 to 0.81, which suggests that the performance of CNN classifier is depend on the size of transcripts. Similar trends can be seen in the YTHDC2 datasets, the trained model with different input size achieves different AUROC score, with optimal input transcript size of 251bp (AUROC = 0.89)

Regarding the fitness of CNN+RNN classifier with the six reader datasets, models shows similar performance for YTHDF3, YTHDF2, YTHDF1, YTHDC2 datasets (with AUROC around 0.9). Moreover, the model trained with these four datasets as well as the YTHDC1 datasets (with AUROC around 0.875) seems transcript-size independent since lines are relatively stable. Interestingly, the performance of models trained with EIF3a datasets varied greatly from length to length (AUROC varied from 0.88 to 0.94). The structure variation between YTH family protein and EIF3a might contribute to the difference on model performance.

To assess the feasibility of the two classifiers, namely CNN and RNN, performance of models was interpreted and compared. Figure 3(B) compares the performance of models with different size of EIF3a transcripts. As indicated, the combination of CNN and RNN classifier achieves overall better performance than the CNN classifier for both full transcript and mature transcript. Since the trend of line graph for CNN+RNN model is more stable than the line for CNN model, we can infer that the combination of CNN and RNN makes the model less dependent on the length of transcript used.

![Alt text](https://github.com/yuxuanwu17/m6A_reader/blob/master/plot/cmbd2.png)

**Figure 3** (A) Compared the performance of CNN model and CNN+RNN model in the prediction of six m6A reader substrates under different length in full transcripts. (B) Compared the AUROC value in either full transcript or mature transcript when predicting the EIF3A reader substrates. 

### ROC and PR-curve comparison between multiple sequence length

the Receiver Operating Characteristic (ROC) curve and Precision-Recall curve for EIF3A datasets under the combination of CNN and RNN were visualized in Figure 4. As can be seen from the figure that, although the performance was different under different sequence size, the overall trend was stable and devoid of fluctuation. In addition, the overall performance in full transcripts could outperform the mature transcripts, probably the reason that full transcript data could cover either the exon or intron region. 

Here, we mainly opted EIF3A dataset for easy demonstration in this paper. More details of the other five datasets could be achieved in the supplementary file.

![Alt text](https://github.com/yuxuanwu17/m6A_reader/blob/master/plot/rocs_update.png)

**Figure 4** (A) Compared the ROC curve and the regarding AUROC of mature and full transcript of EIF3A under CNN+RNN model in various sequence lengths. (B) Compared the PR curve and the regarding PRAUC of mature and full transcript of EIF3A under CNN+RNN model in various sequence lengths. 
