# Jon Geiger's Semi-Modular Resume

This project aims to make the process of creating tailored resumes more streamlined. With so many job applications to submit, so many companies ask for different requirements. By making each component of the resume a different part to a whole, it becomes much easier to edit the document to incorporate different skills and experiences to avoid wasting the time of those who look over the document.



## The Format

This will be a brief description of the methodology used to create this resume. 

### `geiger_resume.tex`: The Hub

This is where all of the individual components of the resume are put together. There is actually very minimal code in this document because of the multitude of `input` commands used, referencing other `.tex` files. It's much easier to change the order of single `input` lines, rather than trying to move around a bunch of formatting all the time. 

The resume has five main sections, as well as a title for the top of the page. Four out of five of these sections have modular components, where I didn't see a need to make the **Education** section modular due to it having only one component. 

### `/experience` directory 

Relevant work experience can be mostly unique to a specific job. Because of this, I've started to create two different listings for each work experience, in the `experience/brief` and `experience/full` folders. The `full` descriptions of each job are for use in the Relevant Experience section of the resume, whereas the `brief` descriptions fit nicely at the bottom in the Additional Experience section.  

### `/skills` directory

The skills directory serves a slightly different purpose from the `/experience` directory. The skills directory sorts skills into "general" and "technical," denoted in subfolders with `gen` and `tech`. These subfolders contain files with each set of skills, where each file has each skill splayed out onto a new line. This makes it easy for me to edit and reorder the skills themselves, and having them each in their own file makes it easier for me to reorder the skill categories. 

### `setup.tex`: The annoying bits, shoved in the closet

`setup.tex` includes all of the document information, imported packages, new commands, and useful settings for the document using the imported packages. The title command is also present in this file, which is used for both this resume and any cover letters I send (not included in this repo). 
