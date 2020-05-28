# CARMA Short Course 2020: Introduction to Python and Content Analysis of Text

## Overview

Content analysis is a structured way to extract meaning from artifacts (e.g., texts, images, videos), and its application ranges from qualitative to quantitative research designs.
Using modern computational techniques, we can bridge the two designs to varying degrees, retaining more of the depth of qualitative research at the traditionally larger scale of quantitative research.

This short course focuses on computational approaches to content analysis that enable large scale quantitative research using text data, with a particular emphasis on the foundational skills of identifying, collecting, and preparing text data using Python.
We will begin with an overview, emphasizing the specific skills that have a high return on investment for researchers.
Then, we will walk through foundational Python skills for working with data.
Using those skills, we will cover collecting text data at scale using several techniques, including web scraping and application programming interfaces (APIs).
From there, we will extract meaning from text, in the form of quantitative measures, using computer-augmented human coding, dictionary methods, supervised machine learning, and unsupervised machine learning.
By the end of the course, you will have the skills—and many hands–on code examples—to conduct a rigorous and efficient pilot study, and to understand the work needed to scale it up.

The course design does not assume any prior training, though reasonable spreadsheet skills and some familiarity with one of the commonly–used commercial statistical systems is helpful.
In particular, no prior knowledge of Python is required, and we will cover an introduction to Python in the beginning of the course content.


## Prerequisites

The skill requirements assume essentially no prior training, though reasonable spreadsheet skills and some familiarity with one of the commonly--used commercial statistical systems (in either micro or macro work) is helpful.


## Schedule

The course is divided into five sections, each with two 75 minute segments, with breaks between segments.
In most segments, we will briefly cover some concepts with slides, then we will walk through notebooks to see and experiment with code, and use breakout rooms to apply those concepts further.


### Applied methods

segment | topic
---|--------
0a | Introduction
0b | Setup, Anaconda, and Jupyter
1a | Python basics I
1b | Python basics II
2a | Data handling
2b | Data retrieval
3a | Text analysis I
3b | Text analysis II
4a | Supervised learning
4b | Unsupervised learning



## Materials

The materials for this course are available in a course Dropbox shared with participants, and they are also posted in a public Github repository.

There is a notebook and slide deck for each segment.
The slides are available in zip archives containing Keynote and Powerpoint versions in the releases section (on Github) and in a subfolder in the course Dropbox.
Please note that the Keynote slides are (usually) the ones actually presented.

Also, there is an `environment.yml` file for setting up your Anaconda environment, using the instructions below.


## Preparing for the course

Before the first meeting, please complete the following.
If you encounter issues, get as far as you can, and we will work through them in class.

**Please note:** It is best to install (and work with) this software on a physical computer (i.e. not virtualized) that is not locked down with IT permissions.


### Install software

1. Install [Anaconda, Python 3.7 version](https://www.anaconda.com/distribution/).
1. (optional, but encouraged) Install Microsoft Visual Studio Code. The Anaconda installer asks if you would like to install it.
1. (experts-only alternative) Install miniconda instead of the GUI version. While there are direct download versions, you would typically use a package manager (e.g., brew on macOS, apt on Ubuntu). Similarly, you could install VS Code with your package manager as well.


### Importing the Anaconda environment

1. Open the Anaconda Navigator app.
1. On the left, click Environment.
1. At the bottom of the resulting main window, click Import.
1. In the resulting popup, click the folder icon, navigate to the `environment.yml` file, and click Open.
1. Back in the import popup, the environment name should be filled in automatically from the file, `carmapy` in this case. Click Import.
1. Wait for the packages for the environment to be downloaded and installed. This could take a few minutes.

**Note:** there is also a file named `environment_full.yml`.
This file is much more specific about particular software versions, and it is largely specific to both macOS and particular hardware.
I include it for documentation reasons, but you should generally use the more general (i.e. compatible) `environment.yml`.


### Install the Jupyter Lab Extension for Plot.ly

1. Open a terminal (on Windows, use the prompt labeled either "Anaconda Prompt" or "Anaconda (64-bit)" in the start menu).
1. Activate the `carmapy` environment using the command `conda activate carmapy`.
1. Install the extensions using these commands:

```
jupyter labextension install jupyterlab-plotly@4.7.1
jupyter labextension install @jupyter-widgets/jupyterlab-manager plotlywidget@4.7.1

```

**Note:** On my desktop, each command listed above takes between two and three minutes to complete, so give it time. For your reference, these instructions are adapted from the [plot.ly getting started](https://plot.ly/python/getting-started/) document.


### Install TextBlob text corpora and spacy word models

1. Open a terminal (on Windows, use the prompt labeled either "Anaconda Prompt" or "Anaconda (64-bit)" in the start menu).
1. Activate the `carmapy` environment using the command `conda activate carmapy`.
1. Install the corpora using the command `python -m textblob.download_corpora`. There may be warnings or errors that are not relevant for our purposes, but you should see a series of successful downloads.
1. Install the spacy English models using the command `python -m spacy download en_core_web_lg`.


### (optional) Run intro notebook

You can run the notebook that we will use in the first session as a test of whether the most important packages are working properly.


1. Open Anaconda Navigator.
1. Near the upper left of the main part of the window, find the control labeled "Applications on" followed by a drop down box (usually containing "base (root)").
1. Click the dropdown and select `carmapy` which the environment you installed in the instructions.
1. After a few seconds, the main window will refresh. Then, find "Jupyter Lab" and click the "Launch" button.
1. A browser window will pop up, and the Jupyter Lab interface will load. Note: if you appear to have a blank page, make sure you are using a modern browser like Safari, Chrome, or Firefox as your default. Older versions of Microsoft's browsers (even on Windows 10) lack modern features, though the newest Microsoft Edge browser should be fine.
1. On the left side of the Jupyter Lab interface, use the file browser to navigate to the location where you saved the `0a_intro.ipynb` notebook and double click it. Note: if you are using the Dropbox version, the folder is read only, so you should copy the files somewhere convenient.
1. Once it loads, click the "Kernel" menu in the menu bar (inside the Jupyter Lab interface), and then click "Restart Kernel and Run All Cells..."
1. The notebook should run quickly, and you should not see errors. Note: the single most common issue with any import errors at the top is that you have not selected the environment in step 3 above. You need to do that before launching Jupyter Lab, and a subsequent change will not affect the already--running Jupyter Lab.


## About Jason

Jason T. Kiley is an Assistant Professor and Spears Fellow at Oklahoma State University.
His research examines the interplay of audience perceptions of firms, impression management, and their associations with outcomes, including recent publications in the Academy of Management Journal and Strategic Management Journal.
As part of his work, he works to advance the use of software to increase the range, efficiency, and rigor of conducting empirical research.
He is a co-organizer of the annual AOM Content Analysis PDW, and his published and in-progress work often uses state-of-the-art content analysis techniques, including recent work with semantic text analysis and machine learning.
