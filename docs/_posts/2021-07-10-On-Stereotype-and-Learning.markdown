---
layout: single
title:  "On Stereotype and Learning"
date:   2021-07-10 13:45:12 +0700
categories: generalization learning AI ML
---

> **Melanie**: Well, maybe it's going to learn that some statistical patterns in the data that might have to do with the fact that people who live in certain zip codes are likely to have more recidivism than people who live in other zip codes. Sure, it's true, but it's not the cause. Living in that zip code is not necessarily the cause of that. The system has no causal model of the world and how the world works. The system just Learning patterns from data. And so it's inevitable that you're going to get biases. We humans are wired to have biases.

> We saw that the other night when Rajiv Sethi gave a talk about our stereotypes and how and why we have stereotypes, and how they can be beneficial, and also very unbeneficial. But we don't just learn patterns from statistics, we have kind of these causal models of the world. So we're likely to know that living in a certain zip code, that those particular five numbers are not the reason why you did well on the SAT or why you went to prison. You kind of have this world model of causality. And we also have, as we talked about, metacognition.

Let consider a stereotype: "all black people are uneducated criminals". If the medias are flooded with breaking news on black thieves, black gangsters, crimes done by black people, then will a blank slate human (like a child) learn this stereotype? It might be possible that we humans indeed learn statistical pattern from data, since there are some people actually believe that all black people are bad.

Note that a stereotype is actually called a hypothesis in Statistical Learning Theory: it assigns a label "criminal" or "not criminal" to samples, which are people in this case, based on some features, like skin color, ZIP code, biển số xe, etc.

The interesting question is how we debug this stereotype? Why do most of us realize that this stereotype is not true? Considering a stereotype in Vietnam: "Women are stupid and belong to the kitchen". While people from older generations might hold such view, a much larger portion of younger generation doesn't. What causes the change?

Is that younger peoples are exposed to more contradicting examples (women are as smart and capable as any other man), so that what they learn from the data is different? I doubt that this is solely based on Statistical Pattern learning, since the portion of successful women is much smaller compared to men, even in 2021, therefore this stereotype statement is still statistically correct.

Considering a Hypothetical World where most women were actually stupid and did nothing, then a few exceptional women were just outlier examples and would be considered as noise signals to our cognition model. In a statistical point of view, the data distribution concentrates at positive examples (stupid women), while negative examples (smart capable women) are at the tail. This is a troublesome long tail distribution.

There might be some model correctly describes most or all the data, yet the fact that the data distribution concentrates on some regions hinders learning this model. The catch is, just by picking up the Statistical Pattern of the dense regions where most of the data come from, you will have a simple model which is correct most of the time. In many case, this is our stereotypes. However, this practice is easy and efficient, why bother for more?

This is conventional machine Learning, statistical learning theory. It works under the iid assumption: the test distribution must be identical to training distribution.

I'm very much interested in the point where we started to doubt our model, paying more attention to and thinking more about these previously called noises. What causes this transition of mind?

What if the mechanism involves hypothesis testing, that a statement is deemed not correct if there is a portion of X% samples contradicting the statement.
    
After recognizing something might be wrong, we would want to improve our inaccurate model. In humans, how could just a few samples completely change our mind?

It might be that we pay more attention to the negative examples and try to learn something from that. In other words, although we couldn't meet more successful women, we pay a lot of attention to each one we meet, and try to let these examples undoing our biased minds.

One way to do that is via normal statistical learning just like before, however with more weights on these negative examples. This is equivalent to shift the data distribution, from concentrating at the stereotype-positive examples to the stereotype-negative examples. It's like we would construct our own hypothetical world, in which there were a lot of successful women, and hence the data distribution is different to the world we lived in.

This is actually the setting of Domain Generalization, and in general Out-of-distribution Generalization, with only data shift and minor to zero shift in ground-truth labeling mechanism. I hypothesize that we might be constantly constructing hypothetical worlds, shifting the distributions inside our mind to test our model, which helps discarding spurious statistical correlations and retaining only the Causal Model of the world.
