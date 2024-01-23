# caMicroscope GSoC 2024

<h2 align="center">
  <a href="http://camicro.org/"><img src="https://avatars2.githubusercontent.com/u/12075069?s=400&v=4" style="background-color:rgba(0,0,0,0);" height=230 alt="camicroscope: a web-based image viewer optimized for large bio-medical image data viewing"></a>
</h2>

caMicroscope serves as a digital pathology image viewer, supporting human and machine-generated annotations and markups. The project's source code is available on GitHub at [caMicroscope GitHub Repository](https://github.com/camicroscope/caMicroscope) under the BSD 3-Clause License.

**caMicroscope Organization:**

- The caMicroscope organization hosts various related tools and products, accessible at [caMicroscope GitHub Organization](https://github.com/camicroscope/).

**Communication Channels:**

- **General Communication:** GitHub discussion forums are the primary communication channels.
- **GSOC-specific Communication:** Utilize the [GSOC Forum](https://github.com/camicroscope/GSOC/discussions) for GSOC-related discussions, including project ideas, timelines, and advice.
- **Organization-wide Questions:** For caMicroscope organization-wide questions not directly related to GSOC, use the [general forum](https://github.com/orgs/camicroscope/discussions).
- **Specific Communication:** Issues or discussions on individual repositories should be used for relevant and specific communication.
- **Private Communication:** For private communication with mentors, please email gsoc@camicro.org.

**Selection and "Code Challenges":**

- The caMicroscope mentor/admin team is reevaluating student selection processes. Emphasizing meaningful contributions to caMicroscope over disconnected demos is the priority.
- Refer to the [contribution guide](https://camicro.org/contributing.html) for details on making meaningful contributions.

**List of Ideas:**

- Project ideas have been compiled with input from contributors and collaborators.
- Ideas are not listed in any specific order.
- Submissions are not limited to the provided list but should be relevant to caMicroscope organization goals, see the [roadmap document](https://camicro.org/roadmap.html) for more guidance.
- Discussion on project ideas is encouraged through the [GSOC Forum](https://github.com/camicroscope/GSOC/discussions).

***

## High Dimensional Imaging Support

**Primary Mentors:** Ryan Birmingham

**Overview:** Most of the whole slide image data that we see are RGB images, representing the direct reading from an optical scanner on a tissue sample. This, combined with chemical stains on the image, provides a way to let experts assess an image based on inferences of relative color (e.g. H&E slide pink-purple ratio).
Sometimes, the spatial data represented is not the direct RGB values from a scanner. In this case, we encode three values as RGB. However, caMicroscope does not support datasets which have a spatial representation for more than three channels.
This project aims to add the backend support and frontend interactions to let users make sense of higher-dimensional data via multi-channel imaging support. This should likely be accomplished by adding a supplementary tile server which can read one channel at a time and return it as pyramidal images dynamically, and a user interface to let user select and mix such channels.

**Required Skill:** Image Processing, User Experience

**Difficulty:** Medium 

**Project Length:** Long 

**Source Code:** New Project

## Modularization of Components 

**Primary Mentors:** Nan Li 

Overview: caMicroscope is a web-based biomedical image and data viewer, with a strong emphasis on cancer pathology WSI (Whole Slide Imaging). Application is written in pure javascript, CSS and HTML and it makes developers and contributors easy to understand caMicroscope code base. However, the pure Javascript and CSS makes the code less regular and hard reuse by new features. It is increasing the development and maintenance problems. To keep caMicroscope become a robust and feasible application, the modularization design of frontend components should be involved. It will create a health and feasible fundamentals of caMicroscope development and maintenance. We propose to refactor and create a series of web components to help people who want to learn and use this project quickly creating a customized version to fit their demands.   

**Required Skill:** Prior experience in Javascript, HTML, CSS and Bootstrap. Understand object-oriented design (OOD) 

**Difficulty:** Medium 

**Project Length:** Long 

**Source Code:** https://github.com/camicroscope/caMicroscope 

## Exploratory Annotation Interaction

**Overview:** Annotating images is an essential feature of caMicroscope, and this can be accomplished a vatiety of different ways. Ultlimately, the goal is to let a user share their understanding and perspective, which can be centered on a region of interest of a slide, and entire slide, or a set of slides at once. This project involves basic research and creating multiple varied prototypes of new annotation UX workflows in order to allow for collected data to reflect the perspective and expertise of users.

**Required Skill:** User Experience, Data Visualization

**Difficulty:** Medium 

**Project Length:** Long 

**Source Code:** http://github.com/camicroscope/camicroscope

**Primary Mentor:** Nan Li

## Semantic Data Export and Exploraton

**Overview:** This project focuses on enhancing caMicroscope's data representation by incorporating a semantic layer. The goal is to provide a sophisticated framework for handling slides, annotations about slides, and annotations nested within other annotations. Through the use of semantic representation, we aim to create a more structured and meaningful way to organize and understand the data.

The project involves the development of interactive features, allowing users to seamlessly navigate through the semantic layers, expand or collapse nested annotations, and gain a comprehensive understanding of the relationships between slides and annotations. This holistic approach aims to improve the overall user experience by offering a clearer and more insightful view of the complex data interactions within caMicroscope.

**Required Skill:** Semantic Web

**Difficulty:** Difficult 

**Project Length:** Long 

**Source Code:** http://github.com/camicroscope/camicroscope

**Primary Mentor:** Ryan Birmingham

## Batch Image Visualiation and Annotation

**Overview:** In caMicroscope, images are often acquired in batches, such as during the digitization of multiple samples. These batches, intended to share common features, occasionally face issues like errors in staining, scanning, or labeling. This project addresses these challenges by enabling users to efficiently explore multiple slides visually. Users can add slide-level annotations, such as quality scores or flags indicating a need for re-scanning. This approach ensures a rapid and comprehensive assessment of slides, enhancing the overall quality of datasets within caMicroscope. By providing a quick and intuitive means to identify and address issues, the project significantly contributes to the platform's goal of maintaining high-quality, accurate datasets for robust medical imaging analysis.

**Required Skill:** User Expirence, Image Visualization

**Difficulty:** Easy 

**Project Length:** Short 

**Source Code:** http://github.com/camicroscope/camicroscope

**Primary Mentor:** Ryan Birmingham

## Pathologist Annotation Behavior Report

**Overview:** caMicroscope is a widely used open-source end-to-end platform for digital pathology. Many pathologists use caMicroscope to annotate WSI cases in their daily work. How pathologists annotate on the slide and the different behaviors that different pathologist works on the same slide are interesting questions. It is a good idea to collect and track pathologists’ annotation behavior in caMicroscope. Currently, caMicroscope only tracks the center position and zoom level of the user view. We propose an implementation intended for improving how to track the pathologist annotation behaviors and generating a pathologist behavior report in various formats such as image and pdf. The behavior report generally has the Pathologist’s view on a slide in  timeline and the pathologist's actions in the slide viewer.

**Required Skill:** Prior experience in Javascript, HTML and CSS, Familiar with backend and MongoDB

**Difficulty:** Easy 

**Project Length:** Short 

**Source Code:** http://github.com/camicroscope/camicroscope

**Primary Mentor:** Nan Li

## Eaglescope Automatic Configuration

**Primary Mentor:** Ryan Birmingham

**Overview:** Eaglescope is a web application for exploratory analysis on high dimensional datasets, especially biomedical datasets. This tool has been designed primarily to focus on cohort identification, that is to identify a set of criteria which produce distinct or interesting data. Right now, in order to create a dashboard, the entire layout needs to be specified in a configuration manifest. However, this has the side effect of requiring that users already understand the data well enough to select which possible visualizations would be most interesting.
This project, Eaglescope Automatic Configuration, aims to provide instant statistical insight into which fields or combinations of fields can be best represented in the various different visualizations implemented in eaglescope. This would have the added bonus of letting a user quickly explore a new dataset without writing any configuration. This has been proposed as a short project, and would focus on classical statistical methods. 

**Current Status:** New frontend application

**Required Skills:** UX, JavaScript, TensorFlow

**Difficulty:** Medium

**Project Length:** Short

**Source Code:** https://github.com/sharmalab/eaglescope

&nbsp;
***
# Applying for GSOC

Mentors and evaluators typically look for the following:

- The proposal is clear, relevant, and realistic.
- The contributor has demonstrated the relevant skills to complete the proposal.
- The contributor has shown an interest in open source, especially caMicroscope, including community involvement.

## Application Template

The following template is provided to help organize all required information for a successful GSOC application. While following this template is not required, ensure that your application is complete.

**1) Project Title:**

**2) Abstract / Project Summary:**

Summarize the project in your own words.

**3) Contributor Name:**

**4) Contributor Email and Slack username:**

**5) Potential Mentor(s):**

**6) Personal Background (Brief CV)**

**7) Project Goals**
Describe specific outcomes, measurable or otherwise, as bullets.

**8) Detailed Project Proposal**

Describe what you propose to do for the project.

**9) Project Schedule**

Break the timeline into periods of approximately 7 days. Be clear on project size and timeframe, in compliance with google's requirements.
We also highly recommend including a something to show organization-wide as a demo in advance of both midterm and final evaluations to both show off your hard work, and elicit feedback beyond your mentor(s).

**10) Planned GSoC work hours**

Please indicate the work hours (including the timezone) that you hope to work on your project.

**11) Planned absence/vacation days and other commitments during the GSoC period (including the community bonding period)**

Indicate any examinations or other personal commitments.

**12) Open Source and Skills**

Include and explain your open-source contributions, and explain them as needed. Additionally, highlight your relevant skill set to complete this project. Ideally, there would be some overlap between your open-source portfolio and the skillset, showing familiarity with relevant pieces of caMicroscope's codebase.
