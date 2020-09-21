# flipgrid-pm
Testing out new things for the transition from JIRA to GitHub.


## Key Requirements
A summary of key requirements for Flipgrid's move from JIRA to GitHub. 

**Tracking**
- Issues, sprints, and release tracking
- Epics & roadmap
- Work dependency tracking across repos

**Administration**
- Roles & permission profiles
- Documentation and requirements (spec) management
- Assign multiple people to issues
- Migration from JIRA to GitHub
- Vidku to Flipgrid repo migration

**Workflow**
- General GitHub pros/cons
- Helpshift integration
- Idea intake
- User notifications
- Figma integration 

**GitHub Plugin Recommendations**
- Overall best for tracking (Zenhub)
- Overall best roadmapping and idea intake (productboard + Zenhub)
- Others


***

### Tracking
#### Issue Types
GitHub issues are differentiated by labels (eg. story, improvement, bug)


#### Projects
Projects track issues and could be used for sprint management. Project templates: Custom, Kanban (Automated or Manual), Bug Triage. Projects made at the org level can also span multiple repos, which would be another avenue for tracking completion of a large feature that spans multiple repos.


#### Milestones
Milestones could be used for release planning/scheduling. It is basically a tag that is added to an issue. Out-of-the-box GitHub implementation doesn't easily allow milestones to span multiple repos, however Zenhub does [provide this efficiency](https://help.zenhub.com/support/solutions/articles/43000010361-create-edit-close-cross-repo-milestones#:~:text=As%20long%20as%20the%20above,be%20selected%20in%20the%20dropdown.).


#### Epics & Roadmap 
Epic and roadmapping within GitHub will require a plugin from the Marketplace. [Zenhub](https://www.zenhub.com/) appears to be the most efficient GitHub native option for everything except for roadmapping. The most optimal roadmapping solution appears to be [productboard](https://www.productboard.com/), which integrates seamlessly into Zenhub (should we choose to pursue). [Detailed overview](https://thedigitalprojectmanager-com.cdn.ampproject.org/v/s/thedigitalprojectmanager.com/zenhub-overview/amp/?_gsa=1&amp_js_v=0.1).


#### Work dependency tracking across repos
GitHub supports cross-repo issue referencing via [Flavored Markdown](https://docs.github.com/en/github/writing-on-github/autolinked-references-and-urls) and [GitHub Documentation](https://docs.github.com/en/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue).


***

### Administration
#### Roles & permission profiles 
View [Access  permissions on GitHub](https://docs.github.com/en/github/getting-started-with-github/access-permissions-on-github#organization-accounts)


#### Documentation and requirements (spec) management 
GitHub offers [Wikis](https://docs.github.com/en/github/building-a-strong-community/about-wikis) which could be a solid solution for spec and requirements storage. 


#### Assign multiple people to issues 
Depending on the solution for Epics - if Zenhub, it appears it may support multiple assignees, else GitHub out-of-the-box supports multiple assignees on issues.


#### Migration from JIRA to GitHub
- Migration of JIRA **open** and **in progress** issues (Epics, Story, Improvement, Bugs, Spikes) to Github
- Migration of 6 months to 1 year of closed JIRA issues for posterity reference - would need to figure out where/how to map them
- Consider migration of labels and custom fields for open and in progress issues

[spring.io migration experience](https://spring.io/blog/2019/01/15/spring-framework-s-migration-from-jira-to-github-issues) migrating from JIRA to Github via a script 


#### Vidku to Flipgrid repo migration 
Most of our repos are still in TeamVidku. Is this our opportunity to migrate to Flipgrid?

***

### Workflows
#### General pros/cons
**Pros to GitHub:** Everything in 1 place and reduced administrative lift for power users in product development. No more license count concerns as we grow. GitHub is owned by Microsoft. Projects made at the org level can span multiple repos. 

**Cons to GitHub:** Non-power users will need to learn how to  utilize GitHub. Epic & Roadmapping tools will require a native integration into GitHub - Chloe's recommendation is [Zenhub](https://www.zenhub.com/). 


#### Prioritization
Out-of-the-box GitHub option for prioritization would be adding a label to an issue. There is no rank ordering. 


#### Helpshift integration
Ability for Support to open issues directly within a dedicated Support repo, and move issues to development team repos and/or link to Epics. We'll need to ask Support to see if Helpshift has any existing connectors with GitHub. 


#### Idea intake
We need to improve our idea intake process. There are no native, public facing solutions GitHub offers. This would require an integration - [productboard](https://www.productboard.com/) integrates with recommended [Zenhub](https://www.zenhub.com/). Should we choose to pursue Zenhub, productboard might be a nice option to also pursue. 


#### User notifications
GitHub has a robust, yet at some times overwhelming, in-app notification system where users can filter notifications by project (repo) and need (mentioned, review requested, etc.). A guide for [configuring notifications.](https://docs.github.com/en/github/managing-subscriptions-and-notifications-on-github/configuring-notifications)


#### Figma integration
The only GitHub Marketplace app for Figma is [Figma Action](https://github.com/marketplace/actions/figma-action) which exports Figma components directly into your repo. This could possibly be a benefit for static, Flipkit, mobile, and/or camera repos. 

***

#### Summary of Tools & Plugin Options
[GitHub Marketplace](https://github.com/marketplace)

**Overall best for tracking** option appears to be [Zenhub](https://github.com/marketplace/zenhub): Project management tool that is integrated natively within GitHub's user interface. Nobody would ever have to leave GitHub. Zenhub states that Microsoft uses them - are they SSPA compliant?
- [Zenhub Help Center Info on Epics](https://help.zenhub.com/support/solutions/articles/43000010341-an-intro-to-zenhub-epics)
- [Pricing](https://www.zenhub.com/pricing)


**Overall best for roadmapping and idea intake** appears to be [productboard](https://www.productboard.com/). productboard states one of their customers is Microsoft - are they SSPA compliant? 
- [productboard + Zenhub roadmap solution](https://help.zenhub.com/support/solutions/43000042876)  
- [Zenhub's roadmap from productboard](https://portal.productboard.com/zenhub/1-zenhub-s-roadmap/tabs/1-launched)
- [Pricing](https://www.productboard.com/pricing/).


**Other Marketplace option** for an Epic creation workaround: [Epic Generator](https://github.com/apps/epic-generator). A bot that facilitates creating Epics. Benefit is issue-specific. 

Beautifying autolink references in issues: [Autolink references](https://docs.github.com/en/github/administering-a-repository/configuring-autolinks-to-reference-external-resources) could assist with beautifying references to links in issues. Out-of-the-box when an issue is referenced, it only hyperlinks the issue #. 

GANTT chart workaround: [GanttLab](https://www.ganttlab.com/): Separate page, but all information is sourced from GitHub issues. The view is a bit inflexible, and I also had to keep entering my personal access token when I'd refresh (not sure what's up with that)

Figma integration: [Figma Action](https://github.com/marketplace/actions/figma-action) which exports Figma components directly into your repo. This could possibly be a benefit for static, Flipkit, mobile, and/or camera repos. 