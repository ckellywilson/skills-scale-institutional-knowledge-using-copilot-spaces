# OctoAcme — Role-Specific Checklists and Templates

## Purpose
This document provides practical checklists and templates for key project roles to ensure consistent execution of responsibilities and clear accountability.

---

## Release Manager Checklist

### Pre-Release Checklist
- [ ] Release branch created and all target PRs merged
- [ ] All acceptance criteria verified and signed off
- [ ] CI/CD pipeline passing (build, tests, security scans)
- [ ] Release notes drafted and reviewed
- [ ] Rollback plan documented and tested
- [ ] Smoke test scenarios prepared
- [ ] Deployment window scheduled (if required)
- [ ] Stakeholder notifications prepared
- [ ] On-call coverage confirmed for release window

### During Release
- [ ] Deploy to staging environment
- [ ] Execute smoke tests on staging
- [ ] Obtain go/no-go decision from stakeholders
- [ ] Deploy to production (follow deployment runbook)
- [ ] Execute post-deployment verification tests
- [ ] Monitor error rates, latency, and key metrics
- [ ] Announce release completion to stakeholders

### Post-Release
- [ ] Confirm all verification tests passed
- [ ] Update release status in project tracking
- [ ] Archive release artifacts and documentation
- [ ] Conduct release retrospective
- [ ] Document lessons learned and process improvements

### Release Notes Template
```markdown
## Release [Version Number] - [Date]

### Summary
Brief description of this release and its primary goals.

### New Features
- Feature 1: Description and benefit
- Feature 2: Description and benefit

### Improvements
- Improvement 1: What was enhanced and why
- Improvement 2: What was enhanced and why

### Bug Fixes
- Fix 1: Issue resolved
- Fix 2: Issue resolved

### Breaking Changes
- Change 1: What changed and migration steps
- Change 2: What changed and migration steps

### Known Issues
- Issue 1: Description and workaround (if available)
- Issue 2: Description and workaround (if available)

### Deployment Notes
- Special deployment instructions or prerequisites
- Configuration changes required
- Data migration steps (if any)

### Rollback Procedure
- Steps to rollback to previous version if needed
```

---

## Communications Lead Checklist

### Communication Plan Setup
- [ ] Identify all stakeholder groups and their information needs
- [ ] Define communication channels and cadences
- [ ] Create distribution lists and access to communication tools
- [ ] Establish communication standards and templates
- [ ] Set up documentation repository and structure
- [ ] Schedule recurring communication touchpoints

### Weekly Status Communication
- [ ] Collect updates from Project Manager and team leads
- [ ] Review risk register for items requiring stakeholder awareness
- [ ] Draft status update using template
- [ ] Review with Project Manager before distribution
- [ ] Distribute to stakeholder groups via appropriate channels
- [ ] Archive communication for project records

### Weekly Status Update Template
```markdown
## Project Status Update — [Project Name] — [Date]

### Progress This Week
- Accomplishment 1
- Accomplishment 2
- Accomplishment 3

### Upcoming Next Week
- Planned work item 1
- Planned work item 2
- Key milestone or decision point

### Risks & Blockers
- Risk 1: Description, impact, mitigation status
- Blocker 1: Description, escalation status

### Decisions Needed
- Decision 1: What needs to be decided and by when
- Decision 2: What needs to be decided and by when

### Questions or Feedback?
Contact [Communications Lead] or [Project Manager]
```

### Incident Communication Checklist
- [ ] Confirm incident severity and impact scope
- [ ] Draft initial incident notification (see template)
- [ ] Distribute to affected stakeholders immediately
- [ ] Provide regular updates every [X] minutes/hours
- [ ] Send resolution notification when incident is closed
- [ ] Share post-incident report and lessons learned
- [ ] Update incident communication runbook as needed

---

## QA Analyst Checklist

### Test Planning Phase
- [ ] Review requirements and acceptance criteria with Product Manager
- [ ] Identify test scenarios and edge cases
- [ ] Design test cases covering functional and non-functional requirements
- [ ] Determine test data needs and setup requirements
- [ ] Plan test environment configuration
- [ ] Estimate testing effort and timeline
- [ ] Communicate testing approach to team

### Test Execution Phase
- [ ] Set up test environment with required configurations
- [ ] Execute test cases and document results
- [ ] Log defects with clear reproduction steps and severity
- [ ] Verify developer fixes and confirm resolution
- [ ] Execute regression testing for related functionality
- [ ] Update test case pass/fail status in tracking system
- [ ] Report testing progress daily in standup

### Test Case Template
```markdown
## Test Case: [TC-ID] [Test Case Name]

**Priority**: High / Medium / Low
**Type**: Functional / Integration / Regression / Performance

### Objective
What this test case validates

### Preconditions
- Precondition 1
- Precondition 2

### Test Steps
1. Step 1: Action to perform
   - Expected Result: What should happen
2. Step 2: Action to perform
   - Expected Result: What should happen
3. Step 3: Action to perform
   - Expected Result: What should happen

### Test Data
- Data element 1: Value or source
- Data element 2: Value or source

### Postconditions
- System state after test completion
- Cleanup steps if required

### Notes
Any additional context or dependencies
```

### Bug Report Template
```markdown
## Bug: [BUG-ID] [Short Description]

**Severity**: Critical / High / Medium / Low
**Priority**: P0 / P1 / P2 / P3
**Status**: New / In Progress / Resolved / Closed
**Found in Version**: [Version]

### Description
Clear description of the bug

### Steps to Reproduce
1. Step 1
2. Step 2
3. Step 3

### Expected Behavior
What should happen

### Actual Behavior
What actually happens

### Environment
- OS: [Operating System]
- Browser: [Browser and version, if applicable]
- Configuration: [Any relevant config]

### Screenshots/Logs
[Attach or link to supporting materials]

### Impact
Description of user impact and affected workflows

### Suggested Fix (Optional)
QA analyst's suggestion for resolution approach
```

---

## Customer Liaison Checklist

### Feedback Collection Cycle
- [ ] Schedule regular customer feedback sessions
- [ ] Prepare discussion guide or survey
- [ ] Conduct customer interviews or surveys
- [ ] Document feedback in standardized format
- [ ] Analyze patterns and themes across feedback
- [ ] Prioritize feedback with Product Manager
- [ ] Share insights with team in planning meetings
- [ ] Close the loop with customers on actions taken

### Customer Feedback Template
```markdown
## Customer Feedback — [Customer Name] — [Date]

### Source
- Customer: [Name/Organization]
- Contact Method: Interview / Survey / Support Ticket / Usage Session
- Facilitator: [Customer Liaison Name]

### Context
Brief description of customer's use case and environment

### Feedback Summary

#### What's Working Well
- Positive point 1
- Positive point 2

#### Pain Points
- Pain point 1: Description and impact
- Pain point 2: Description and impact

#### Feature Requests
- Request 1: Description and use case
- Request 2: Description and use case

### Recommendations
- Recommendation 1: Suggested action based on feedback
- Recommendation 2: Suggested action based on feedback

### Follow-up Actions
- [ ] Action 1: Owner and due date
- [ ] Action 2: Owner and due date

### Customer Response
- [ ] Feedback shared with customer on [date]
```

---

## Metrics/Analytics Owner Checklist

### Metrics Framework Setup
- [ ] Define project success metrics with Product Manager
- [ ] Identify data sources and instrumentation requirements
- [ ] Work with Developers to implement tracking and logging
- [ ] Build dashboards for key metrics and KPIs
- [ ] Establish baseline measurements before changes
- [ ] Set up alerting for metric thresholds
- [ ] Document metric definitions and calculation methods

### Regular Reporting Cycle
- [ ] Collect and analyze metrics data weekly/sprint
- [ ] Identify trends, anomalies, and patterns
- [ ] Prepare metrics summary for team review
- [ ] Present insights and recommendations in sprint reviews
- [ ] Update long-term trend charts and forecasts
- [ ] Archive metrics reports for historical reference

### Metrics Report Template
```markdown
## Metrics Report — [Project Name] — [Period]

### Executive Summary
High-level summary of key findings and recommendations

### Success Metrics

#### [Metric 1 Name]
- **Current Value**: [Value and unit]
- **Target**: [Target value]
- **Trend**: ↑ Improving / ↓ Declining / → Stable
- **Analysis**: Brief interpretation of the metric

#### [Metric 2 Name]
- **Current Value**: [Value and unit]
- **Target**: [Target value]
- **Trend**: ↑ Improving / ↓ Declining / → Stable
- **Analysis**: Brief interpretation of the metric

### Key Insights
- Insight 1: What the data reveals
- Insight 2: What the data reveals

### Recommendations
- Recommendation 1: Data-driven action to consider
- Recommendation 2: Data-driven action to consider

### Experiments & A/B Tests
- Experiment 1: Status and preliminary results
- Experiment 2: Status and preliminary results

### Dashboard Links
- [Link to Dashboard 1]
- [Link to Dashboard 2]

### Appendix
Detailed charts, methodology notes, or supplementary data
```

---

## RACI Matrix Template

Use this template to clarify role assignments for key project activities. RACI stands for:
- **R** = Responsible (does the work)
- **A** = Accountable (owns the outcome)
- **C** = Consulted (provides input)
- **I** = Informed (kept in the loop)

| Activity | PM | PdM | Dev | QA | Release Mgr | Comm Lead | Customer Liaison | Metrics Owner |
|----------|----|----|-----|-------|-------------|-----------|------------------|---------------|
| Define project goals | C | A | C | I | I | C | C | C |
| Create project plan | A | C | C | C | C | C | I | I |
| Implement features | C | C | R/A | C | I | I | I | I |
| Execute test cases | I | C | C | R/A | I | I | C | I |
| Plan release | C | C | C | C | R/A | C | I | I |
| Write release notes | I | C | C | C | R/A | C | I | I |
| Stakeholder updates | C | C | I | I | I | R/A | C | C |
| Gather customer feedback | I | C | I | C | I | C | R/A | C |
| Track project metrics | C | C | I | C | I | I | C | R/A |
| Conduct retrospective | A | C | R | R | R | R | C | C |

_Customize this matrix for your specific project needs._

---

## Using These Templates

### For Project Managers
Reference these checklists when delegating work and verifying completeness of activities. Use the RACI matrix during project kickoff to clarify responsibilities.

### For Role Owners
Use role-specific checklists as your personal guide to ensure you're covering all essential responsibilities. Customize templates to fit your project context.

### For Teams
Review these templates during sprint planning and retrospectives to identify process gaps and improvements.

---

**Related Documents:**
- [Roles and Personas](octoacme-roles-and-personas.md) — Detailed role descriptions
- [Project Planning](octoacme-project-planning.md) — Planning phase guidance
- [Execution & Tracking](octoacme-execution-and-tracking.md) — Execution best practices
- [Release & Deployment](octoacme-release-and-deployment.md) — Release process details

**Related Issue:** [#4 - Adding more personas and roles](https://github.com/ckellywilson/skills-scale-institutional-knowledge-using-copilot-spaces/issues/4)
