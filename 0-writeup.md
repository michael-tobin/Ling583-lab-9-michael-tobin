Michael Tobin
Prof Malouf
LING 583
04/26/2021
Lab 8

**1-rnn.ipynb**
Of the three, I wound up spending the most time with this notebook. I have never dealt with deep learning prior to this course and assignment, so I wound up going through the whole notebook a few times to get a better grasp on what it was doing and to annotate it with notes from the lecture. 

Later, when attempting to get the accuracy above 91, I spent a few hours running different parameters. If you look at the notebook, I have a changelog where I tracked the various adjustments that I made to the model, though it does not contain the first few adjustments that I had attempted before I started the log. 

I was never able to get the accuracy above 91; the highest that I was able to attain was 90.750, and that was without using the additional dimensions that were eventually added to the vocab. My experience with the additional dimensions was that they lowered the scores across the board; my lowest accuracy scores were attained with those dimensions, and the highest score with them was middle of the road for the previous scores.

In my experience, the single adjustment that had the most positive effect was dropout. By the end of the guided portion, dropout was at .5, but my highest accuracy run was gained by bringing the dropout down to .25 with no other adjustments. 

From there, the number of epochs seemed to have the next strongest effect on the accuracy, with the best run having 5 epochs, and 6 epochs being hit or miss. I had tried a few runs with 4 epochs before tracking the runs, but the results were nothing to write home about. 

The metric that had the most profound effect on runtime with little effect on accuracy was the hidden layers. For most of the runs I left that at 2, but for a few of them I tried bumping it up to 3, which nearly doubled the time taken for each epoch.

**2-distilbert.ipynb**
I the guided portion of the video, your model peaked at 2 epochs with, ))if I recall, around 92% accuracy before going down after the third epoch. When I ran my notebook, I received my highest accuracy score, 91.7, after the first epoch, with a drop to 90.99 after the second. Out of curiosity, I ran a few more epochs and found that after the third epoch, there was a slight uptick to 91.15 before dropping down to 90.94 and 90.39 after the fourth and fifth epochs, respectively. 

**3-lime.ipynb**
My experience with the results of this notebook just reinforced the idea that you put forth in the video; the reviews that were incorrectly categorized were likely due to the confusing wording as compared to the star ratings. Reviews that read as negative would have 4 or 5 stars and reviews that had low ratings would read fairly positive. While this is a limitation of the model, it is consistent with our previous findings with the linear models. 

As an aside, I asked my wife to read a few of the miscategorized reviews and to tell me what she thought the sentiment was. She agreed with the models (incorrect) choices almost every time. 