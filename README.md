# Project of Data Visualization (COM-480)

| Student's name     | SCIPER |
| ------------------ | ------ |
| Naël Dillenbourg   | 288423 |
| Victor Schneuwly   | 311018 |
| Anne-Laure Tettoni | 295880 |

[Milestone 1](#milestone-1) • [Milestone 2](#milestone-2) • [Milestone 3](#milestone-3)

## Milestone 1 (29th March, 5pm)

**10% of the final grade**

This is a preliminary milestone to let you set up goals for your final project and assess the feasibility of your ideas.
Please, fill the following sections about your project.

_(max. 2000 characters per section)_

### Dataset

The dataset that we want to explore is on this website : https://lobbywatch.ch/fr/node/197.
It is about lobbies, groups of interest and the politicians they are affiliated to in the landscape of Swiss politics. We have information about every currently elected politician, and various groups of interest that are active in Switzerland, as well as the connections between them. In terms of quality, it is already quite clean, although there are a lot of different files that we need to explore to better understand them, and decide which ones are the most relevant for us to use. A step that may also be necessary is translating the feature names from German to English.

### Problematic

With this project, the aim is to create a visualization that will educate and inform Swiss citizens and people living in Switzerland about the work being done in Bern to influence our elected politicians. It will also show the affiliations of certain parties and politicians. We want to continue the project of [Lobbywatch](https://lobbywatch.ch/fr), which is to give better transparency to Swiss politics. We want to create a navigable view that is global, where people can explore parties, politicians and groups of interest without having to navigate across many different pages, as is the case on the website we got the data from. We want to create a visualization to help citizens understand the global patterns in lobby involvement in the parliament better, which will bring a better understanding of Swiss society in general.

### Exploratory Data Analysis

The data has 245 members of parliament, affiliated to 7 parties. The exploration is in the notebook ["exploration.ipynb"](/notebooks/exploration.ipynb). An interesting feature is whether the affiliation to a group of interest is paid or not.

### Related work

The website [Lobbywatch](https://lobbywatch.ch/fr) already contains visualizations, but there isn’t one as broad and general as what we want to do. On the website, one can browse and find each person and see how they are linked to certain groups of interest, as well as the strength of the link. We also see if they are paid or not for their work related to the group of interest.
Our approach is to have one visualization, that regroups the most pertinent information of the data. Here is an inspiring visualization : https://observablehq.com/@d3/zoomable-circle-packing?intent=fork.

## Milestone 2 (26th April, 5pm)

**10% of the final grade**

## Sketch of the final product :
![Sketch](Images/circles.png)
![Sketch2](Images/sketch2.png)


## Tools, lectures needed : 
For the main visualization, we will need D3 and JavaScript, covered in lectures 2, 3, 4 (“JavaScript”, “D3”). We will also obviously need data, covered in lecture 4 (“Data”), and ours is in JSON form. We will want the visualization to be interactive (with clickable circles that zoom in or out of the visualization, and that relates to lecture 5 (“Interaction”, “Interactive D3”). We will also try to be careful with colors to create something aesthetically pleasing, as well as meaningful (certain colours will represent certain parties, to be able to give a good ensemble view) (lecture 6 “perception, color”). And lastly, we will want the visualization to be contextualized and for that, lecture 12 (“Storytelling”) will be useful.

## Goals breakdown
- Clean data, keep only useful features, make it usable
- Create main visualization : a big circle for each main category of groups of interest, subcircles inside for more specific categorization (e.g, as in sketch : "Agriculture" has as a subcategory "Anti-OMG"), and inside, smaller circles, each representing a person. The background of the person's circle is a specific color, representing the party they belong to, and people of the same party are in the same zone.
- The bigger the person's circle, the more efficient they are (there is a notion of efficience on LobbyWatch's website, here is how it looks on the website : <img width="150" alt="Capture d’écran 2024-04-18 à 3 35 13 PM" src="https://github.com/com-480-data-visualization/data-viz/assets/56971914/4f3bf4f3-05e8-4846-922e-0d00fc66aad7">). So there are 3 possible widths.
- Each person's circle has the title of the related group of interest under their name, and a "$" sign if they were paid for their commitment.
- The border of the circle is different depending on whether or not the relation to the lobby is direct or indirect. Direct means they worked directly with them, indirect means they invited someone who works with them in the parliament. (<img width="150" alt="Capture d’écran 2024-04-18 à 3 40 18 PM" src="https://github.com/com-480-data-visualization/data-viz/assets/56971914/49b51048-1556-4f55-911a-f712b813df9d">). So there are two possible borders, one that is a continuous line for direct, and one that is a dashed line for indirect.
- Extra idea : represent the statistical variance in interest groups (for example, the socialist party is very active, while the "Verts libéraux" are less active). So for example, see which parties have a lot of variance in them : some very active people, some very unactive.

## Milestone 3 (31st May, 5pm)

**80% of the final grade**

## Late policy

- < 24h: 80% of the grade for the milestone
- < 48h: 70% of the grade for the milestone
