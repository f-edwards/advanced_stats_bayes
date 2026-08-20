---
layout: default
---

| Advanced Statistics: Bayesian   | 27:202:641 |  
| Monday, Tuesday 10:00AM - 12:40PM | Room: CLJ 574 |
| Instructor: Frank Edwards | frank.edwards@rutgers.edu|
| Office hours: Wednesday 10AM-12PM | Room: CLJ 579B |

## Quick links

[Lecture slides](https://github.com/f-edwards/advanced_stat_bayes/tree/master/slides)

[Homework assignments](https://github.com/f-edwards/advanced_stat_bayes/tree/master/hw)

## Prerequisites

This course requires previous graduate-level coursework in statistics. Students are expected to be comfortable with probability, statistical inference, and generalized linear models. Instruction will be in R, but users of Python or Julia are also welcome.

If you are new to to R, I recommend working through chapters 1-8 of [R for Data Science](https://r4ds.hadley.nz/).

## Course description

This is the course syllabus for Advanced Statistics: Bayesian, Fall 2026. It is a graduate-level introduction to Bayesian inference and modeling. Our emphasis will be on applied Bayesian statistics for social scientists. 

Bayesian methods have several advantages over their frequentist analogues: they allow for  incorporation of prior knowledge into our estimates, they are easy to interpret, and they allow for very flexible inference. 

The primary disadvantages of Bayesian methods are 1) increased compute time (less of a problem every year) and 2) the requirement of additional thought and care in specification (this is good, actually). There's are few good reasons not to adopt a Bayesian approach to social science.

We will cover the basics of Bayesian probability, Bayesian updating, causal inference for social science using directed acyclic graphs (DAGs), and regression using Markov Chain Monte Carlo (generalized linear models through multilevel models). Throughout, we will pay careful attention to how we connect questions, theory, models, priors, data, posterior inferences, and communication of findings.

## Course goals

1. Become comfortable with Bayesian inference

2. Develop a thoughtful social science workflow

3. Become skilled at connecting theory to explicit causal and statistical models

4. Understand how to conduct simulations for each stage of the statistical workflow

5. Understand how to estimate and interpret Bayesian regression models

6. Produce high-quality data visuals to communicate statistical findings 

## Book

- Required: McElreath. Statistical Rethinking. [Book website](https://xcelab.net/rm/)
	- McElreath has also posted lectures based on the book [here](https://www.youtube.com/watch?v=ztbYkBPDOgU&list=PLDcUM9US4XdPMtSV81e1R_4B6NugQBvTP), I highly recommend them

- Recommended: Kurz. [Statistical Rethinking with brms, ggplot2, and the tidyverse.](https://bookdown.org/ajkurz/Statistical_Rethinking_recoded/index.html)
	- You are welcome to use McElreath's package for modeling and base R for visualization, but I will primarily present material using tidyverse R code and brms. Kurz has written a more or less complete translation of the examples in Rethinking using these packages.

## Communication

Email is my preferred mode of communication. Announcements will be sent to the class listserv. We won't be using Canvas.

## Expectations

- Attendance is required. 

- Bring a computer.

- Complete homework on time. 

- Keep up with the reading.

- Be respectful and professional. 

- Collaborate with your colleagues. 

- Document your code. 

- Try not to use AI tools.

## AI Policy

Large language models have become incredibly good at writing `R` code. They also have caused tremendous social and environmental harm and have been shown to impede learning. 

I will allow AI usage under the following conditions:

1. You do not ask an LLM to complete an entire assignment or homework question. You are here to learn. Please don't waste my time by having me grade LLM output.
2. You first try to solve a problem yourself. You should expect to struggle with the material, it is hard. But the struggle is where learning happens!
3. Only use LLMs for specific advice on technical problems: i.e. 'how do I compute a z-score for a variable in R?' or 'how do I change an axis label in ggplot?'. 
4. Clearly indicate where you used AI in your assignment with the flag **AI support used**
5. Include a full transcript of your LLM sessions. The following prompt will do it: "provide a transcript of this session". Attach this log to homework submissions as `LLM_log.txt`

Companies like Anthropic and OpenAI want you to become paying users dependent on their platforms. You don't want them to own your workflow. You should build you workflow with open-source tools whenever possible. Open-source and on-device models have several advantages for researchers. They don't cost money, they can produce reproducible output, and they keep your data secure. If you are going to use an LLM, I recommend using [Ollama](https://ollama.com/) with Gemma4 (or similar) on your laptop.  

## Software

All instruction will be conducted in the `R` statistical programming language. R is free and open-source, and can be downloaded [here](https://cran.r-project.org/).

We will be using the [RStudio integrated development environment](https://www.rstudio.com/products/rstudio/download/). RStudio provides a powerful text editor and a range of very useful utilities. Positron is similar and is an acceptable choice if you prefer it.

In addition to writing code, RStudio a great tool for writing reports, papers, and slides using [Quarto](https://quarto.org/), which is a plain text format based on markdown. This syllabus, most of my course materials, and most of my academic papers are written in markdown. 

You are required to submit assignments as rendered Quarto output. 

Lastly, I recommend learning some form of version control to ensure your work is a) backed up, b) easily accessible to collaborators and c) reproducible. Git and GitHub are great and flexible tools for software development that have powerful applications for researchers. Here's a useful [intro to GitHub](https://happygitwithr.com/) for R users.

We'll be using the packages `cmdstanr`, `brms`, `tidyverse`, and `tidybayes` frequently. 

If you'd like to clone the course repository on your laptop, you can run

```
git clone https://github.com/f-edwards/advanced_stats_bayes.git
```

To keep it up to date with current slides and homework, just navigate to the course directory (`cd advanced_stats_bayes`), then run

```
git fetch
```

## Assignments and grading

Grades are based entirely on homework assignments. I grade assignments with a simple 2 point scale, and am generally a forgiving grader. If your work indicates a serious effort to complete the assignment, you can expect to receive full 2 points of credit. If you submit incomplete or sloppy work, you can expect 1 point of credit. Incomplete work will receive a zero.

Statistics is hard, and I prioritize growth and learning over getting correct answers in grading and evaluation.

All students who work hard and complete the assignments can expect to receive an A as their final grade. 

### Homework

I will assign homework each week. Assignments are due on Sunday by 10pm. Email your homework assignments (output and source code) to the instructor.

Don't wait until the last minute to get started. These homeworks should take you on average about 6 hours of work to complete. Space that work out and give yourself time to ask for help from your peers and your instructor. 

Group work is strongly encouraged. I recommend scheduling a time to meet with your classmates to work on the problem sets collectively. Quantitative research is a team sport, but I still do expect you to write your own code and interpretation. Don't just copy/paste from your peers, the internet, or a chatbot. Cheating will make me grumpy, please don't do it. 

Life happens. All students are granted two free extensions on homework, no questions asked. Just email prior to the due date to let me know you'll be taking an extension and when I should expect your submission.

## Course schedule, topics, and readings

**Week 1**

Reading: 
- Rethinking Chapter 1 

- 9/1: Introduction
	- All models are wrong...
	- Connecting scientific knowledge to models
	- The importance of generative models
	- Software install and setup
	 
- HW 1 Due 9/6 

**Week 2**

Reading: Rethinking Chapter 2

- 9/8: Bayesian probability, 1
	- Counting, permutations, combinations
	- Probability as plausability, probability as limit under replication
	- Introducing prior information
	- Updating information with the posterior distribution

- HW 2: Due 9/13 (Extension available for Rosh Hashanah)

**Week 3**

Reading: Rethinking Chapter 3

- 9/15: Bayesian probability 2
	- Linking models to Bayes theorem
	- Review of random variables and densities
	- Introduction to prior simulation
	- Learning from the posterior distribution

- HW 3: Due 9/20 

**Week 4**

Reading: Rethinking Chapter 4 

- 9/22: Linear regression 1
	- Normal distributions 101
	- Why linearity?
	- Priors and prior prediction
	- Posterior inference

- HW 4: Due 9/27 

**Week 5**

Reading: Rethinking Chapter 8

- 9/29: Linear regression 2
	- Interactions
	- Treatment heterogeneity
	- Advanced visualization of posterior inferences with `tidybayes`

- HW 5: Due 10/4

**Week 6**

Reading: Rethinking Chapter 5

- 10/6: Structural causal models 1
	- Introduction to DAGs
	- Confounding 101
	- Interpreting parameters under causal assumptions
	- Interpreting parameters without causal assumptions

- HW 6: Due 10/11

**Week 7** 

Reading: 

- Rethinking Chapter 6
- Lundberg, Johnson, and Stewart, 2021. "What is your Estimand" *American Sociological Review*. https://doi.org/10.1177/00031224211004187

- 10/13: Structural causal models 2
	- Connecting theory to a causal graph
	- Associations, interventions, counterfactuals
	- Common structures in DAGs
	- Structures leading to confounding
	- Backdoor paths, d-separation, and identfying adjustment sets

- HW 7: Due 10/18 

**Week 8** 

Reading: Rethinking Chapter 7

- 10/20: Regularization and prior choice
	- What are priors for? 
	- Evaluating priors through simulation
	- Why regularization is good
	- Choosing informative priors
	- Model comparison with LOO and WAIC

- HW 8: Due 10/25 

**Week 9** 

Reading: Rethinking Chapter 9

- 10/27: Markov Chain Monte Carlo
	- Metropolis algorithm
	- Gibbs sampling
	- Hamiltonian Monte Carlo
	- Basics in cmdstanr and brms
	- Diagnostics for convergence
	- Troubleshooting convergence problems

- HW 9: Due 11/1 

**Week 10** 

Reading: Rethinking Chapter 10

- 11/3 GLMs
	- Understanding generalized linear models and link functions
	- Taxonomy of common distributions used for GLMs
	- Link functions, parameters and prior choince

- HW 10: Due 11/8 

**Week 11** 

Reading: Rethinking Chapters 11 (12 optional)

- 11/10: GLMs 2
	- Bayesian logistic regression
	- Bayesian Poisson models
		- Other approaches for count data (negative binomial, zero-inflated)

**Week 12** 

Reading: Rethinking Chapter 13

- 11/17: Multilevel models 1
	- Introduction to multilevel models
	- The benefits of regularization
	- Clustering 
	- Varying intercept models
		- Cross-classification
	- Formula syntax for multilevel models (lme4)

- HW 12: Due 11/24 (extended for ASC)

**Week 13** 

Reading: Rethinking Chapter 14.1-14.2

11/24: Multilevel models 2
	- Varying slope models
	- Other options for clustered trajectories: splines and GAMs
	- Prior choice
	- Posterior inference

- HW 12: Due 11/24 (same hw as week 12)

**Week 14**

Reading: Rethinking 14.3 

- 12/1: Instrumental variables
	- DAGs and IVs
	- Estimation
	- Other approaches to causal inference with observational data

- HW 14: Due 12/6 

**Week 15**

Reading: Rethinking 14.5 

- 12/8: Gaussian processes
	- Introduction to GP
	- Estimation of exact GP
	- Estimation of approximate GP
	- GP as spatial model

- HW 15: Due 12/13
