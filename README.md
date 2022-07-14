# Non-Separable-Classification-using-MLP-Multi--Font-Character-Recognition-Classification-Problem

Non-Separable Classification using MLP: Multi- Font Character Recognition 

# Problem Statement 
Evaluate the performance of MLP networks on the problem of multi-font character 
recognition. The network will be trained on upper-case English letters in selected fonts. 
The data that will be used for this assignment, consisting of 6 fonts (Courier, New York, 
Chicago, Geneva, Times, and Venice), was collected and quantized by Lee [1988]. A 
summary of the data collection method is presented here [Logar et al., 1993]: 


## Dataset 
- The image of the letter is normalized to an 18 x 18-character matrix, where the 
line thickness is one and the image is represented by 0's (background) and 1's 
(foreground). 
- Fourteen properties similar to those proposed by Fujii and Morita (see reference) 
were extracted from each image. Each property is a 3 x 3 matrix, thus, for each 
image, a 14 x 9 matrix is generated. This is the X matrix for that image. A property 
recognition matrix, Y, is constructed for each image and is also a 14 x 9 matrix. It 
is chosen arbitrarily and is as simple as possible. W is a 9 x 9 filter matrix that 
maps X to Y and can be found from W = X* Y, where X* the pseudo-inverse of X. 
- A 3 x 3 window is moved from upper left to lower right over the character image. 
The 9 elements in the window are multiplied by the matrix W. If the output matches 
a row of Y, say row k, the kth place in the count matrix is incremented by the 
weighting factor of that property. 
- Thus, the count matrix for a character contains the number of exact template 
matches, weighted by position. The result is 156 (26 x 6) 14-element vectors 

### Train Data 
Train data contains Courier, New York, and Chicago Fonts; 78 Patterns in Total (26 x 3). 
- Length of the Input Per Pattern: 14 
- Length of the Output Per Pattern: 26 (Binary Values Check Alphabet Match: 0 
denotes "no match" and 1 denotes "match") 
Sequence: 
- Pattern #1: Courier Font Alphabet A 
- Pattern #2: New York Font Alphabet A 
- Pattern #3: Chicago Font Alphabet A 
- Pattern #4: Courier Font Alphabet B 
- Pattern #5: New York Font Alphabet B 

- Pattern #6: Chicago Font Alphabet B 
- Pattern #76: Courier Font Alphabet Z 
- Pattern #77: New York Font Alphabet Z 
- Pattern #78: Chicago Font Alphabet Z 

### Test Data 
Test data contains Geneva, Times, and Venice Fonts; 78 Patterns in Total (26 x 3). 
- Length of the Input: 14 
- Length of the Output Per Pattern: 26 (Binary Values Check Alphabet Match: 0 
denotes "no match" and 1 denotes "match") Length of the Pattern: 40 
Sequence: 
- Pattern #1: Geneva Font Alphabet A 
- Pattern #2: Times Font Alphabet A 
- Pattern #3: Venice Font Alphabet A 
- Pattern #4: Geneva Font Alphabet B 
- Pattern #5: Times Font Alphabet B 
- Pattern #6: Venice Font Alphabet B 
- Pattern #76: Geneva Font Alphabet Z 
- Pattern #77: Times Font Alphabet Z 
- Pattern #78: Venice Font Alphabet Z 

## Methodology 
The following steps are followed to address each problem using MLP: 
1. Data Reviewing 
2. Data Preprocessing 
3. Build a baseline model and optimize parameters 
4. Build and Train Model using optimized parameters 
5. Model Evaluation 
