# 1.Machine Learning ?
- Hum machine ko data dete h and machine uss data se learn karta h and find patterns and jab tm uss data se related koi question puchoge to uska answer milega. (jitna jyada data and good algorithm then utna accha prediction)

simply,
ML = Data + Algorithms → Learn Patterns → Make Predictions


# 2. Types of Machine Learning

i. Supervised Learning
- data are labelled
- labelled data - input ke sath uska output given hota h
- humne model train kar diya ki kiss input ke liye output kya h , fir Phir jab naya input mile — to model correct output predict kar deta hai.

Ex:- Email spam detection , Price prediction ,  Medical field

ii. Unsupervised Learning
- data are not labelled

iii. Reinforcement Learning
Socho tum video game khel rahe ho.
Koi direct guide nahi, par jab sahi move karte ho toh points milte hain,
galti karte ho toh life chali jaati hai 😅
Dheere-dheere tum samajh jaate ho — “kaunsa move best hai!”

💡 Same logic in ML:
Agent environment mein action leta hai.
Us action ke basis par reward ya punishment milta hai.
Goal: zyada se zyada reward earn karna.
Model try–error karke best strategy seekhta hai

# 3. Overfitting vs Underfitting
Machine Learning ka main goal hota hai —
"Data se seekhna, aur naye data par sahi predict karna."
Lekin kabhi model zyada seekh leta hai,
aur kabhi kam seekhta hai


* Underfitting - Model ne data achhe se seekha hi nahi .
             - Model ne data samjha hi nahi.

* Overfitting -  Model ne data itna yaad kar liya ki naya question dekhke confuse ho gya.
            -  Model training data pe perfect, par new data pe fail.


# 4. Regression aur Classification
- Regression mein hum numbers (continuous values) predict karte hain.
Example:
Ghar ka price predict karna (₹25 lakh, ₹50 lakh, ₹1 crore)
Temperature predict karna (29.5°C, 32.7°C)


- Classification mein hum categories ya classes predict karte hain.
Example:
Email spam hai ya nahi? (Spam / Not Spam)
Tumhare photo mein dog hai ya cat? (Dog / Cat)
Student pass hua ya fail? (Pass / Fail)


# 5. Regression
- Prediction of continuous value,means koi number ya quantity predict karna.
- Example: Ghar ki price predict karna , Student ke marks predict karna

i. Linear Regression
- old data se pattern sikhta h and fir new data par prediction karta h.
- y=mx+c  (x-independent variable , y - dependent variable)


ii. Polynomial Regression
- y=b0​+b1​x+b2​x^2+b3​x^3+...+bn​x^n


* Note:- if x is known so how to find y , m , c
step1: humare paas x and y ka value diya hoga i.e, training dataset
iske help se hum m and c find kar lenge.
| x (Hours Studied) | y (Marks) |
| ----------------- | --------- |
| 1                 | 40        |
| 2                 | 50        |
| 3                 | 65        |
| 4                 | 75        |

step2: use this formula to finc m and c
![formula to calculate m and c](Least_Squares_Method_formula.png)

Now , we get m and c

step2: now kisi bhi particular new x point ke liye y find kar lenge.

Ex:- Netflix algorithm thousands of users ka data use karke m aur c find karta hai (pattern between x & y).
Phir naye user ke liye predict karta hai — “Agar ye itna comedy dekhta hai, to usse ye rating pasand aayegi.”


# 6. SVM (Support Vector Machine)
- ye classification ke liye bana tha — jaise: Ye image cat ki hai ya dog ki?
- SVM ek boundary line(hyperplane) banata hai jo classes ko alag karta hai



# 7. Decision Tree
- It is a Supervised Machine Learning used for both Classification aur Regression.
* Yeh algorithm ek tree structure me decisions banata hai:
        - Root Node: jahan se decision start hota hai
        - Internal Nodes: jahan condition lagti hai
        - Leaf Node: final output

* Example : - Bank tmhe credit card dega ya nhi ?
     Feature: Income , Credit Score , Age

    Tree:-
                   [Credit Score > 700?]
                 /             \
              Yes               No
             /                    \
    [Income > 50K?]          Reject Loan
       /       \
    Yes         No
   /             \
Approve Loan    Reject Loan

* Features:-
i.Handles both categorical and numerical data.
ii.Easy to understand and visualize

* Advantages


# 7. Bagging and Boosting

* Bagging
- Original data me se randomly kuch data ko select kro
- ab random select kiya hua data pe decision tree train karo.
- jiska majority sabse jyada hoga wahi output hoga.
- Predictions combine karo:
        Classification: majority vote
        Regression: average/mean

    Classification- Jab output category/label ho (jaise Yes/No, 0/1, Cat/Dog)
    Regression- Jab output numerical value ho (jaise price, age, temperature)

- Original data ka randomly select kiya hua part, jisme same data point repeat ho sakta hai

- Example: Random Forest follows bagging technique

- real life:- Ek question ke liye 10 students independently answer dete hain → majority ka answer final hota hai.


* Boosting
- Pehla tree train karo.
- Jo points galat predict hue → unko zyaada importance (weight) do.
- Agla tree sirf un galti points ko better predict karne ki koshish kare.
- Repeat karte jao → final prediction = sab trees ka weighted combination

- real life:- Ek student step by step apni mistakes  se seekh raha hai → next attempt me galti kam hoti hai



# 8. Random Forest
- It is an extension of Decision Tree.
- It removes the problem of Decision Tree.
- Decision Tree me hum ek dataset se 1 tree create karte h and random forest me hum multiple tree create karte h and multiple Decision Tree milke forest banata h.
- Decision Tree me overfitting ka problem tha usko Random Forest solve kar deta h.

