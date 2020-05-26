---
layout: post
title: Analysing Bitcoin - Data Science Fundamentals
date: 2020-05-24 16:53:00 +1200
categories: [blog, datasci]
author: Lee Jordan
published: false
---

<h2>Data Science and Bitcoin</h2>

<p>So, you are interested in data science and cryptocurrencies. You imagine that there must be some way to see how cultural trends may influence the price and/or popularity of your favourite coin(s), but you aren't sure where to begin to compare trends with prices. This article has been written for you. This article also for you if you want to get some idea of following trends, but don't intend to do data science yourself.</p>

<h2>First things</h2>

<p>You cannot determine a casual relationship between most events and cryptocurrency prices. If you are looking for absolute answers (or investment advice), you are not going to find what you seek. Investors look at wide trends and then use their intuition (life experiences) to make hunches - yes, hunches - for investing. If there were simple formulae and answers, then everyone would be rich (but then, if we were all "rich", no one would be). Best not to go down the path of philosophical considerations, here. Suffice it to say that there are no ANSWERS, but by looking at some figures and events, we are going to see how data science might be applied in a simple way to cryptocurrencies.</p>

<h2>Cryptocurrency Question</h2>

<p><i>Do moments of political instability generally increase Bitcoin prices?</i><p> 

<p>This question is too broad to be useful, so how can we limit the concept of "political instability" to something meaningful? Once we define instability, we will need to figure out how to get Bitcoin prices, but let's start with defining political instability.</p>

<h2>Question Definition</h2>

<p>Instability - As our cryptocurrency exchange will be in the USA (with pricing in USD) and the US is a significant market for Bitcoin, we will look at political instability within a US context. Also, while what is defined as "instability" could be considered subjective in many instances, we will limit ourselves to a few events that (hopefully) are generally considered to be times of instability. These will include the election of Donald Trump and the arrival of COVID-19 to the USA, among other events.<p>

<p>Regarding the price of Bitcoin, it has already been noted that we will be using a US Bitcoin exchange. I am going with <a href="https://www.coinbase.com/" title="Coinbase cryptocurrency exchange" rel="nofollow" target="_blank">Coinbase</a>, as I know this company and it has been trading since quite early days (2012), so there is significant data with which to work. You can pick whatever exchanges you want when you do this analysis yourself.</p>

<h2>Initial Data</h2>

<p>You can do analysis on your own machine with <a href="https://rstudio.com/" rel="nofollow" target="_blank" title="RStudio">RStudio</a> or <a href="https://cryptograph.co.nz/jupyter-notebooks/" title="Jupyter Notebooks">Jupyter Notebooks</a>, but this often involves downloading large data files. Because I don't want to again download Bitcoin historical data (and the data cleansing and analysis is slower, even on a decent machine), I will use online data that I connect with the Jupyter Notebooks on <a href="https://colab.research.google.com/" rel="nofollow" target="_blank" title="Google Colab">Google Colaboratory</a>.<p> 

<p>Coinbase's Bitcoin buy and sell data goes back to 01 December, 2014. The data is available at:</p>

<p><a href="http://api.bitcoincharts.com/v1/csv/coinbaseUSD.csv.gz" title="Bitcoin historical data from Coinbase (USD)" rel="nofollow" target="_blank">Bitcoin historical data from Coinbase (USD)</a></p>

<p><img class="img-border" src="https://cryptograph.co.nz/public/assets/images/coinbase-usd-24-may-2020 .png" alt="Coinbase Bitcoin historical dataset for download"></p>

<h2>Jupyter Notebook on Google Colaboratory</h2>

<p>I introduced Jupyter Notebooks briefly <a href="https://cryptograph.co.nz/jupyter-notebooks/" title="Jupyter Notebooks">here</a>. I will be using the Google Colaboratory version, with my working file linked to:</p>

<p><a href="https://colab.research.google.com/drive/1KgRltQDvYXDA_S3uuFdnUtY9giOEetd2?usp=sharing" title="Bitcoin Historical Data Analysis on Google Colaboratory" rel="nofollow" target="_blank">https://colab.research.google.com/drive/1KgRltQDvYXDA_S3uuFdnUtY9giOEetd2?usp=sharing</a></p>

