# Mentor-Recommendation
To recommend mentors to aspirants based on shared preferences like subjects, city, English proficiency, and college preferences.

Approach Overview

Data Import:Two datasets are loaded from an Excel file
1.Aspirants sheet: Contains information about law aspirants.
2.Mentors sheet: Contains mentor profiles.

Profile Construction:
A combined "Profile" string is created for each aspirant and mentor using Preferred/strong subjects,City,English proficiency,Preferred/current college.
(This ensures that the same vocabulary is used for both aspirants and mentors)

Text Vectorization:These profile strings are transformed into vector representations using CountVectorizer, which converts text into numerical feature vectors.

Similarity Computation:Cosine similarity is used to compare aspirant profiles with mentor profiles to determine how similar they are.

Recommendation Logic: For each aspirant, the top 3 most similar mentors (highest cosine similarity score) are recommended.
