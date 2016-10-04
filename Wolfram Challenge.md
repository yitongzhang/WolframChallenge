# Approach
There is also no wrong way to illustrate your recommendations - research reports, annotated screenshots, ad-hoc usability tests, flow diagrams, sketches, static wireframes, interactive prototypes, etc. are all acceptable. Just show us how you think and are able to tackle a design problem. More thorough your ideas are, the better it would be of course.

# The problem
## Status quo:
Save files to Desktop, share with others using email, school web portal, dropbox, instructor’s personal site or GitHub.
## What’s wrong with the status quo?
- version control: sharing files directly creates version management issues.
- permissions: sharing files means the only permission is full permission
- friction: using another tool to share and manage files creates extra steps for the users
## Problem statement:
Mathematica users want to share files with one another with varying levels of read/write permissions

# Research Questions
Sample: 2 quick conversations with friends who use Mathematica in grad school. Although the data is not quantitatively representative, it gives us some qualitative understanding of users. Combined with some reasonable assumptions, these interviews give us some context for the act of sharing. 

## How do users currently organize their Mathematica files?
While some users use GitHub, Dropbox seems to be the most popular option. Most email files or use Dropbox links. Few will use GitHub. Most use the native interface of the app. 
## Why do user usually share Mathematica files?
The most frequent sharing use case is sharing between colleagues at a lab of 5-10 people. Sometimes, users share files with themselves to transfer from one computer to another. 
## What are the technical or organizational constraints around file management, version control and collaboration?
Assumptions: 
* Line by line version control is not in the short term road map. Any versioning will be done at a file level.
* Collaborative file editing is also not in the short term road map. Any edits will be done at a file level.
* The collaboration feature will first be implemented on the web Mathematica, from which it is currently harder to share files.


# User flow
Initiator flow: 
1. Initiate share
2. Set share settings
3. See the status of the collaborators on the file

Receiver flow: 
1. Be notified of shared file 
2. See the status of the collaborators on the file 
3. Start “Initiator flow” (if such privilege has been granted)

# Features needed
## Feature 1 - The act of sharing
* How do users initiate the share flow?
* How do users add/remove sharing recipients?
* How do users change permission levels?

## Feature 2 - Displaying shared status
* How are edits to the file displayed?
* How are collaborators and their status displayed?

## Feature 3 - Notifying collaborators
* How are recipients notified of files shared?

# Wireframes
We use wireframes to try out different answers to each of the questions around how to build features. 

## Feature 1 - The act of sharing
### How do users initiate the share flow?
Ideas:
1. Directly from file system 
2. From file system dialogue menu
3. From recent notebooks

Decision: 2 and 3 both are necessarily. As they both the recent and filesystem views display the same files, users should be take action in the same way in both views. 1 would be overkill, because sharing is not used as often as all the other menu options combined.
<img src="http://imgur.com/B06N1Ol">
<img src="http://imgur.com/B06N1Ol">
### How do users add/remove sharing recipients?
Ideas:
1. Add via email
2. Previous collaborators
3. People sharing a same networked license

Decision: Primary box to add via email, secondary “shortcut” panels for people you might already want to collaborate with.
### How do users change permission levels?
1. Toggle between: admin, edit, view
Decision:
## Feature 2 - Displaying shared status
### How are collaborators and their status displayed?
Ideas:
1. Next to files
2. On the sharing setting overlay

Decision: 1 and 2. Next to files provides a quick overview of both who and how many people have have access. A more detailed view of the different collaborator and their permission-level can be viewed from the setting overlay. Finally 3 seems like overkill as typical Mathematica teams are relatively small.

### How are edits to the file displayed?
Ideas:
1. Date of last edit and collaborator only
2. Timestamped history of all edits in a dashboard

Decision: 1 should be enough for small teams. Maybe an eventual enterprise version could use an edit dashboard.


## Feature 3 - Notifying collaborators
### How are recipients notified of files shared?
Ideas:
1. Simple email would suffice. 

Decision: Indeed it should.

## User test
Because of the short timeframe of the exercise, it was difficult to schedule an user test, but here are some of the things I’d like looking to test if I had a chance to:
1. How easily can testers accomplish all tasks related to sharing
2. Are the placement of the different elements intuitive and expected for testers
