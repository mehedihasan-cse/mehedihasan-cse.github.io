---
title: "Depression Detection From Bengali Text On Social Media Using Machine Learning Algorithms."
collection: publications
permalink: /Depression-Detection-From-Bengali-Text-number-1
excerpt: 'This paper is an ongoing process.'
date: 2023-09-25
venue: 'THE 2ND INTERNATIONAL CONFERENCE ON CROSS-DISCIPLINARY ACADEMIC RESEARCH (ICAR)
paperurl: 'http://academicpages.github.io/files/ICAR_ Full Paper_DepressionX.pdf'
#citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal #1</i>. 1(1).'
---

Depression is a serious public health concern that has a significant negative impact on a person's mental 
condition. It changes their acts, behaviors, mental health, and interactions with others. When individuals
can no longer handle this mental stress, they commit suicide. According to the WHO, 850,000 people die 
every year because of the most severe depression. The majority of people in low-income nations struggle 
with depression. Only an early diagnosis of depression can play a vital role for the person to get the proper therapy, which will allow him to resume his everyday life. This research looks into how machine learning algorithms can be used to identify depressed people from social media comments. There are millions of speakers of the Bangla language around the world, considering this Bengali social media community was 
chosen as the data source. The dataset was classified into two classes according to the commenter's 
emotional condition. Various algorithms, such as SVM, Logistic Regression, Decision Tree, KNN, 
Multinomial Naive Bayes, and CatBoost were applied. The study's findings indicated that the SVM 
algorithm performed the best and was capable of detecting depressive text from the given dataset. This 
outcome indicates that text data from social networking sites could represent valuable insights and by 
utilizing these insights of text data depressive persons can be detected. Additionally, the results can be used to design automated tools for detecting the real-time depression rate among people and necessary treatment can be taken as well.


----


{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

<!-- New style rendering if publication categories are defined -->
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
