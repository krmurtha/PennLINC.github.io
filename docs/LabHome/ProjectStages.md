---
layout: default
title: Stages of a Project
parent: Lab Basics
nav_order: 5
---

# Stages of a Project at PennLINC

There is no such thing as a “quick” scientific project. All projects take careful planning and follow a stereotyped process. Understanding the life cycle of a project is critical for ensuring feasibility, avoiding surprises, and maximizing fun. Given how long any project takes (approximately 1 year minimum) it is essential that every project be carefully thought-out to justify the investment. As ever, the most important question is “What is the question?”


### 1)	Setup the infrastructure

Each project in the lab has a well-defined infrastructure.  See relevant pages including

a) [Project setup overview](https://pennlinc.github.io/docs/LabHome/ProjectSetup/)

b) Project setup on PMACS (coming soon)

c) [Project reproducibiltiy guide](https://pennlinc.github.io/docs/LabHome/ReproSystem/)

d) [Guide to weekly project meetings](https://pennlinc.github.io/docs/LabHome/ProjectMeetings/)


### 2)	Define initial hypotheses

The ultimate impact of any project is largely determined by the question being asked. Spending two years chasing down the answer to a question that is not very interesting is a recipe for disappointment. Start broad (“forest”) and try to identify questions at a conceptual level (rather than methodological) that are likely to be of broad interest to the field. It is good to write these questions down at this stage, even if they need refining. Strongly consider pre-registration and prospectively identify potential replication datasets.


### 3)	Conduct a literature review

This step is skipped at one’s peril. Nothing is worse than sitting down to write a paper and then realizing at that late stage that the question was largely answered by a study you were not aware of. A literature review also is critically important in sharpening hypotheses to maximize the potential impact of the question being asked. As the first author, aim to rapidly become the expert on the topic of the project — do not rely on your faculty mentor to be aware of all relevant literature (often the primary motivation for a project is to explore a new area in which the faculty member is not an expert). It is important to stay organized. All literature reviews must be conducted using a reference management system (i.e., Zotero). Try to be comprehensive at this stage - reading abstracts and examining figures is a way to rapidly get the sense of a new field. This broad overview is usually followed by an extremely detailed examination of the most relevant half-dozen articles.


### 4)	Sharpen hypotheses and outline testable predictions in an analysis plan

As noted above, “what is the question?” is always the most important question. At this stage, the first author should be able to concisely state the overarching hypothesis. It is a good idea to literally write this down, as it will appear in the last paragraph of your introduction. Next, one needs to operationalize how this hypothesis will be tested according to specific predictions that are linked to a defined analytic plan. It is useful to imagine that everything in the study “works” and you get your dreamt-of results. What tests do you need to do to generate these results?


### 5)	Prospectively identify collaborators & co-authors

Authorship on papers is a frequent source of conflict in other labs. The best way to avoid conflict, enhance transparency, and accelerate collaborations is to identify collaborators who will be co-authors on the final paper prospectively. Ask yourself ‘Whose help do you need to get this project done?’ Explicitly inviting someone to collaborate rather than peppering them with questions will often help things go more smoothly. While the number of collaborators may grow (a bit) as the project develops, most of the time most collaborators are fairly obvious from the beginning. While the faculty lead should address author order on large collaborative projects prospectively, do not be afraid to further the discussion.  


### 6)	Identify a replication buddy

The lab standard is to release all analysis code. To ensure reproducibility, all results should be replicated by an independent member of the lab at multiple stages. The replication buddy should be involved in the project from the beginning, and often is the second author on the paper. This is a lot of work and should not be taken on lightly; also think ahead for a long project and ensure that the buddy will be present in the lab for the anticipated duration of the project. See the  [Project Reproducibility Guide](https://github.com/PennBBL/labhome/wiki/Project-Reproducibility-Guide) for more information.


### 7)	Assess data availability & ensure data access

Before one spends too much time on a project, one should ensure that the necessary data is available. This step arguably should come earlier. Much of the impact of a paper is determined by the sample size; small samples reduce statistical power and preclude some methods from being used. In particular, pay attention to key subject level variables such as demographics, symptom scores, and  diagnoses. If the imaging data has already been processed and QA’d, it is good to verify sample size after QA (see also “inclusion criteria and sample construction” below). Note that lab members should receive explicit written approval from the study PI who collected the data prior to a project’s beginning. For the PNC, this includes approval of the data access committee, which meets once per month; please account for this process with regards to timeline / deadlines.


### 8)	Process & QA imaging data

If data has not already been processed, this is an important, and sometimes time-consuming, step. We prefer a highly-structured procedure for image processing to ensure reproducibility, using XCP-based modules whenever possible. See XCP documentation for further information (coming soon). Note that a sub-sample (usually n~10) of subject level data should be replicated, and the main subject-level derivatives produced by the pipeline should be placed in a read-only data freeze for the dataset. For most projects, analyses should only use replicated data that is pulled directly from this data freeze folder. See the  [Project Reproducibility Guide](https://github.com/PennBBL/labhome/wiki/Project-Reproducibility-Guide) for more information.  


### 9)	Clearly define inclusion criteria and construct sample in a reproducible manner

It cannot be over-emphasized how critical this step is, as changes in the inclusion criteria will inevitably require re-doing all analyses as the sample changes. Similarly, the reproducibility of results depends on the reproducibility of the sample selection procedure. Thus, this step should use code to pull in data from the data freeze folder, and arrive at the final sample by filtering the data using clear QA codes. It is a good idea to explicitly go over this step—and the code—with both your replication buddy and the faculty mentor.


### 10)	Data analysis and documentation

This stage is usually the longest, and varies considerably by project. One general point is that organization pays off: keeping code clean and updating your project repo daily guards against both lost work or the risk of nasty code excavation job at the replication stage.


### 11)	 Replicate interim results

As detailed in the [Project Reproducibility Guide](https://github.com/PennBBL/labhome/wiki/Project-Reproducibility-Guide), once a “main result” that will be the organizing hook for a paper is revealed, it is a good idea to call your replication buddy.   Cleaning your code and having them provide both a “true” replication (taking input data and running a model with their own code) and a “technical” replication (i.e., stepping through your code) is advised to make sure errors are caught before a paper is written. (Often, around this stage, a project is presented at a conference — see the conference wiki for more information).


### 12)	 Paper first steps: abstract & figure outline

The scientific narrative of a paper should be readily apparent from the abstract and figures. Before deciding that analyses are “done” it is good to write the abstract and make an outline (in text) of what the figures will show. Oftentimes this step reveals that something is missing, or one or two more analyses need to be done.


### 13)	 Create draft figures

It is often good to create draft figure panels for the entire paper before polishing them for publication. These figures should be made reproducibly so they can be replicated (in the next step). Making beautiful final figures before replication often is not efficient.


### 14)	 Final reproducibility check: Clean code, make github repo, companion wiki, and replicate final results

At this step, one has all the code and results in hand. Before writing (or as it begins), it is important to make a clean github repository that will be submitted with the paper, along with a companion wiki that thoroughly steps interested readers through this code and allows them to reproduce your work. Once this is complete, send the wiki and repo to your replication buddy, who will check your work (see [Project Reproducibility Guide](https://github.com/PennBBL/labhome/wiki/Project-Reproducibility-Guide)). Note that it is imperative to repeat this process if results change in the writing process below; analyses added at a late stage when one is trying to get the paper out the door are likely to be more problematic.



### 15)	Make final figures & write text

In general, we recommend writing the methods, results, and figure legends prior to writing the introduction and discussion. For further information, read [this article](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005619) by Konrad Cording prior to starting your paper. 


### 16)	Polish text with faculty mentor

Experience suggests that the number of draft iterations is a dominant factor in how good the final text of a paper is. Expect 3-5 rounds of revision of the text with your faculty mentor prior to sending the paper to co-authors. Tracking changes and careful version control at this phase is key. Saving paper versions with a date suffix (in format YYYYMMDD) can be helpful. Although Latex is often desirable, most journals require manuscripts to be submitted in Word, so it is recommended to use Microsoft from the beginning of the editing process. One alternative option is to write using a Google Doc to allow all authors to use the same version, and then export to word prior to submission.


### 17)	Integrate co-author feedback

We usually allow ~1-2 weeks for co-authors to provide feedback on a paper. The faculty lead will send a reminder email to those collaborators who do not reply in the specified window.
 

### 18)	Submit paper, code, & post on a preprint server

After months, if not years, of work, you are now ready to submit the paper. The final built PDF should be proof-read several times by various individuals if possible—often, egregious formatting errors or typos are caught at this stage. Furthermore, pay careful attention to the quality of the figures in the built PDF. Note that if figures are large, the journal will downsample these considerably when making the PDF. Note that many reviewers will not click on the “high resolution figure” link available to them—they will just use what is in the built PDF. To avoid spending time creating beautiful figures that result in downsampled, poorly rendered images, the author can submit figures as compressed PDF’s using widely available free software (this depends in part on what type of figures the journal in question accepts). 

Once the paper is submitted to the journal, it is a good idea to put it on a preprint server as well, such as arxiv, bioarxiv, etc (note that bioarxiv does not allow you to remove preprints—only update them). Use of preprints will help generate enthusiasm for the work even while it is stuck in peer review, prevent others from “scooping” you (especially w/ public datasets like the PNC), and also increases transparency. Feel free to tweet the link when it is up.
As noted above, it is the lab standard to submit all analysis code (in the form of a github repo) along with the paper. Please make sure the repo submitted with the paper is cleaned, and does not include old code for parts of the project that did not pan out / were not included in the final manuscript. Including old code can confuse reviewers and others interested in reproducing your work. One way to do this is to make a new public repo that only uses a subset of code from the original working repo.

After they are posted, we advertise new preprints via twitter, and post them on the main pennlinc.io publications page.


### 19)	Revise & resubmit / Repeat as needed

Peer review can be a long process. To use a football analogy, the first submission is like being on the 20-yard line, rather than the 1-yard line. Dogged persistence and a thick skin is critical for navigating peer review. In general, it is almost always better to “show them with data” and perform any additional analyses requested. Even if rejected, it is generally useful to try to address the reviewers’ comments in the subsequent (new) submission, as it is quite possible you will get the same reviewer at the next journal. This stage is often the part of the project that requires the most intense work in order to meet revision deadlines. Quick turn-around for revision and resubmissions is very important to prevent the project from stalling.


### 20)	Celebrate and disseminate

Congrats! Your paper was accepted. Next, make sure it reaches as many eyes as possible, through mechanisms including Twitter, Penn/SOM PR, a post on our website blog, etc. Make sure the final version of the paper is posted on the pennlinc.io “publications” page.
