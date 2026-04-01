# ACO Brief Assessment Tool

A lightweight AI-powered tool for assessing ACO communications briefs at daily coordination meetings.

## Files

- `index.html` — the complete tool (single file, no dependencies)
- `robots.txt` — prevents search engine indexing

## Deploying to GitHub Pages

1. Create a new repository on GitHub (can be public — no keys are stored in the code)
2. Upload both files (`index.html` and `robots.txt`) to the repository root
3. Go to **Settings → Pages**
4. Under **Source**, select **Deploy from a branch**
5. Choose **main** branch, **/ (root)** folder, and click Save
6. GitHub will provide a URL in the format: `https://yourusername.github.io/repo-name`
7. Share this URL with your assessment team

## Sharing the API key

- Do NOT put the API key in the code or repository
- Share the key with team members separately (Teams message is fine)
- Each person enters the key once in the tool — it saves to their browser's local storage
- The key is never sent anywhere except directly to the Anthropic API

## API key setup (one-time)

1. Go to console.anthropic.com
2. Create a new API key (name it something like "brief-assessment-tool")
3. Set a monthly spend limit — $10–20 is more than enough for this use case
4. Share the key with your team out of band

## Updating assessment criteria

The assessment dimensions and scoring logic live in the `SYSTEM_PROMPT` constant near the top of the `<script>` block in `index.html`. It is clearly labelled with a comment.

To update criteria:
1. Open `index.html` in a text editor
2. Find the `SYSTEM_PROMPT` section (search for "ASSESSMENT CRITERIA")
3. Edit the dimension descriptions as needed
4. Save and push to GitHub — the deployed tool updates automatically
5. No need to reshare the URL or ask team members to do anything

## Security summary

- No API key in source code or repository
- Keys stored only in each user's browser local storage
- `robots.txt` and `noindex` meta tag prevent search engine discovery
- Monthly spend cap limits blast radius if a key is ever misused
- Revoke and reissue the key at console.anthropic.com if needed
