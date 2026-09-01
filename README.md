# Autumn 2026 QA Hiring Homework

This repository contains a sample React application used to assess the candidate's skills in the QA task. The repo is front-end only.

**Fork this repository** and work in an isolated copy of your own. Forking gives you your own independent copy of the repo where you can commit, branch, and push freely without affecting the original or other candidates' work. Each candidate works only in their own fork, so your work stays private to you.

## The Sample App

The app is a simple Task Manager application that displays a list of Tasks.
A task has 5 ( user-facing ) properties:

```
- Title - string
- Description - string
- Importance - High, Medium, Low
- Label - Work, Social, Home, Hobby
- Completeness - boolean
```

The app has the following features:

1. User should be able to **add** a task
2. User should be able to **delete** a task
3. User should be able to **edit** a task
4. User should be able to **mark** a task as **complete / incomplete**
5. User should be able to **filter** tasks **by label**
6. User should be able to **sort** tasks **by importance**

Product requirements for adding tasks are:

1. Title and Importance are required
2. Description and Label are optional
3. Completeness is set to false by default
4. Importance is set to Medium by default
5. Label is set to Work by default
6. Title should start with capital letter

Other requirements are up to the candidate's interpretation - since a lot of the times on the job, requirements are not clear and the QA has to make a decision based on the context. A thing to keep in mind is that the app should be user-friendly and intuitive.

## Homework

The position is highly focused on automation ( around 90% ), but sometimes manual testing is inevitable - especially when trying to move things along and validate small fixes for deploys - that's why we expect candidates to be proficient in both. The homework is divided into two parts:

1. Exploratory Testing and Bug Reporting
2. Automated Testing

### Exploratory Testing and Bug Reporting

- The candidate is expected to test the application and report any bugs found.
- We encourage to look for both functional and visual (UX) bugs.
- The candidate should provide a report of the bugs found.

You will be evaluated on the quality of the report and the bugs found.

### Automated Testing

The candidate is expected to write automated tests for the application, by choosing either Cypress or Playwright as the testing framework.
Here is what should be covered

- 5 user stories
- 3 regression tests for functional bugs found during manual testing ( they should fail when run, because the bugs are not fixed yet )
- A test that generates a test of all possible combinations of the task properties ( importance, label, completeness ) and takes a screenshot of the app after each combination is added.

The test suite must also run in CI. Add **two GitHub Actions workflow files** under `.github/workflows/`:

- `e2e.yml` — runs the functional / end-to-end tests
- `visual.yml` — runs the visual (screenshot) tests and uploads the results to **[Argos](https://argos-ci.com)** for visual regression comparison

## Steps to follow

1. **Fork** this repository to your own GitHub account - https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo . Your fork is your own isolated copy to work in.
2. Invite the reviewer to your fork valaheugen(valaheugen237@gmail.com)
3. Clone your fork
4. Install the dependencies `npm install`
5. Run the app using `npm run dev`, http://localhost:5173/
6. Start testing the app
7. Write the bug report based on findings and commit it in the root folder
8. Install the testing framework of your choice
9. Write the automated tests
10. Add two CI workflow ( `.yml` ) files in `.github/workflows/` — one for the e2e tests and one for the visual tests ( Argos )
11. Commit the tests and workflows to the project
12. Push the changes to your fork on a new branch
13. Open a PR to the main branch of your fork
14. Add the reviewer as a reviewer to the PR

If you have any questions, feel free to open an issue in your own fork and I'll do my best to answer them ASAP.
