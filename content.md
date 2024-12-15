---
layout: page
title: Back to the Future 
subtitle: Back to the Future - Time-Traveling through Wikispeedia
mathjax: true
cover-img: "/ada-outlier-datastory/assets/img/Marty_and_Doc/dolo_flamme.png"
---

<!--
TEMPLATE DE DIALOGUE POUR AVOIR LES IMAGES CORRECTEMENT:


<div class="chat">

   <div class="Marty_crazy">
      <div class="icon"></div>
      <div class="message">
      text marty with crazy icon
      </div>
   </div>

   <div class="Doc_crazy">
      <div class="message">
      text doc with crzay icon
      </div>
      <div class="icon"></div>
   </div>

   <div class="Marty">
      <div class="icon"></div>
      <div class="message">
      text marty with normal icon
      </div>
   </div>

   <div class="Doc">
      <div class="message">
      text doc with normal icon
      </div>
      <div class="icon"></div>
   </div>

</div>
-->


<div class="chat">

   <div class="Marty">
      <div class="icon"></div>
      <div class="message">
      Hey Doc! What's up? You know, this web game, Wikispeedia? I've been playin' it a few times and it's way harder that I thought it would be.
      </div>
   </div>

   <div class="Doc">
      <div class="message">
      What are you talking about Marty? You know your old Doc, I am not quite into online games or whatsoever.
      </div>
      <div class="icon"></div>
   </div>

   <div class="Marty_crazy">
      <div class="icon"></div>
      <div class="message">
      Ok, ok, hear me out:
      </div>
   </div>

</div>



~ small presentation about Wikispeedia principle and how to play the game ~


<div class="chat">

   <div class="Doc">
      <div class="message">
      Fascinating! Marty, you are saying it is harder that you thought, how so?
      </div>
      <div class="icon"></div>
   </div>

   <div class="Marty">
      <div class="icon"></div>
      <div class="message">
      Yeah Doc, I dunno, sometimes I don't even now the target so I try but I just fail… Or sometimes I just keep going back and forth between articles because they just don't look like how I expected them to be, like at all! It seems like they are not nowadays Wikipedia articles and do not contain the next link I was looking for, things like that… Is this game too old for me? Am I just bad at this game?
      </div>
   </div>

   <div class="Doc_crazy">
      <div class="message">
      Hmm I see… Well Marty, you just gave me a BRILLIANT idea! Let us inspect this game and see how people performed on it since it's been created!
      </div>
      <div class="icon"></div>
   </div>

   <div class="Marty_crazy">
      <div class="icon"></div>
      <div class="message">
      Sure Doc, take the lead!
      </div>
   </div>

</div>


~ Presentation of the dataset by Doc ~


# Part 1: How are people performing in Wikispeedia?

<div class="chat">

   <div class="Doc">
      <div class="message">
      The articles present in the Wikispeedia dataset have categories. Do these categories influence your success, Marty? Let's explore that together!
      </div>
      <div class="icon"></div>
   </div>

   <div class="Marty">
      <div class="icon"></div>
      <div class="message">
      Well, tell me Doc, what do the categories look like?
      </div>
   </div>

</div>

For most of them, one main category is followed by more precise subcategories. For example, the mixed-breed dog article has the main category "Science", first subcategory "Biology" and second subcategory "Mammals". For simplicity, we will keep only the first category, i.e. the main one. You can take a look at the distribution of those main categories here.

Second, we notice that among the 4598 articles, some have more than 1 main category: we count 590 articles with 2 main categories and 8 articles with 3. It complicates our analysis. To keep things simple, we will impose rules on which main category we think is the most important for the article considered. For this, we have created a partial ordering in the categories, based on what we could observed. The reasoning is explained on this page. HERE:: insert link to partial ordering page.

<!--
First, what do the categories look like? For most of them, one main category is followed by more precise subcategories. For example, the mixed-breed dog article has the main category "Science", first subcategory "Biology" and second subcategory "Mammals". For simplicity, we will keep only the first category, i.e. the main one. You can take a look at the distribution of those main categories here. HERE::\<insert image of Einstein the dog\>

HERE:: more analysis?

Second, we notice that among the 4598 articles, some have more than 1 main category: we count 590 articles with 2 main categories and 8 articles with 3. It complicates our analysis. To keep things simple, we will impose rules on which main category we think is the most important for the article considered. For this, we have created a partial ordering in the categories, based on what we could observed. The reasoning is explained on this page. HERE:: insert link to partial ordering page.
-->

<iframe 
    src="/ada-outlier-datastory/assets/img/pie_cat.html" 
    class="responsive-iframe" 
    title="Pie chart of the categories">
</iframe>


<div class="chat">

   <div class="Marty">
      <div class="icon"></div>
      <div class="message">
      Wow! Back in 2007, science articles represented almost 1/4 of the encyclopedia, whereas art articles comprised less than 1% of it.
      </div>
   </div>

   <div class="Doc">
      <div class="message">
      You're right! Let's now look at the links between the articles: from which to which categories go the links? Do they lead to an article from the same category or to another? Is it easy to navigate to another category?
      </div>
      <div class="icon"></div>
   </div>

</div>


<!--
Back in 2007, science articles represented almost 1/4 of the encyclopedia, whereas art articles comprised less than 1% of it. 


Let's first look at the links between the articles: from which to which categories go the links? Do they lead to an article from the same category or to another? Is it easy to navigate to another category?
-->

<iframe src="/ada-outlier-datastory/assets/img/links_categories.html" width="900px" height="600px" alt='links_categories'></iframe>

<!-- INITIAL TEXT:
Wow, lots of information on this plot! First, the diagonal, i.e. links staying in the same category has bigger values compared to the lines or columns in general. Then, we can observe that the brighter columns are the ones from science, geography and countries. For science and geography, it makes sense as these are the most represented categories as we have seen previously. On the other hand, it seems very easy to reach articles about countries: there are more than twice of links pointing to countries as links going out from countries. It seems logical as for many concepts, the place of invention discovery or birth is mentioned, including the country. Science articles are the ones linking out the least to other categories, with only 41% of links going elsewhere than in science articles. With these data in mind, are there categories of articles that are harder to guess?

To answer this question, we can investigate the categories of starting articles and target articles of the players.

BUBBLES AND PLAIN TEXT:
-->

<div class="chat">

   <div class="Marty">
      <div class="icon"></div>
      <div class="message">
      Wow, lots of information on this plot! Help me there Doc!
      </div>
   </div>

   <div class="Doc_crazy">
      <div class="message">
      Don't worry Marty, we just need to break this into small steps. Here:
      </div>
      <div class="icon"></div>
   </div>

</div>


First, the diagonal, i.e. links staying in the same category has bigger values compared to the lines or columns in general. Then, we can observe that the brighter columns are the ones from science, geography and countries. For science and geography, it makes sense as these are the most represented categories as we have seen previously. On the other hand, it seems very easy to reach articles about countries: there are more than twice of links pointing to countries as links going out from countries. It seems logical as for many concepts, the place of invention discovery or birth is mentioned, including the country. Science articles are the ones linking out the least to other categories, with only 41% of links going elsewhere than in science articles.


<div class="chat">

   <div class="Marty">
      <div class="icon"></div>
      <div class="message">
      Ok I see! But then, does this mean that there are categories of articles that are harder to guess?
      </div>
   </div>

   <div class="Doc">
      <div class="message">
      To answer this question Marty, we can investigate the categories of starting articles and target articles of the players!
      </div>
      <div class="icon"></div>
   </div>

   <div class="Marty_crazy">
      <div class="icon"></div>
      <div class="message">
      Hah! Leave it to me Doc…
      </div>
   </div>

   <div class="Doc">
      <div class="message">
      Wait a second Marty! We have to clean a bit the data...
      </div>
      <div class="icon"></div>
   </div>

   <div class="Marty">
      <div class="icon"></div>
      <div class="message">
      What do you mean? What's wrong with the data?
      </div>
   </div>

   <div class="Doc">
      <div class="message">
      First, there are some articles that doesn't appears in `categories.tsv`... We don't know their categories. Thus, we will remove these games. Second, some players seemed not to take the game very seriously... They didn't even click on a link! We will also remove these paths.
      </div>
      <div class="icon"></div>
   </div>

   <div class="Marty">
      <div class="icon"></div>
      <div class="message">
      But don't we introduce a bias in this way?
      </div>
   </div>

   <div class="Doc">
      <div class="message">
      We get rid of only 0.13% of the finished paths and 21.18% of the unfinished paths. 21.18% can look big but most of the discarded paths have a length of 1, and the player didn't take any action! These paths are not exploitable, discarding them is our best option.
      </div>
      <div class="icon"></div>
   </div>

</div>



<iframe src="/ada-outlier-datastory/assets/img/categories_finished_paths_start2target.html" width="900px" height="600px" alt='categories_finished_paths_start2target'></iframe>

<iframe src="/ada-outlier-datastory/assets/img/categories_unfinished_paths_start2target.html" width="900px" height="600px" alt='categories_unfinished_paths_start2target'></iframe>

<div class="chat">

   <div class="message-wrapper">
      <img src="/ada-outlier-datastory/assets/img/Marty_and_Doc/marty1.png" alt="Marty" class="profile-pic">
      <div class="message Marty">
         Both heatmaps look similar! Should we conclude that there is no difference between finished and unfinished paths categories?
      </div>
   </div>

   <div class="message-wrapper">
      <div class="message Doc">
         We cannot conclude that quickly Marty. Let's perform a statistical test for that. In our case, we should use a chi2 contingency test: our null hypothesis is that both distributions are identical. What is meant by distribution is a vector of 15x15 that contains the count of links from the start category to the end category. It's simply the data from the heatmap, in the form of counts. We choose a level of significance of alpha=0.01.
      </div>
      <img src="/ada-outlier-datastory/assets/img/Marty_and_Doc/doc1.png" alt="Doc" class="profile-pic">
   </div> 

   <div class="message-wrapper">
      <img src="/ada-outlier-datastory/assets/img/Marty_and_Doc/marty1.png" alt="Marty" class="profile-pic">
      <div class="message Marty">
         Ok, let me see… The results are the following: `pvalue=0.0, statistic=2953.30`. And, the test gives the same results while comparing the distribution of link counts towards one target category (`statistic=207557.76`) or from one source category (`statistic=39997.79`).
      </div>
   </div>

   <div class="message-wrapper">
      <div class="message Doc">
         Great! We can thus safely reject the null hypothesis!
      </div>
      <img src="/ada-outlier-datastory/assets/img/Marty_and_Doc/doc_crazy.png" alt="Doc" class="profile-pic">
   </div> 

   <div class="message-wrapper">
      <div class="message Doc">
         If we dig into the details, we see that a few major differences occur. First, there is 4 times less target from the Countries category in among the unfinished paths, whereas there is 2 times more target from Design_and_Technology. There are also an increase of 66% of target articles in Everyday_life category.
      </div>
      <img src="/ada-outlier-datastory/assets/img/Marty_and_Doc/doc1.png" alt="Doc" class="profile-pic">
   </div> 

   <div class="message-wrapper">
      <img src="/ada-outlier-datastory/assets/img/Marty_and_Doc/marty1.png" alt="Marty" class="profile-pic">
      <div class="message Marty">
         So apparently, finding an article in Countries category is easier than finding an article in Design_and_Technology or Everyday_Life for example.
      </div>
   </div>

</div>

<!--
Both heatmaps look similar! But what do the statistics tell us? Let's perform a chi2 contingency test with `scipy.stats.chi2_contingency` function: our null hypothesis is that the distributions are identical. 
What is meant by distribution is a vector of $$15\times15$$ that contains the count of links from the start category to the end category. It's simply the data from the heatmap, in the form of counts. We choose a level of significance of $$\alpha=1$$%. The results are the following: `pvalue=0.0, statistic=2953.30`. We can thus safely reject the null hypothesis! The test gives the same results while comparing the distribution of link counts towards one target category (`statistic=207557.76`) or from one source category (`statistic=39997.79`).

Let's dig through some details. A few major differences occur. First, there is 4 times less target from the Countries category in among the unfinished paths, whereas there is 2 times more target from Design_and_Technology. There are also an increase of 66% of target articles in Everyday_life category.

We can then conclude that finding an article in Countries category is easier whereas finding an article in Design_and_Technology or Everyday_Life seems harder.
-->

<div class="chat">

   <div class="message-wrapper">
      <img src="/ada-outlier-datastory/assets/img/Marty_and_Doc/marty_cool.png" alt="Marty" class="profile-pic">
      <div class="message Marty">
         Hah! We found why the players lose! Wasn't that hard.
      </div>
   </div>

   <div class="message-wrapper">
      <div class="message Doc">
         Hold on a second Marty! There might be other interesting factors…
      </div>
      <img src="/ada-outlier-datastory/assets/img/Marty_and_Doc/doc1.png" alt="Doc" class="profile-pic">
   </div> 

</div>



One can assume that the shorter the shortest path, the more likely it is to find a path, because both articles are closely connected by links. 

{: .box-note}
  The **shortest path** between two articles is given by the minimum number of links you must click plus 1.

This is well illustrated in the following plot. The longer the shortest path is, the fewer finished paths there are! The biggest shortest path for which we have finished paths is 7. Only 17.37% of the game collected are victories. We also notice that two-thirds of the players did not go far enough anyway to reach the target, as they stopped before even reaching the shortest path length. As we could expect, the bigger success rate occurs with a shortest path of 3 and decreases monotonically while the shortest path increases. 

<iframe src="/ada-outlier-datastory/assets/img/distrib_path_lengths_wrt_shortest_path.html" width="900px" height="600px" alt='distrib_path_lengths_wrt_shortest_path'></iframe>

Another parameter might be the number of links leading to the target: intuitively, the more there are the easier it is to reach the article. Let's work on this hypothesis. The following plot shows the distribution of the links to the target number depending on whether the player found the target. The distributions look different! Let's try a t-test of independence to confirm our intuition. Our null hypothesis is that the two distributions are identical. Using the `ttest_ind_from_stats` function from scipy, we obtain a p-value of 0 and a test statistic of 45.50. We can thus safely reject our null hypothesis and conclude that the two distributions are indeed different! Both distribution shapes are similar, but the one from unfinished paths is shifted to the left and there is a peak at 1.

<iframe src="/ada-outlier-datastory/assets/img/distrib_links_to_target" width="900px" height="600px" alt='distrib_links_to_target'></iframe>

How can we now use these observations to predict player success? Let's do a logistic regression! We want to predict if a player will succeed for a given start and end article, depending on the shortest path and the number of links pointing to the target.

Log. regression:
table with results?








# Part 2: How did Wikipedia's structure evolve since 2007?

M: Okay I know more about Wikispeedia and the general performance of players on the game. I wonder 

Let us now compare the differences between the old wikipedia from 2007 and our current wikipedia from 2024. The first factor that could influence the performances of the players is the number of links per articles. Wikipedia is expanding everyday thanks to its collaborative process and has significantly improved and grown since 2007. Let's see how much that changes compared to now ! 

{: .box-note}
  **Basic Comparison:** \
  2007 : 119882 links \
  2024 : 225800 links


## 2.1 Number of links per pages

![distrib_links_per_article](/ada-outlier-datastory/assets/img/distrib_links_per_article.png)

As expected, there is much more links per pages **on average** in our 2024 dataset ! The distribution also shows that more pages have a higher number of links. This could probably influence users' performances. 

<div class="chat">
  <div class="Marty">
    <div class="icon_crazy">
    </div> <!-- icon-->
    <div class="message">
        Cool! So that's why the game is harder in 2007?
    </div><!-- message -->
  </div><!-- Marty -->
  
  <div class="Doc">
      <div class="message">
        Wait a bit Marty let's look more into the details before driving any conclusions. Let's look at individual articles:
      </div><!-- message -->
      <div class="icon">
      </div> <!-- icon-->
  </div><!-- Doc -->
</div>


In the plot below, we visualize every articles within our dataset of the 4604 selected articles from the Wikispeedia game on the x axis and compute the differences in the number of links between the two timepoints. Anything above zero, in green, represents more links in 2024 than in 2007, and anything below, orange, corresponds to less links in the page in 2024 than in 2007.

![diff_links_per_article](/ada-outlier-datastory/assets/img/diff_links_per_article.png)

<div class="chat">
  <div class="Doc">
        <div class="message">
          Overall we see that there is much more pages that gain new links than pages losing links in 2024 !
        </div><!-- message -->
        <div class="icon">
        </div> <!-- icon-->
    </div><!-- Doc -->
    <div class="Doc">
      <div class="message">
        Let's now move to the **interesting** part : the network of the links...
      </div><!-- message -->
      <div class="icon_crazy">
      </div> <!-- icon-->
  </div><!-- Doc -->
</div>

## 2.2 Network differences 

For now, we only have been looking at the repartitions of links on the pages with no interested to where those links would redirect to, even though this is probably our most crucial information to conclude wheter the structure of 2024 has really changed compared to 2007. In this part we look at how the pages are interconnected and compare it for the two different years. To do so we will use the Shortest Path metric. 

<div class="chat">
  <div class="Marty">
        <div class="message">
          Hey Doc... What is actually the shortest path ? 
        </div><!-- message -->
        <div class="icon">
        </div> <!-- icon-->
    </div><!-- Doc -->
    <div class="Doc">
      <div class="message">
        Well Marty it's in the name ! The most direct path from one point to another in a network is the shortest path. We should look at how direct the connections between articles are in 2024 and see where it gets us.
      </div><!-- message -->
      <div class="icon_crazy">
      </div> <!-- icon-->
  </div><!-- Doc -->
</div>

{: .box-note}
  **Shortest Path Algorithm** \ 
  There exist different strategies to compute the shortest path. Here we have decided to use the Floyd-Warshall Algorithm from the 'Networkx' librairy. This algorithm provides the same result for the Shortest Path MAtrix as the one computed in the orginal dataset provided by the source article, when tested on the 2007 dataset.



![heatmap_diff](/ada-outlier-datastory/assets/img/heatmap_diff.png)


![reachable_nodes](/ada-outlier-datastory/assets/img/reachable_nodes.png)


# Part 3

# Part 4: Are the players(LLMs) stronger in 2024 than in 2007 ?

<!--
**Marty** : Doc are the players today stronger than in 2007 ? 
**Doc** : I don't know Marty, we don't have any data about the players in 2024.
**Marty** : But we have the data from 2007, can't we compare the two years ?
**Doc** : We might be able to do that, let me think about it... we can use my favorite tool LLMs <3 to compare the two years.
**Marty** : LLMs ? But, the results will differ from the ones we got from the players's data, right ? Which model should we use ?
**Doc** : Yes, it might be different, but we can test different models and see which is the most similar to the players' data.
**Marty** : That's a great idea Doc, let's do it ! but how would we know if the model is similar to the players' data ?
**Doc** : First, we can verify that the model can finish a game, then we can compare the path length with the players, and eventually, we can measure if the model has chosen the same articles as the players.
**Marty** : Wow, that's a great plan Doc, and once we have the model, we can compare the two years and see if the LLM model is better at the game in 2024 than in 2007.
**Marty** : Heeu Doc, I know you are a genius, but how will you train the models on the 2007 data ?
**Doc** : I will use the games that at least 10 players have played and I will train the models with [Ollama](https://ollama.com/) and based on the path length distribution of the players that we can see below(**INSERT**). I will limit the number of prompts to 50.
-->

<div class="chat">
  <div class="Marty">
    <div class="icon"></div>
    <div class="message">Doc, are the players today stronger than in 2007?</div>
  </div>

  <div class="Doc">
    <div class="icon"></div>
    <div class="message">I don't know Marty, we don't have any data about the players in 2024.</div>
  </div>

  <div class="Marty">
    <div class="icon"></div>
    <div class="message">But we have the data from 2007, can't we compare the two years?</div>
  </div>

  <div class="Doc">
    <div class="icon"></div>
    <div class="message">We might be able to do that, let me think about it... we can use my favorite tool LLMs &lt 3 to compare the two years.</div>
  </div>

  <div class="Marty">
    <div class="icon"></div>
    <div class="message">LLMs? But, the results will differ from the ones we got from the players' data, right? Which model should we use?</div>
  </div>

  <div class="Doc">
    <div class="icon"></div>
    <div class="message">Yes, it might be different, but we can test different models and see which is the most similar to the players' data.</div>
  </div>

  <div class="Marty">
    <div class="icon"></div>
    <div class="message">That's a great idea Doc, let's do it! But how would we know if the model is similar to the players' data?</div>
  </div>

  <div class="Doc">
    <div class="icon"></div>
    <div class="message">First, we can verify that the model can finish a game, then we can compare the path length with the players, and eventually, we can measure if the model has chosen the same articles as the players.</div>
  </div>

  <div class="Marty">
    <div class="icon"></div>
    <div class="message">Wow, that's a great plan Doc, and once we have the model, we can compare the two years and see if the LLM model is better at the game in 2024 than in 2007.</div>
  </div>

  <div class="Marty">
    <div class="icon"></div>
    <div class="message">Heeu Doc, I know you are a genius, but how will you train the models on the 2007 data?</div>
  </div>

  <div class="Doc">
    <div class="icon"></div>
    <div class="message">I will use the games that at least 10 players have played and I will train the models with <a href="https://ollama.com/">Ollama</a> and based on the path length distribution of the players that we can see below(**INSERT**). I will limit the number of prompts to 50.</div>
  </div>
</div>



![players_path_length](/ada-outlier-datastory/assets/img/players_path_length.svg)

![llms_path_not_found](/ada-outlier-datastory/assets/img/llms_path_not_found.svg)

<iframe src="/ada-outlier-datastory/assets/img/performance_scatter.html" width="100%" alt='models_performance' frameBorder="0"></iframe>

![llm_jacard](/ada-outlier-datastory/assets/img/jacard.svg)

![llama3_2007_2024](/ada-outlier-datastory/assets/img/llama3_2007_2024.svg)





# References

[1] Robert West and Jure Leskovec:
     Human Wayfinding in Information Networks.
     21st International World Wide Web Conference (WWW), 2012.
     
[2] Robert West, Joelle Pineau, and Doina Precup:
     Wikispeedia: An Online Game for Inferring Semantic Distances between Concepts.
     21st International Joint Conference on Artificial Intelligence (IJCAI), 2009.
