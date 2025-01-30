# OfficeUtils

Sooner or later in the lives of most teams comes it - the move. You are taken to a clean empty room, which will become a place where you will spend most of your life. If you are a designer, the first thing you will do is figure out how to hang pictures and put flowers so that the room plays with new colors. If you are an experienced office samurai, you will immediately determine the best place with a swit eye and be the first to claim the rights to it. If you are the head of the department, you will probably have a headache about the seating of all employees. But if you lead a team of data scientists, the Python tomonet will help you.

Of course, everything determines your management style. If you prefer authoritarian decisions, you can just point with a domineering finger where everyone should go. And it doesn't matter if someone is against sitting face down against the wall or with each other. However, since the abolition of serfdom in 1861, this style is systematically losing popularity in our country. And if you are still concerned about the comfort of employees, then you should collect and somehow take into account their preferences. But this is where the devil sneaks up, the one who is in the details: how to collect, how to take into account, who to give preference to, etc.

In view of many years of experience in organizing Olympiads for schoolchildren, where equality of conditions is one of the main priorities, I was determined to create transparent and understandable mechanisms in which more experienced or fast employees do not get any advantages.

You can't please everyone or still...?

We make a premise that employees may have seating preferences, and we want to minimize possible dissatisfaction. That is, it is necessary to organize a system of distribution of places so that some employees, acting in an optimal way for themselves, do not enter into a clear conflict with others. The strategy of "whoever got up first, that slippers" clearly does not lead to this goal. If you determine some order of choice (for example, based on merit), the task is still not solved - a person who chooses earlier, but who cares relatively, can accidentally take a place chosen by others. Not to mention that such an order is a controversial thing in itself.

We chose the type of voting in which everyone's vote depends on how the others voted: if a person more or less does not care which of the two places to sit, then the optimal strategy is to claim where there are fewer competitors.

Our way to the perfect seating

First of all, it was necessary to determine where you could sit down at all. Here the task was for everyone, because everyone is interested in making as many comfortable places as possible - because in this case the competition decreases. We made a map and carried out explanatory work "among the population", promoting each place as ideal.



In an ideal world, everyone should give preference points to each of the places, but it is difficult for a person to estimate to hundredths how one place differs from another.
Therefore, everyone was asked to choose lists of priorities, the number of which is not limited at all: which places he would like to take first, which second, and which third.

It should be noted here that the logic of the employees' preferences was very different: someone wanted to be closer to the window, someone wanted to look out the window, someone was interested in the proximity to the air conditioner and even the color of the walls. It is difficult to take into account the preferences themselves, here you can only give people the opportunity to choose a place.

Then it was necessary to determine the metric of success of the arrangement. The more uncomfortable a person sits, the more such a model should be fined. I decided to make a square fine to avoid blatant inconveniences.

It turned out like this: if a person was put in a place from his TOP-1 list, then a fine of 2; if from the TOP-2 list - a fine of 4, TOP-3 - 8, TOP-4 - 16 and so on. I'm not saying that this metric is optimal, but it looks reasonable.

I wrote a simple program in Python - it introduces priorities from colleagues, and it calculates the arrangement options with a minimum penalty. The algorithm was announced to colleagues in advance (how naive I was!). All the lists were published in the open so that they could agree if desired.

However, after seeing the calculations, some employees realized that you can try to pick up your "application" to get the place they are looking for. Data scientists are such data scientists!:)

As a result, the second round of elections was organized, when it was possible to make changes to their priorities in the closed one. Thus, everyone was again on equal terms - everyone could select and make changes.

Having collected applications from the second round, I run the program finally. Phew! Everyone seems to be happy.

Instead of P.S.

It is worth noting that the wishes regarding the proximity of employees to each other were not taken into account here. But in this paradigm they are also quite easy to implement by creating wish lists (who wants to sit next to whom and what places are nearby, according to these employees), and then to fine the model for non-fulfillment of these wishes.

Of course, it is always possible when two settings have the same penalty.
In this case, I have already decided to rely on the coin - optimization is further powerless :).

Nikolai Knyazev, head of the machine learning group "Infosystems Jet"
