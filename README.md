# StockSetu

StockSetu is a capstone prototype for everyday inventory, billing and supplier workflows.
## Google sign-in

1. In [Google Cloud Console](https://console.cloud.google.com/) → **APIs & Services → Credentials**, create an **OAuth client ID** of type **Web application**.
2. Under **Authorized JavaScript origins** add every origin the site runs on, e.g. `http://localhost:8000`, `http://127.0.0.1:8000`, and your Vercel URL. (No redirect URI is needed.)
3. Set the client ID as an environment variable on the backend (a local `.env`/shell export, and in Vercel project settings):

   ```
   GOOGLE_CLIENT_ID=1234567890-abcdefg.apps.googleusercontent.com
   ```
4. Install the new dependencies: `pip install -r requirements.txt`.

If `GOOGLE_CLIENT_ID` is not set, the Google button is simply hidden and email/password login keeps working.
