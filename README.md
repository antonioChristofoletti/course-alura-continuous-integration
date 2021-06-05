# Continuous Integration (CI)

### Why CI?

- Nowadays we have big teams with a lot of developers;
- The team usually finishes the sprint tasks at same time;
- Problem integrating all the changes and on the merge process and deploying the applications on the dev, qa machines;
- Delay and a lot of headache dealing with all the changes coming at same time.


CI defines some practices and pattern in order to integrate the code in the main repository as fast as possible in small quantities.

It is part of CD (Continous Delivery) and DevOps. 

CD is the next step and it is related the application deploy.

DevOps is a culture moviment aiming a better communication and work among the teams, since the developers until operation team. DevOps is about collaboration, improvement and continuous learning


### How Make It Work?

- CI demands a VCS (git for example) for handle the changes and the differents branch version;
- Test Automation for always test the integrity of the code and make easy the integration in the repositories since there will be a set of tests that will insure the branch stability;
- Automated application build for increase the speed, check the stability and make easier the deploy on the environments;
- Use CI-daemon (CI machine to handle the repo and the CI)


#### How avoid long life branches (Idealist vision)

The idea of CI is put all the new code in a main branch, avoiding feature and development features for example. In order to do that exists many ways, such as:

- Features Flags: Use a flag system to not use the new code until be ok to use it.
- Branch By Abstraction: Each module or feature will be used through an interface, so It will be possible create a new implementation without impacting the current code. Eventually when everything be all right with the new version It will be just necessary switch the implementation.

### Branching Models

Common types of branches:

- Temp branches;
- Features branches;
- Historical branches (master and developer);
- Environment branches (Staging and production);
- Maintenance branches (release and hotflix).

Branching model types:

- Trunk-Based Developement: Everything goes to master, no ramification.
- Feature Branch workflow: Contains master and features branches. It works in a feature branch and then merge in master.
- Gihub flow (master + feature branch + pull request): Add a Pull Request, so someone need to make the codereview what It was done before merge.
- Gitlab flow(Feature Branch + Pull Request + ENV Branches): It has master,feature, pre-production and production branches.
- Git Flow(Feature branches + Pull Request + Maintenance Branches + Historical Branches): It was master, hotfix, release, development and features branches.


#### Cool links

- https://trunkbaseddevelopment.com/;
- https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow;
- https://guides.github.com/introduction/flow/;
- https://docs.gitlab.com/ee/topics/gitlab_flow.html;
- https://danielkummer.github.io/git-flow-cheatsheet/index.pt_BR.html.

### Automated Tests

Use automated tests: unitary, integration, UI tests and smoke tests.

### Automated Build

High-lights points:

- use automatization tools for the build;
- use commit build;
- build needs to be indepedent of the IDE;
- Everything needs to be on the repository;
- Directories structure well known;
- Quick builds that fail first;
- Unique script that build for environments (parameters);
    - Simple commands to build.
- Use buld machine(CI Daemon).

### CI-daemon

Each commit or branch will execute the pipeline to check the status of the code.

There are many CI-daemons tools on market, such as, Jenkins, Gitlab, AWS Code Pipeline  and Azure.

A CI-daemon features and responsabilities:

- Run the build of each branch and repository (Watching changes, find changes to run a new pipeline build/test, run build);
- Give feedback about the pipelines, especially when fails (Integration with Slack for example);
- Publish and keep the build artifact after completed.

### Cool Links

- https://www.thoughtworks.com/pt/continuous-integration;
- https://martinfowler.com/bliki/ContinuousDelivery.html;
- https://martinfowler.com/bliki/ContinuousDelivery.html;
- https://blog.caelum.com.br/branches-e-integracao-continua-o-problema-de-feature-branches/;
- https://blog.caelum.com.br/integracao-continua-builds-rapidos-com-grids-e-paralelismo/;
- https://blog.caelum.com.br/integracao-continua-deploys-e-aprovacoes-sem-dores-de-cabeca-para-o-cliente/;
- http://codebetter.com/jeremymiller/2005/07/25/using-continuous-integration-better-do-the-check-in-dance/.