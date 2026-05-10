# WordBridge

A real-time word chain game built with Reflex.

## 🚀 Deployment to Reflex Cloud

To deploy this application to Reflex Cloud, follow these steps:

### Prerequisites
- Ensure you have **Reflex version 0.6.6 or higher** installed.
- Ensure your `requirements.txt` is up to date.

### Steps
1. **Login to Reflex Cloud**
   ```bash
   reflex login
   ```
   This will open your browser to authenticate your account.

2. **Access Your Project Dashboard**
   Navigate to the [Reflex Cloud dashboard](https://reflex.dev) and select your project.

3. **Get the Deployment Command**
   In your project's dashboard, you will find a specific deployment command (e.g., `reflex deploy --project <your-project-id>`).

4. **Deploy**
   Run the deployment command in your terminal:
   ```bash
   reflex deploy --project <your-project-id>
   ```

5. **Verify**
   Follow the interactive prompts in the terminal to complete the deployment.

---

## 🌐 Connecting a Custom Domain (GoDaddy)

To connect your GoDaddy domain to your Reflex Cloud app:

### 1. Add Domain in Reflex Cloud
- Log in to your [Reflex Cloud dashboard](https://reflex.dev).
- Select your app and go to the **Custom Domain** tab.
- Enter your domain (e.g., `yourdomain.com`) and click **Add domain**.
- Reflex will display a set of DNS records (A records or CNAME records). **Keep these handy.**

### 2. Update DNS Settings in GoDaddy
- Log in to your [GoDaddy Account](https://dcc.godaddy.com/).
- Find your domain and click **DNS** (Manage DNS).
- **Add the records** provided by Reflex Cloud:
  - If Reflex provides **A records**, update your `@` record with the provided IP addresses.
  - If Reflex provides a **CNAME record**, update your `www` (or other subdomain) record.
- **Delete** any existing A records that conflict with the new Reflex IP addresses.

### 3. Finalize
- Return to the Reflex Cloud dashboard and click **Verify** or refresh the page.
- Once verified, **redeploy** your app using `reflex deploy`.
- *Note: DNS propagation can take anywhere from a few minutes to 48 hours.*

---

## Local Development

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Run the app:
   ```bash
   reflex run
   ```
