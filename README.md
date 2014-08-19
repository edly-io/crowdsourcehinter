This is the Crowd Sourced Hinter XBlock. The Crowd Sourced Hinter provides students
with hints when they incorrectly answer a numerical-or text-input problem. Additionally,
the hints that are provided to students are student-made hints.

This XBlock is still under construction. Functionalities to set default hints, properly moderate flagged hints, and lots of improvements to user interface are to be done soon. 

backlog: https://docs.google.com/a/edx.org/document/d/1lOBLZWohwRmnfgwz53gc4b4GdfP4EER3UNohdYfcEJU/edit#

An example of a student recieving a hint 
![CrowdSourcedHinter Hint Screenshot](crowdsourcedhinter_hint.png)


An example of a hint giving feedback
![CrowdSourcedHinter Student Feedback Screenshot](crowdsourcedhinter_feedback.png)

To bring the crowd sourced hinter into a demo course:

First, follow https://github.com/edx/edx-platform/blob/master/docs/en_us/developers/source/xblocks.rst#testing for general xblock creation.
The name of the module will be "crowdxblock" in advanced settings.

After creating a new unit, add the crowdsourcedhinter xblock just like any other custom xblock. The name of the crowd sourced hinter may not show up for some reason, but an empty space where its name should be will be clickable. 

Testing the functionality of the crowd sourced hinter works best when switching between different users and answering the same problem within a unit. 


After a student incorrectly answers a problem, a hint will be provided. This hint will either be a default hint or a hint that has been submitted specifically for that incorrect answer (if such a hint has previously been submitted). If multiple hints exist for a single incorrect answer, the current system will choose the highest rated hint to show the student. 

After a student has correctly answered the problem, they can give feedback on hints. Students can upvote, downvote, or flag the hint that they recieved for each aswer as well as 2 other hints that exist for that aswer (if these exist). Students also can submit new hints for their answer. 
