
# Admin Instructions
## Developing Starter Code
Developing starter code for labs and assignments should be fairly straight forward. Simply add a repo under this organisation and edit is as you would any other repo. Whatever you put in this repo will be available to students when they import the starter code.

## Releasing a lab/assignment
When a repo is ready to be released (ie it is time to release lab 3 to students), add a tag to the repo. This tag should start with `lab` if it is starter code/solutions for a lab or `ass` if it is starter code for an assignment. To create a tag, use the commands
```bash
git tag [tagname]
git push origin [tagname]
```
OR
Create a new release under the "releases" tab of a repo

Currently it is not possible to tag one commit of a repo as starter code and a later commit as solution code but this functionality is in discussion.
## Removing a released lab/assignment
To remove a repo from the students view, simply remove the tags. It is easiest to do this via the GitHub UI under the tags tab for a repo. Please note that, if you created the tag as a *release* (as in the second method above) then you will have to delete both the *release* and the *tag*
## TravisCI integration
TravisCI is used for automarking students submissions. To set it up for a specific lab, you will have to add a `.travis.yml` file that tells Travis what to do in the root of the repo.
It is suggested you follow something like the following structure:
```yml
language: python
branches: 
    only:
        master
script:
    [test command here]
```
