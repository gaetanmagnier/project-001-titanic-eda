# Project 001 - Notes

## Objectives

Determine which factors were most strongly associated with passenger survival on the titanic.
---
## Initial observations

891 passengers

Features:
- PassengerId: [1, 891]
- Survived: target variable, binary. 1 = survived
- Pclass: {1, 2, 3}. 1 = upper class, 3 = lower class. High interest. Classes likely reflect socioeconomic status and cabin location.
- Name: String. Contains passenger titles (Mr., Mrs., Miss., Master...) that may be informative. Also contains surnames that could identify family groups. Keep for now and investigate before removing.
**Never remove a variable because it looks useless. Remove it because you've shown it doesn't add information.**
- Sex: {male, female}. High interest. Females
- Age. At first look contains many missing values. Counted NA on excel: 177. High interest
- SibSp: Siblings and spouses count, int.
- Parch: Parents and childs count, int.
- Ticket: Format appears inconsistent. Check weither some passengers shared a ticket
- Fare: Continuous variable representing ticket price. May correlate with passenger class and survival.
- Cabin: Counted NA on excel: 680 missing values. Investigate whether simply having a recorded cabin number is associated with survival.
**Sometimes missingness itself is informative.**
- Embarked: {S, C, Q}. Departure port. Investigate weither embarkation location is associated with survival