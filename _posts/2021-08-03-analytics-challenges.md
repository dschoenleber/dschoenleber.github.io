---
layout: splash

title: "Data-driven organizations as Potemkin villages"
tags: 
  - analytics
  - data org

excerpt: "An analysis of why organizations fail to unleash the value of their data."
header:
  overlay_color: "#000"
  overlay_filter: "0.3"
  overlay_image: /assets/images/marius-badstuber-wFHqJCuGB1g-unsplash.jpg
  caption: "Photo by [Marius Badstuber](https://unsplash.com/@marius_badstuber) on [Unsplash](https://unsplash.com/)"
---

Working in data can be painful, and the mismatch between propaganda and practice in industry has been noticed by many before me. In this post, I am taking two insights borrowed from the amazing book *The Art of Action*, and apply them to analytics, which I hope provides a new angle for analyzing the challenges of building data-driven organizations.

## Prologue

In a recent project, I supported a small analytics team within a large, established corporation, which focused on delivering insights on the usage of their digital products. Given that some of the KPIs reported by the team were tracked by the CEO of this multi-billion dollar company, I was baffled by the lack of power, resources, as well as tooling and technology available to the team -- not to mention the mismatch between job titles and day-to-day duties. To be fair, the company, whose core business is physical rather than digital, had only recently began its digital transformation journey. What is more, there is nothing special about this experience -- I have seen many companies struggling on their journey to becoming analytics-enabled, data-driven companies.  

## Rumblings in the industry

I am by far not the first one [pointing out](https://hackernoon.com/the-ai-hierarchy-of-needs-18f111fcc007) the difference between [expectation and reality](http://veekaybee.github.io/2019/02/13/data-science-is-different/) in data, the challenge of [working in data](https://maximebeauchemin.medium.com/the-downfall-of-the-data-engineer-5bfb701e5d6b), or the lack of effective [analytics management](https://pedram.substack.com/p/modern-data-team). But in my personal bubble, it feels as if the rumblings have begun to get louder.  

Just then, Benn Stancil [hypothesized about](https://benn.substack.com/p/third-rail) why analytics (and, self-identifying as data scientist, I might add data science) often does not deliver the value it claims to be able to provide. Having seen the struggles of organizations to build impactful analytics functions first-hand, this question deeply resonated with me.

## Beyond the individual

In my opinion, the answer to this question cannot be given in a self-reflective way by assessing the analytics role within the organization, but rather by assessing the organization in the light of the analytics function.  

The necessity for framing the analysis of shortcomings in an organizational rather than an individual way suggested itself during reading of the amazing Book *The Art of Action* by Stephen Bungay. The author, a management consultant by trade, decided after many years in the field to write about military history, a topic that fascinated him since childhood. In his writing, he analyzes battles not as clashes between individual commanders or nations, but between organizations. *The Art of Action* takes the reverse approach, by bringing the long-forgotten insights about building effective organizations from 19th century Prussian military to 21st century corporations.

There are two insights from the book that I believe are helpful in providing context for the question above:  

### 1. Scrutinize the org structure

> Every organizational structure makes doing some things easy and doing other things difficult. If the structure makes doing some things so difficult that the is a *conflict* between structure and strategy, the structure will win.  
Bungay, S. (2011), *The Art of Action*, p.143

This is the classical *[no free lunch theorem](https://chemicalstatistician.wordpress.com/2014/01/24/machine-learning-lesson-of-the-day-the-no-free-lunch-theorem/)* applied to organizational structures. But despite its simplicity, it seems to be often overlooked, leading to a plethora of friction for analytics, as I know from my own experience:

* An analytics team is tasked with KPI creation requiring data from different countries, and is pressured by the Product Manager (PM) to do their best to meet a pre-determined deadline. The countries, which are running different operational systems, are caught up in their own set of tasks, and deliver incomplete or "dirty" data via Excel sheets, causing delays and operational overhead.
* Stakeholders raise data quality issues to the analytics team, which in turn tracks the issues back to the source data provided by the backend, operated by a software engineering (SE) team. The SE team does not have a clue what happened, since testing is focused on the core functionality, not the data providing part, and asks for guidance around what could have gone wrong.
* Data Scientists try to implement data science use cases in the cloud, provisioned by the data platform team, and are slowed to grinding halt trying to attain compliance with data protection and security, whose representatives keep on changing their mind on which requirements need to be fulfilled for the platform to be production-ready.

I am not arguing against data protection or security, nor do I believe that an analyst's / data scientist's job is to only do the shiny things. I believe in ownership, in that whatever is required for you to succeed with your task is part of your job. Debugging data anomalies and communicating with stakeholders is clearly part of the job.  

The issue here is that while companies are claiming to be data-driven because they hired some data analysts or data scientists, *the "adjacent" functions required for delivery do not have skin in the game*. These functions are not measured by the successful delivery of the data product, whatever this may be -- they are measured by their performance to deliver software, to output guidelines on compliance or such. How can we expect data teams to thrive under such circumstances? If it were a software team, it had a PM owning the full delivery, with the power to remove obstacles; and it is common sense by now to organize software teams in such a way that [dependencies are minimized](https://www.scrum.org/resources/blog/eliminate-dependencies-dont-manage-them).

This line of thought is also reflected in [Tristan Handy's response](https://roundup.getdbt.com/p/purple-people-the-impact-of-analysts) to Ben's post, which is, as always, spot-on.
As long as companies are product (manager) driven, they are not data-driven. Being data-driven is [beyond tech or meeting arbitrary KPI targets](https://erikbern.com/2021/07/07/the-data-team-a-short-story.html).  

Note that I don't want to point fingers here -- the organizational design was certainly valid and reasonable at some point, but the big question is whether this is still the case. If companies do not really believe that an effective data team can help them, it might be, but if the do, they should scrutinize the way their organization enables or disables the work of the data function.  

### 2. Differentiate between the levels of business activity

Another insight from *The Art of Action* is to break business activity down into three levels: *strategy*, *execution*, and *tactics*. *Strategy* describes the (business) intent, the direction, the *what* and *why*. *Tactics*, in contrast, describes the "standard operating procedures" (SOPs)[^1]. SOPs provide efficiency, they create uniformity and therefore predictability where it provides high value. *Execution*, in turn, focuses on the exploitation of advantages through independent thinking that is aligned with the overall strategy.[^2]

While this distinction might seem merely academic and meaningless, I'll give fleshing it out a try, acknowledging that the result might be an undue oversimplification. In analytics, *tactics* to me mean basic technical skills (e.g. writing SQL) and the practices shaped by tech and tooling (e.g. dbt). Without scalable, efficient, and standardized SOPs, every task might trigger discussions about how to do it, and after a while, we end up with a Rube Goldberg machine. That's why the initial push in the field was [towards establishing SOPs](https://blog.getdbt.com/what-exactly-is-dbt/), and the need for good tooling is far from being saturated. The SOPs in need do not only cover analytics, but more broadly the whole data space. It's chilling to see the data swamp on which analytics is built on in some companies, lacking standardization, data discovery, and data quality measures. *Tactics* plays a vital role in analytics business activity, [but it can be taught](https://benn.substack.com/p/analytics-is-at-a-crossroads).

The level above *tactics*, *execution*, is all about flexibly adapting actions, led by the overall strategy. The questions about what can and has to be done to achieve the tasks deduced from the strategy, which blockers have to be eliminated etc relate to *execution*. This is where analytics brings most value -- the *tactics* is there to ensure things are done the right way, *execution* is to ensure that the right things are done. This is the level where [good and bad](https://ianwhitestone.work/good-ds-bad-ds/) analysts / data scientists differ most. And at the same time, I see seniority -- experience gained outside the concrete function, be it in graduate school or other work functions -- go to waste in many companies. Maybe we haven't learned to "lead upwards" yet, but I wonder whether not often opportunities are [suppressed](https://locallyoptimistic.com/post/agile-analytics-p1) in a [vanilla](https://eugeneyan.com/writing/data-science-and-agile-what-works-and-what-doesnt/) Scrum environment, where the "urgency" of tasks are determined as part of the Product Owner's responsibility, or dictated by the needs of adjacent functions.  

## Conclusion

It's not fair to put the blame for suboptimal results on organizations and back off in resignation. The fact that these issues are passionately discussed by "insiders" shows that there is still so much room to grow -- even on the inside, things look not obvious, how much more from the outside. As a field, I believe we still have a few do-and-adapt cycles ahead of us.

But organizations striving to become data-driven are well-advised to re-think their org structure and make sure that their org structure reflects and enables achieving their real intentions.
If they truly desire to be data-driven, they have to think deeply about how to ensure that the data team has real organizational power, that there is alignment throughout whole organization on the data foundation for the data team, that the [technical debt](https://refactoring.fm/p/the-true-meaning-of-technical-debt) incurred by learning the domain is payed back, that the potential of their hires is taken advantage of by deploying them beyond *tactics*, and to [hire with realistic mutual expectations](https://benn.substack.com/p/third-rail#footnote-anchor-4) and provide attractive career paths for their data hires.

[^1]: An example SOP in the military would be the formation of a road block, in the fast-food industry the chopping of onions, and slide formats in consultancy.
[^2]: Please see chapter seven of *The Art of Action* for a better explanation of the distinction than I have given it here.
