# 🏡 Home Assistant Newt Add-on

## 📌 About this Add-on
This Home Assistant add-on allows you to easily run **Newt** from [Fossorial](https://docs.fossorial.io/Newt/overview) directly in Home Assistant. The add-on lets you configure **PANGOLIN_ENDPOINT**, **NEWT_ID**, and **NEWT_SECRET** via the Home Assistant interface.

## 🚀 Features
✅ Easy installation via Home Assistant Add-on Store  
✅ Automated setup and execution of the Newt container  
✅ Supports `amd64`, `armv7`, `armhf`, and `aarch64` architectures  
✅ Automatic restart on crash  

---

## 🛠️ Installation

### **1️⃣ Add the GitHub Repository as an Add-on Source**
1. Go to **Settings → Add-ons → Add-on Store**.
2. Click the menu (three dots in the top right) and select **Repositories**.
3. Add the following URL:
   ```
   https://github.com/Ferdinand99/home-assistant-newt-addon
   ```
   or
   ```
   https://git.opland.net/Ferdinand99/home-assistant-newt-addon
   ```
5. Click **Add** and wait for the repository to load.

### **2️⃣ Install and Start the Add-on**
1. Find **Newt Add-on** in the list and click **Install**.
2. Go to the **Configuration** tab and enter your values for:
   - **PANGOLIN_ENDPOINT** (e.g., `https://example.com`)
   - **NEWT_ID**
   - **NEWT_SECRET**
3. Click **Save** and then **Start**.
4. Check the **Logs** tab to verify that everything is running correctly.

---

## ⚙️ Configuration
After installation, you can configure the add-on via the Home Assistant UI:

```yaml
PANGOLIN_ENDPOINT: "https://example.com"
NEWT_ID: "your_newt_id"
NEWT_SECRET: "your_newt_secret"
```

### **Docker Environment Variables**
The following environment variables are passed to the `Newt` container:
- `PANGOLIN_ENDPOINT`
- `NEWT_ID`
- `NEWT_SECRET`

---

## 🔍 Troubleshooting
💡 **Add-on does not start?**
- Check the logs in Home Assistant (`Settings → Add-ons → Newt → Logs`).
- Ensure that `PANGOLIN_ENDPOINT`, `NEWT_ID`, and `NEWT_SECRET` are set correctly.

💡 **Changes in configuration do not take effect?**
- Restart the add-on after making changes.
- Try removing the container manually:
  ```sh
  docker stop newt
  docker rm newt
  ```
  Then start the add-on again.

💡 **Docker not available?**
- Home Assistant OS manages Docker automatically, but check if the system has access to Docker by running:
  ```sh
  docker info
  ```
  If this fails, there may be a restriction in Home Assistant OS.

---

## 🔗 Useful Links
- 📖 [Newt Documentation](https://docs.fossorial.io/Newt/overview)
- 🏡 [Home Assistant](https://www.home-assistant.io/)
- 🐳 [Docker Docs](https://docs.docker.com/)

---

## ❤️ Contribute
Have suggestions for improvements? Create a **Pull Request** or report an issue in the **Issues** tab!

---

© 2025 - Made with ❤️ for Home Assistant users 🚀

