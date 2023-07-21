# Lookup Service - Level 1

Your task is to build a backend service that implements the [Lookup Service REST API](https://infra.devskills.app/lookup/api/1.0.0) and integrates with the [Credit Data REST API](https://infra.devskills.app/credit-data/api/1.0.0) to aggregate historical credit data.

Please agree with the hiring team regarding the tech stack choice.

## Before you get started

### If you run into a problem

Head over to [our community on GitHub](https://github.com/orgs/DevSkillsHQ/discussions/categories/help) to get assistance.

### Import a boilerplate project

We have created a set of boilerplate projects for different tech stacks to help you get started quicker.

To import a boilerplate project:

1. Check out [this list](https://help.alvalabs.io/en/articles/7972852-supported-coding-test-boilerplates) to pick a desired boilerplate and copy its name (e.g., `backend-boilerplate-php-laravel`).
2. Go to the "Actions" tab of your GitHub repository and select the "Setup boilerplate" workflow in the left side panel.
3. In the "Run workflow" dropdown, paste the previously copied boilerplate name along with the branch name where you want the boilerplate to be imported (e.g., `implementation`) and click the "Run workflow" button.
4. After the workflow has finished, your selected boilerplate will be imported to the specified branch, and you can continue with your task there.

<details>
<summary>If you instead want to use a custom setup, complete the steps below to make the E2E tests run correctly.</summary>

1. Update the `apiUrl` (where your backend runs) in [cypress.json](cypress.json).
2. Update the [`build`](package.json#L5) and [`start`](package.json#L6) scripts in [package.json](package.json) to respectively build and start your app.

</details>

### Try running the API tests

<details>
<summary>Remotely on the GitHub Actions pipeline</summary>

Push your code to the new `implementation` branch (create it if it doesn't exist), which will trigger a new pipeline run that will run the tests.
  
Check the 'Actions' tab to see the historical runs.

</details>


<details>
<summary>Locally with Docker (Mac & Windows only)</summary>
  
#### Prerequisites

- [Install Docker](https://www.docker.com/get-started)
- Start your app
  
#### Run the tests
```bash
 docker run --add-host host.docker.internal:host-gateway -v $PWD:/e2e -w /e2e cypress/included:3.4.0
```

You can either use the console output or generated screenshots/videos (*check the newly created files that appear after a test run*) to troubleshoot the test results.


</details>

<details>
<summary>Locally with npm</summary>
  
#### Prerequisites

1. [Install node](https://nodejs.org/en/)
2. When in the project's root, run: `sed 's/host.docker.internal/localhost/g' cypress.json > cypress.json.tmp && mv cypress.json.tmp cypress.json`  
3. Start your app
  
#### Run the tests
```bash
 npm run test
```

You can either use the console output or generated screenshots/videos (*check the newly created files that appear after a test run*) to troubleshoot the test results.

</details>

## What we expect from you

1. Make the provided API tests pass.
2. Push your code to the new `implementation` branch. We encourage you to commit and push your changes regularly as it's a good way for you to showcase your thinking process.
3. Create a new pull request, but please **do not merge it**.
4. Document the tech decisions you've made by creating a new review on your PR ([see how](https://www.loom.com/share/94ae305e7fbf45d592099ac9f40d4274)).
5. Await further instructions from the hiring team.

## Time estimate

Between **30min-1h** depending on your experience level + the time to set up the project/environment (go with one of the provided boilerplates to move quicker). 

Also, there is no countdown. The estimate is for you to plan your time.

---

Authored by [Alva Labs](https://www.alvalabs.io/).