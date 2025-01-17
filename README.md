# Classify website visitor queries into measurable categories

> **Chart and respond to trends in information seeking, by classifying your web visitor queries to a taxonomy and an ontology, using completely anonymized data**

Analytics data for *search* for large web sites is often too verbose and too inharmonious to analyze. One "portal" site studied receives around 150,000 "clicks" per month from search-engine results screens, and around 100,000 queries per month from internal site search. Examining the visitor queries reveals many variations on the same conceptual ideas, making the content difficult to analyze and summarize. For this reason, many web managers are not looking for meaning in the search terms their site visitors are using. 

**We should** put our completely anonymized search queries into "buckets" of broader topics, so subject matter experts (SMEs) have a way to understand how customers are currently seeking information within that SME's topic area. Having this, the SMEs can examine whether existing content should be modified to improve its findability, and whether new content should be added to fill gaps in customer needs. Health/medical analytics managers can use the Unified Medical Language System (UMLS) [Semantic Network](https://semanticnetwork.nlm.nih.gov/) and Semantic Groups, to do this to serve customer information needs better.

Search represents a direct expression of our customers’ intent. We should use this data to improve our staff’s awareness of what our customers need from us.


## Use cases

1. A web analyst could say to a product owner, "Did you know that last month, 30 percent of your home page searches were in some way about drugs? Should we take action on this? How might we **improve task completion** and **reduce time on task,** for this type of information need?
2. We should cluster and analyze **trends we know about.** For multi-faceted topics that directly relate to our mission, we should create customized analyses to collect the disparate keywords people might search for into a single bucket. How can we create a better match between user interest and the content we manage for this topic? Where might we improve our site structure and navigation? 
3. We should focus staff work on **new trends, as the trends emerge.** When something new starts to happen that can be matched to our mission statement, we should deploy social media posts on the new topic immediately, and start new content projects to address the emerging information need.
4. On a longer time scale, anyone publishing to the web might want to ask, how are we preparing to **support voice search**? Understanding how people search for information will help understand how to adapt for this possible next-generation technology.


## Pilot project results

72% of search volume (for October 2019) is tagged with broader-topic names within 3 minutes, after multiple iterations that updated the tagging files. This was 205,633 of 282,387 searches (72%), and (because the logs are already aggregated) 30,604 of 89,476 rows (34%) were tagged. What are untagged are terms searched less than a monthly average of once per day, that are often multiple-concept searches of low frequency.

During the pilot we did not create supplemental files for the MetaMapLite or CSpell tools. This would improve results. 


## Screenshots

<kbd><img src="https://github.com/NCBI-Codeathons/Use-UMLS-and-Python-to-classify-website-visitor-queries-into-measurable-categories/blob/master/screenshot-input.png" alt="screen to upload file" /></kbd>

<kbd><img src="https://github.com/NCBI-Codeathons/Use-UMLS-and-Python-to-classify-website-visitor-queries-into-measurable-categories/blob/master/metamap%20output.JPG" alt="UMLS Semantic Types Categories" /></kbd>


## Workflow

Only partially implemented during this Codeathon.

<kbd><img src="https://github.com/NCBI-Codeathons/Use-UMLS-and-Python-to-classify-website-visitor-queries-into-measurable-categories/blob/master/workflow.png" alt="Workflow" /></kbd>


## Dependencies

### Tools

* Python
** Pandas
** FuzzyWuzzy for fuzzy matching and clustering
** Matplotlib
* [MetaMap JAVA API](https://metamap.nlm.nih.gov/JavaApi.shtml)
* [CSpell - Spell checker for consumer language](https://lsg3.nlm.nih.gov/LexSysGroup/Projects/cSpell/current/web/index.html)
* Optional
** Linux UI
** Flask
** Django if assistance in manual matching is needed.

Yet to be integrated; may be useful:

- Medical language abbreviations
- Scikit-Learn multi-class classifier


## Additional output

Search Strings input used for MetaMap and FuzzyWuzzy
![alt text](https://github.com/NCBI-Codeathons/Use-UMLS-and-Python-to-classify-website-visitor-queries-into-measurable-categories/blob/master/wordcloud_search_strings.JPG "Search terms")


## Future work

- Implement tagging interface that provides suggestions for untagged queries above a frequently threshold, to facilitate manual tagging.


## Influences and thanks

* Aronson AR, Lang F-M. (2010). [An overview of MetaMap](https://ii.nlm.nih.gov/Publications/Papers/JAMIA.2010.17.Aronson.pdf). J Am Med Inform Assoc 2010;17:229-236. PMID: 20442139. doi:10.1136/jamia.2009.002733
* McCray AT, Burgun A, Bodenreider O. (2001). [Aggregating UMLS semantic types for reducing conceptual complexity](https://www.ncbi.nlm.nih.gov/pubmed/?term=11604736). Stud Health Technol Inform. 84(Pt 1):216-20. PMID: 11604736. See also https://semanticnetwork.nlm.nih.gov/
* Lai KH, Topaz M, Goss FR, Zhou L. (2015). [Automated misspelling detection and correction in clinical free-text records. J Biomed Inform](https://www.ncbi.nlm.nih.gov/pubmed/?term=25917057%5Buid%5D). Jun;55:188-95. Epub 2015 Apr 24. PMID: 25917057. doi: 10.1016/j.jbi.2015.04.008.
* Lu C, Aronson AR, Shooshan SE, Demner-Fushman D. (2019). Spell checker for consumer language (CSpell) Journal of the American Medical Informatics Association. Mar;26:3:211-218. PMID: 30668712. doi: https://doi.org/10.1093/jamia/ocy171. 
* Thanks to NCBI Codeathon staff and participants; NLM-PSD-RWS Management; 2017 HHS Data Science CoLab Bootcamp (HHS-CTO and participants); MetaMap and UMLS staff; OCCS Desktop Support; Data Society staff; many reviewers.


## People

* Dan Wendling, team lead, NLM/LO/PSD
* Dmitry Revoe, NLM/NCBI/MGV
* Victor Cid, NLM/LHC/CgSB
* Laritza Rodriguez, NLM/LHC/CSB
* Wenya Rowe, NLM/NCBCI/CBB
* Rachit Bhatia, NLM/OCCS/STB

## Past work

https://github.com/NCBI-Hackathons/Semantic-search-log-analysis-pipeline
