# 📖 Guestbook Setup Guide (Ganesh Sahu — Ganesh01110)

This guide covers the guestbook setup — both what's automated (via `guestbook.yml`) and what needs to be done manually.

---

## What the Guestbook Does

When someone visits your GitHub profile and wants to connect, they can comment on the Guestbook discussion. The `guestbook.yml` workflow **automatically replies** to every comment with a thank-you + your portfolio link.

**Flow:**
1. Visitor goes to your profile → sees the `📖 Sign My Guestbook` badge
2. They click it → lands on the Guestbook discussion → leaves a comment
3. GitHub Action fires → auto-replies within seconds
4. You get a notification email → can reply personally if you want

---

## ✅ One-Time Manual Steps

### Step 1: Enable GitHub Discussions
- Go to: `https://github.com/saumysingh01/saumysingh01/settings`
- Scroll to **Features** → Check ☑️ **Discussions** → Save

### Step 2: Create "Guestbook" Category
- Go to Discussions tab → ⚙️ **Categories** → **New category**
- Name: `Guestbook`
- Format: **Open-ended discussion**
- Emoji: 📖
- Click **Create**

### Step 3: Post and Pin the Welcome Discussion
- Go to: `https://github.com/saumysingh01/saumysingh01/discussions/new`
- Select **Guestbook** category
- **Title:** `📖 Welcome to My Guestbook!`
- **Body (copy-paste this):**

```markdown
# 👋 Hey there! Thanks for stopping by!

I'm Ganesh — a Full Stack Developer passionate about building scalable systems,
microservices, and agentic AI applications.

Feel free to leave a message below!
- 🙋 Introduce yourself
- 💬 Share thoughts on any of my projects
- 🤝 Propose a collaboration or just say hi

> 💼 Check out my Portfolio: https://saumysingh01.github.io/

Looking forward to connecting with you! 🚀
— Ganesh
```

- Click **Start discussion**
- Click `...` menu (top right of the post) → **Pin discussion**

---

## 🤖 What's Already Automated

The `guestbook.yml` workflow is already committed and pushed. It:
- Triggers on every new **discussion comment**
- Checks if it's in the **Guestbook** category
- Posts an auto-reply mentioning the commenter's username + portfolio link

**Auto-reply message template (in `guestbook.yml`):**
```
👋 Hey @username! Thanks so much for signing my guestbook — really appreciate it! 🎉
Feel free to check out my portfolio and let's connect! 🚀
```

---

## 🔔 Get Notified of New Messages

To receive email notifications:
1. Go to your Discussions tab
2. Click **Watch** (top right)
3. Select **Custom** → check ✅ **Discussions**
4. Save

---

## 📋 Maintenance Tips

- **Reply personally** to collaborate requests — the auto-reply is just the first touch
- **Don't delete spam** — just **lock** the discussion thread instead
- The guestbook badge in `README.md` links to:
  `https://github.com/saumysingh01/saumysingh01/discussions`
  Update this URL if you create a dedicated category link later.
