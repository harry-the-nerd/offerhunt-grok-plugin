# OfferHunt plugin for Grok Build

OfferHunt gives Grok current job openings and the tools to run a job search. This plugin connects Grok Build to OfferHunt's hosted MCP server. It ships no local code, hooks, skills or scripts: only the server address in `.mcp.json`.

Published by Fluey AI, Inc., the company that operates [offerhunt.ai](https://www.offerhunt.ai).

## What you can do

- Search current employer job postings in the United States and Canada.
- Get personalized matches from your resume file and the preferences you confirm, with fit reasons and concerns: strong matches first, and more on request.
- Save or dislike jobs and read a job's requirements and direct application link.
- Record applications you made anywhere and follow them through applied, screening, interview, offer, accepted, ended or withdrawn.
- Coordinate a browser application when your setup can operate the employer's site and you approve it. OfferHunt itself never contacts employers.

Example prompts: "Find senior backend engineering jobs in Seattle", "Show my best new job matches and the preferences you used", "I applied to that job today. Record it and show my applications."

## Install

```bash
grok plugin install harry-the-nerd/offerhunt-grok-plugin
```

Or browse with `/marketplace` in Grok Build once the plugin is listed.

## Sign-in and credentials

The first connection opens OfferHunt in your browser. Sign in with Google and approve access; Grok Build keeps the OAuth tokens. The plugin needs no API key, environment variable or local file. You can disconnect at any time from your OfferHunt account page, https://www.offerhunt.ai/settings.

## Network endpoints

- `https://www.offerhunt.ai/mcp`: the MCP server (Streamable HTTP, OAuth 2.1 with PKCE).
- `https://www.offerhunt.ai/oauth/*` and `https://www.offerhunt.ai/.well-known/*`: sign-in and OAuth discovery.

No other endpoints are called by this plugin.

## Tools

Read: `get_profile`, `search_jobs`, `get_recommendations`, `get_job`, `list_my_jobs`.
Write: `save_resume`, `update_profile`, `delete_resume`, `update_preferences`, `rate_job`, `claim_application`, `prepare_application_submission`, `track_application`, `mark_application_uncertain`, `mark_application_blocked`, `release_application_claim`.

Tool inputs, outputs and limits: https://www.offerhunt.ai/developers.

## Privacy and support

- Privacy policy: https://www.offerhunt.ai/privacy
- Terms: https://www.offerhunt.ai/terms
- Support: https://www.offerhunt.ai/support or contact@fluey.ai

## License

MIT. See [LICENSE](LICENSE).
