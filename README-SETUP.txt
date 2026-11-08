ROAM & ADVENTURE V4 — NETLIFY DEPLOYMENT

1. Upload the ZIP file to the DEPLOYS page of your EXISTING Netlify project, using "browse files to upload". Do not upload index.html alone: the ZIP contains the Netlify function too.
2. The site will continue showing sample trip ideas until you connect an AI API key.
3. Create an OpenAI API key in your own OpenAI API account. API usage is billed separately from ChatGPT subscriptions. Set a small spending budget/alerts in your provider account before enabling.
4. In Netlify, go to Project configuration > Environment variables and add OPENAI_API_KEY with your secret key. Do not paste it into index.html or share it in chat. Optional: OPENAI_MODEL (default gpt-4o-mini).
5. Trigger a new deploy AFTER saving the environment variable, so the function can read it. Test the planner and check Netlify function logs if needed.
6. Never advertise unlimited free AI calls. This demo includes only a per-instance cooldown, which is NOT reliable abuse protection across serverless instances. Before promoting the website publicly, add persistent server-side rate limiting / CAPTCHA or other bot protection and a hard cost control mechanism.

The site does not access live hotel/flight prices or booking availability. Search links are not affiliate tracking links. AI itinerary suggestions are not verified travel facts.
