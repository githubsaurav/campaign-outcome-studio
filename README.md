# Campaign Outcome Studio

A clickable product concept for an AI experience built on top of Razorpay Engage. It helps a merchant investigate campaign outcomes, review a recommended intervention, approve execution, and learn from measured results.

This is an independent prototype, not an official Razorpay product. All data, agent activity, approvals, experiments, and results are simulated. No real payments, messages, or campaigns are executed.

## Explore the prototype

Start with **Offer clarity** and follow the merchant journey:

1. Investigate the opportunity and supporting evidence.
2. Answer the agent’s questions and choose an intervention.
3. Review the audience, action, and controls before approval.
4. Watch the simulated agent workflow execute.
5. Review results and learning in the experiment.

Six scenarios are included:

- Offer clarity
- Payment recovery
- Incentive efficiency
- Repeat-purchase timing
- Campaign diagnosis using multiple evidence sources
- Profit diagnosis using multiple evidence sources

The fictional merchant is Sunday Home, run by Ananya Shah. Progress is saved in your browser’s local storage. Use the prototype’s reset control, or clear site data, to start fresh.

## Run locally

Requires Python 3 for this optional local server. No dependencies or build step are required.

```sh
python3 -m http.server 8080 --directory dist
```

Open http://localhost:8080.

## Deploy manually on Vercel

1. Create a new Vercel project and import this GitHub repository.
2. Keep the repository root as the **Root Directory** (`./`).
3. Choose **Other** as the framework.
4. Leave the **Build Command** empty (enable its override if needed).
5. Set **Output Directory** to `dist`.
6. Deploy.

The included `vercel.json` supplies these settings. No environment variables, API keys, installation, or backend are needed. If a private repository is not visible, grant the Vercel GitHub app access to this repository.

See [Vercel’s build configuration documentation](https://vercel.com/docs/builds/configure-a-build).

## Files

- `dist/index.html` — application shell and base styles
- `dist/personal.css`, `dist/ambition.css`, `dist/experience.css` — presentation layers
- `dist/workflow.js`, `dist/ambition.js`, `dist/experience.js` — interaction and scenario layers
- `vercel.json` — static hosting configuration

Retain all seven files in `dist` and their current load order. Later layers extend the earlier ones. Navigation uses URL fragments, so server-side route rewrites are not required.

## Scope

This repository contains the prototype only. Research artifacts and demo videos are not part of this export. The prototype has no live Razorpay integration, live AI model, or external execution permissions.
