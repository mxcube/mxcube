# MXCuBE code camp 2024-05-30

## MXCuBE workflows

About workflows for MXCuBE: development, deployment, testing, collaboration, etc.


### Discussion

#### Participants

* Alessandro (Elettra)
* Andrey (Desy)
* Dan (Soleil)
* Fabien (MAX IV)
* Laís (ESS)

#### Notes

_To be completed..._

* Dan:

  What is a good development workflow?

* Fabien:

  At BioMAX, no users on Monday, Tuesday and sometimes Wednesday
  so it is possible to use the beamline to develop software.
  This time is shared with beamline staff and other commissioning work.
  Rest of the week to clean up code and make pull requests
  or work on other tasks.

  At MicroMAX, most coding work is done with emulators assembled in Docker Compose.
  Final tests are done at the beamline.

* Alessandro:

  How to keep up to date with changes upstream on GitHub?

* Fabien:

  ESRF talked a bit about their workflow in their talk the day before.
  They typically rebase their own changes on top of upstream every two weeks.

  At MAX IV, we have a similar workflow, we rebase every two weeks.
  This is okay for now, but we will see if it is sustainable over time.

* Alessandro:

  Is it possible to make a pull request on GitHub from the code on internal GitLab?

* Fabien:

  As far as I know, it is not possible.

  It is important to get very comfortable with git,
  to handle these kinds of cases, switching between multiple repositories.

* Laís:

  It is worth investing time to learn git,
  it makes work much easier, especially in a collaboration like MXCuBE.

* Dan, presents UML diagram of some of the most important classes in MXCuBE-Core:

  I made the diagram by hand, which is time consuming.
  I investigated writing a script that would extract info from code,
  and store info in Neo4J database.
  I chose Neo4J because I know it quite well.
  It would make querying info about the code base easy.
  I could put some more effort into it, if there is interest.

* Laís:

  I would be interested in such diagram.

* Fabien:

  In principle it should be feasible with Sphinx documentation system.
  I have tried it, but the resulting diagram was not readable.
  I should maybe try it again.

_To be completed..._


### Questionnaire

It would be interesting if each facility could share how they handle those topics.

This is a suggestion for a questionnaire to gather this info.

* How to keep up to date with changes on GitHub upstream?
  * How often integrate (latest) changes from upstream?
  * Cherry picking specific changes (i.e.: important bug fixes)?

* How often do you contribute your improvements back to upstream GitHub?
  * Do you have your own forks of MXCuBE repositories?
    * If yes, do you use GitHub, GitLab or anything else like this?

* How to develop?

  * How far can you get working locally on your laptop only?
  * How often do you need to go test directly at the beamline?

* How much resources do you have?

  * How many MXCuBE developers are there in the facility?
    How many MX beamlines with MXCuBE do they have to take care of?

* How to deploy?

  * Python environments
    * Use conda environment? Or standard Python environment? venv, or Poetry?

  * Install Python dependencies?
    * With conda? pip? Poetry?

  * Same question for Javascript dependencies?

  * Infrastructure restrictions?
    * Does you infrastructure/IT team restrict what you can use? Policies?
    * License restrictions
    * Network restrictions
    * Can you use Anaconda?
    * Do you have access to conda channels (package repositories)? PyPI? npmjs.com?

  * Infrastructure services
    * Do you have your own custom conda, PyPI, npm repositories?

  * Do you use Kubernetes, Ansible, or anything like that for deployment?
