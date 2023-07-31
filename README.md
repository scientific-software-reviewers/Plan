# Plan for tutorial exercises


### What if getting started is too hard?

Part of the tutorial is getting familiar with GiHub, but setting up a GitHub account and setting up the tutorial may be a high bar to entry.
One of the goals of this project is to get people looking at open source software. With this in mind, a 'take-a-look' repository with the 
exercise issues and pull requests will be available. This allows people not yet comfortable running their own GitHub actions to walk though the tutorial.
 
### What are the main learning outcomes?

Get people thinking about the following:

When reviewing:  

* Does the pull request address the issue?
* Are there any deal breakers that would stop you accepting the changes?
* Can you suggest any improvements?
   * What is a good way to phrase your suggested improvements?
* Is the solution overly complicated? For an example of an overly complicated solution, see the famous [fizz buzz in Tensorflow](https://joelgrus.com/2016/05/23/fizz-buzz-in-tensorflow/).
* Are the comments up to date, necessary, helpful?
* Would you except the pull request as it is now? Are your suggested changes must-do? nice-to-have? nitpicks? How would you communicate this?
* Do you spend a lot of time reviewing the code style?  Is it worth having a style guide for contributors? Can you make use of an existing style guide? Or a linter?

When workng on your own contributions:  

* When putting in a pull request, how can you make it easy for a reviewer to understand what you have done?
* What makes a good pull request, what makes a bad pull request?
* Can you commit code in a way that lets someone review your code more easily?  Should you separate functional changes from style changes?
Would you use a tool such as [commitizen](http://commitizen.github.io/cz-cli/) to prompt yourself at commit time? Why? Why not?

### What prerequisite knowledge does someone need?

Ideally, it would be good to have minimum coding knowledge to get started reviewing.  The text exercises make no assumptions about coding
knowledge. Variations in cultural knowledge always exist and it is important to have this in mind when writing or reviewing.
Text exercise 2 is an example of culturally specific mixup. 
Python is used by people across various domains by people with various scientific and non-scientific backgrounds.  The python exercises 
will be at the "introduction to python level" found in "learn python" tutorials. 
Fortran has a more restricted user base in terms of which domains people work in. These domains typically have numerical code. For Fortran
exercise 1, some mathematics knowledge is assumed. 





## Text exercises

### Text Exercise 1. Recipe for Cake

Issues with the recipe:

* Mixture of imperial and metric units
* Organization of ingredients vs. baking instructions

Pull request:

* Reorganizes the recipe to have a list of ingredients first
* Missing some units on the list of ingredients

Exercise:

* Does the pull request address the issue?
* What would improve the pull request?
* Add your suggestions on the pull request using the comment feature. When would you use a comment vs. a suggestion?


### Text Exercise 2. Terminology in an article about the Women's world cup

Issue:
In an article about the Women's world cup there has been a mix up between football, soccer, and the NFL.

Pull request:

* Defines terms at the start of the article
* Has a paragraph on the author's favorite NFL team


Exercise:

* Does the pull request address the issue?
* Is the solution overly complicated?  Add a comment on what you think is unnecessary?  What is a good way to phrase your comment, what is a bad way?
* What would improve the pull request? Add your review: Approve or Request changes
* For your own code, do you write for a global audience? Would [Google's developer documentation style guide](https://developers.google.com/style/translation) be helpful?

### Text Exercise 3. Origami instructions 

Issue: The set of instructions for folding a paper plane is missing a step.

Pull request:

* Has the missing instruction
* Duplicated one of the existing steps
* Has added a bunch of white space changes

Exercise:

* Does the pull request address the issue?
* Are there any unnecessary or incorrect changes?
* What would improve the pull request?


## Python exercises

Possible topics to cover:  

  * exception handling 
  * variable names
  * mis-understood requirements
  * tests
  * documentation
  * comments - do these add useful information?
  * repetition


### Python Exercise  1. Printing out vowels and consonants

Covers: Requirements, documentation, comments

Issue: A program to print out the number of vowels and consonants in a string is only printing out the number of vowels.

Pull request:

* Comments are from the original version of the code
* New comments have authors initials and dates
* Two functions have the same docstring (maybe a copy and paste error)
* y is being counted as a vowel

Exercise: 

* Does the pull request address the issue?
* Are the comments up to date, necessary, helpful?  Would you remove some of these comments? Add suggestions for which comments to remove
  and/or change.
* Are there any bugs?
* What would improve the pull request?  Could you use list comprehension? Would you except the solution as it is now?

### Python Exercise 2. Calulcating the number of experiments 

Covers: exception handling, variable names, repetition

Issue: A program to calculate the number of experiment windows between two times does not check the user input for acceptable values. 

Pull request: 

* Raises an exception if the input is above the acceptable
* Adds exception handing if the user enters a string rather than a number
* Changes all the variable names 

Exercise:

* Does the pull request address the issue?
* Are there any unnecessary or incorrect changes?  
* What would make the pull request easier to review?
* What would improve the pull request?  Add a comment.

## Fortran exercises


Possible topics to cover:  

  * variable names
  * private variables
  * comments - do these add useful information?
  * integer division
  * floating point numbers
  * intent in/out for derived types
  * allocatable arrays 
  * [Mistakes that might surprise you](https://fortran-lang.discourse.group/t/mistakes-in-fortran-90-programs-that-might-surprise-you/2687)

### Fortran Exercise 1. Calulcating PI

Covers: variable names, integer division, floating point numbers

Issue: The program to calculate pi is giving incorrect results because of integer division

Pull request:

* Fixes the integer division
* Changes the precision of some of the numbers

Exercise:  

* Does the pull request address the issue?
* Are there any unnecessary or incorrect changes?  
* Why did the author change the precision? Can you find the commit message with the reason?


### Fortran Exercise 2. Refactoring to allow code to be reused

Covers: private variables, intent in/out for derived types

Issue: Functions that are currently in a main program need to be made available to other programs.

Pull request:

* Refactoring: Moves functions from the main program into a module
* Makes some module variables public
* The derived type has intent out
* The comments in the main program have not been updated

Exercise:

* What would make the pull request easier to review?
* What would improve the pull request?  Add a comment.
* Are the comments up to date, necessary, helpful?  Would you remove some of these comments? Add suggestions for which comments to remove
  and/or change.
* Which module variables and routines should be public? Add a suggestion for which variables/routines to make private to the module.
* Have any bugs been introduced during the code refactoring?




