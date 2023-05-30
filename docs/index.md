# Master thesis, overrides title defined in config

## Question I try to answer
about characterizing events, stable pages, recurrent topics

## Explain RTD graph viz tool
* Where it comes from
* Why it has been implemented that way
* What it could bring us for our analysis
* * The limitations: Page level analysis and alpha parameter not optimized

## Throughout a year 
* Current events, exclusive types
* The dimensions we’ll be playing with


### What happened in 2020 ?

{% include divs_dates.html %}
**Figure XX. Top 40 pages contribution to rank turbulence divergence, comparing articles popularity ranking for consecutive months between Dec, 19 and Dec, 20.** 
Including all pages and alpha = 0.3. 
Comment on recognizable events (Covid and so on), on recurrent topics, seasonal topics etc... 

{% include stats_dates.html %}
**Figure 3.** Make title and comment. Explain what each contribution represents, how it was computed.

## Focusing on 2 specific months

### TODO main title

{% include heatmap_setsize.html %}
**Figure X. Allotaxonomic 'rank-rank histogram' comparing articles ranking between July, 17 and March 23.**
The main purpose of this graph is to observe the effect of the selected top N pages on the rank-rank distribution. Moving the slider from left to right includes the top 1'000 pages for both months up to all the pages. In other words, we're including the top N pages, with N fixed by the slider step.
_Explain axes, slider, hover data examples, why I chose to compare those 2 dates._
Comments : exclusive types -> lines at the border. Since we use fractional ranking, all the pages which do not belong to either set are assigned to the same last rank. Pages existing in one of the two compared months are called "exclusive types". 
As we increase N (so called set size), we increase the number of exclusive types for the month of March 23. Indeed, for N smaller than 1'000'000, the number of exclusive pages belonging to either July, 17 or March 23 is rather balanced. 
But for N larger than 1'000'000, the contribution becomes unbalanced. Including all pages from both months, we end up with 9% of the exclusive pages belonging to July 17, and 91% to March 23. 
_Add that in total, 58% of pages belong to March 23, and they gather 53% of all the views. Explain and cote growth of Wikipedia, more pages were created but fewer were deleted and the deleted belonged to the tail_. 
Near exclusive types.
Pages in the middle of the graph, on the diagonal can be considered as stable since their rank in July, 17 falls into the same bin as their rank in March 23. As we move away from the main diagonal, we progress towards the exclusive types. 

{% include divs_setsize.html %}
**Figure XX. Rank turbulence divergence top 40 pages contribution, comparing articles popularity ranking between July, 17 and March, 23.**
alpha = 0.3. Comment on the graph -> exclusive types for March 23 make the difference. Effect of subsampling data on the divergence contribution. 
Comment on topics brought up -> FP Angelsberg Malware and Cleopatra (limitation ?), movies and actors, seasonal (Independence day), event related : ChatGPT and Malaysia airlines flight, sports, recurring : deaths, politics : APJ Abdul Kalam.

### Exploring Rank-Turbulence Divergence tunability

{% include divs_alphas.html %}
**Figure X. Rank turbulence divergence top 40 pages contribution, comparing articles popularity ranking between December, 20 and January, 21.**
Explain both ends of spectrum and what it highlights : exclusive types versus common types.
Detail pages per topic -> highlights different needs.
Considering all pages. Number of pages and total views gathered are about the same for December 20 and January 21. Over all pages that are exclusive, 38% do not exist anymore in Jan 21, and 62% are unique to Jan 21. _For alpha > 0.01, pages from Jan 21 contribute 52% to overall divergence._

## To conclude






