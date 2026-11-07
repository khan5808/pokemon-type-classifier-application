# pokemon-type-classifier-application
Can Machine Learning Guess a Pokémon’s Type from Its Stats?
Short Description:
This project explores whether machine learning models can predict a Pokémon’s type using only its base stats. By analyzing 1,351 Pokémon and testing several algorithms, the results show both the potential and limits of this approach for game design and data science learning.

What Happens When You Try to Predict Pokémon Types from Stats?
If you’ve ever wondered how closely a Pokémon’s stats relate to its type, you’re not alone. For this project, I set out to see if machine learning could predict whether a Pokémon is, say, Water or Electric type, based purely on numbers like attack, defense, and speed. The results were eye-opening and showed just how complex type assignment really is.

Why This Project Matters
Understanding the relationship between stats and types could help game designers balance new Pokémon or give insights into how types are distributed. For data students and fans, it’s a chance to apply machine learning to a fun, recognizable dataset and see the challenges that come with real-world data.

The Data and Tools
I used a Kaggle dataset with 1,351 Pokémon, each with features like attack, defense, special attack, special defense, speed, HP, and both primary and secondary types. Python was my main tool for data cleaning, feature engineering (like z-score normalization), and building models. I also used upsampling techniques like SMOTE and ADASYN to handle the fact that some types are much rarer than others.

What I Found
Predicting a Pokémon’s type from its stats turned out to be much harder than expected. The best models—ensemble tree methods like Extra Trees, Random Forest, and Gradient Trees—could only reach under 40% for key metrics like precision, recall, F1-score, and accuracy. Simpler models, such as a basic Decision Tree, performed worse, staying below 30% for all metrics.

Looking at the dataset itself, 57% of Pokémon have two types, and 43% have just one. Some types, like Water, Normal, and Grass, are common as a first (primary) type, while types like Flying, Fairy, and Ice are rare as primaries but show up more often as a secondary type. Flying type especially stands out, being much more common as a secondary type. The most frequent dual-type combination is Normal/Flying, followed by Rock/Flying, Grass/Poison, Bug/Flying, and Bug/Poison.

Certain types (Dragon, Rock, Bug, Steel, Dark, Flying, Poison) mostly appear as a primary type, while others (Fairy, Normal, Electric, Psychic) are usually secondary. Some types, like Ice, Fighting, and Water, are split fairly evenly between primary and secondary.

Because of these patterns, the models had trouble predicting types that are rare or appear mainly as a secondary type. This highlights that type assignment in Pokémon involves more than just stat numbers.

The Big Picture
While machine learning can spot some trends, base stats alone are not enough to reliably predict a Pokémon’s type. For anyone interested in game design or data science, this is a good reminder that real-world problems often need more features and context than you might expect.

What Could Make This Better?
A next step could be to include features beyond just stats—like abilities, move sets, or even visual design elements—to see if that helps the models do better. It might also be useful to test different algorithms or focus on predicting types within specific Pokémon generations.
