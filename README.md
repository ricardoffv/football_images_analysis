# Tactical and match information extraction through football matches frames

## Abstract

Nowadays, football tactics are developed with sofisticated and innovative techniques more often. Alongside with this scenario, there are several ways to reach out better results on the pitch for a professional team: improve physical tests, study opponents in-match patterns, review mistakes and flaws from past fixtures, amongst many other activities. The technological enhancements in these tasks is currently being led by integrating a different knowledge area: data analysis. This project has the main goal of exploring image datasets composed by match situations frames, provided by an open-source dataset [1], and extract key indicators from the match events displayed, such as tactical disposition, attack or defence scenarios and identification of possible goal situations. The main metric that should be obtained is the amount of players of each team in the analyzed image.

## Methodology

The desired method to extract valuable information from football matches frames involves the use of in-match events frames preprocessed. Then, it will be applied in the selected images the bag of features to describe tactical information about the game scenario. The main goal of the image processingis to obtain the amount of players of each team in certain frame of the match. A secondary information that could be extracted is the classification of the image in attack or defence scenario. All of these descriptions could lead to a rich analysis when enriching the data with more match events such as score and minutes played to analyze how the team behaved in that certain momentum of the competition.

### Dataset

The dataset selected for this project is a fragment of the dataset made available by [1]. The original dataset contains several images of in-match events taken from frames of TV transmission of the fixtures. The situations portrayed as samples can be several: frre-kick angle, card showed by refferee to a player, goal celebrations, amongst many others.

This study has interest only in wide pictures of players distributed through the pitch. Due to that, the complete dataset of the study were refined to mantain only images where tactical information could be potentially extracted, i.e., the dataset used has only images of wide range taken when the ball was inside the pitch and a significant amount of players is shown.

### Preprocessing

A few techniques will be applied on image for better understanding of the behavior of the descriptors applied. Due to that, a conversion to the greyscale will be performed in the input image. Two tests will take place: a conversion by luminance and a conversion adjusted to the input, with need of additional information: Greyscale adjusted only in the channel of team of interest shirt color, e.g., if home team wears red, channel red will be used as reference to convert to greyscale.

The first approach beneath the cited above will be priorized in the study.

### Bag of Features

With the preprocessed images, the algorithm of the bag of features will be applied with the strategy of cutting the players of the original image through the descriptors.

### Desired Results

The results desired after the applying of the algorithms of the methodology is the information extraction from the match frame. The main metric to be obtained is the number of players of each team displayed in that fragment of the pitch, additional information important to be computed in case of successful approach is the attack/defence scenario description. 


References:
[1] Zanganeh, A., Jampour, M., Layeghi, K.: IAUFD: A 100k images dataset for automatic football image/video analysis. IET Image Process. 00, 1– 10 (2022). https://doi.org/10.1049/ipr2.12543
