# DevSearch

A community platform for developers, built with Django. Developers create a profile, list their skills, showcase their projects, review and vote on each other's work, and message one another.

## Features

- **Developer profiles**: bio, location, profile photo, and social links (GitHub, LinkedIn, Twitter, YouTube, website)
- **Skills**: add, edit, and remove skills on your profile
- **Project showcase**: post projects with a featured image, demo link, source link, and tags
- **Reviews & voting**: up-vote or down-vote other developers' projects and leave feedback. One review per user per project, and projects are ranked by vote ratio.
- **Search & pagination**: browse developers and projects
- **Private messaging**: inbox with read/unread status; anyone can message a developer from their profile
- **Authentication**: register, log in, log out; a profile is created automatically on sign-up through Django signals
- **Welcome emails**: new users get a welcome email over SMTP when they sign up

## Tech Stack

| Layer | Tools |
|---|---|
| Backend | Python, Django |
| Database | SQLite |
| Frontend | Django templates, HTML, CSS |
| Data | UUID primary keys, Django signals, image uploads |

## Project Structure

```
devsearch/   # project settings and root URLs
projects/    # projects, tags, reviews and voting
users/       # profiles, skills, messaging, auth, signals
templates/   # shared templates (navbar, pagination, forms)
```

## Running Locally

```bash
git clone https://github.com/ProsperIhionu100/devsearch.git
cd devsearch
python -m venv venv
venv\Scripts\activate        # macOS/Linux: source venv/bin/activate
pip install django pillow
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Open http://127.0.0.1:8000.

---

Built by **Prosper Ihionu** · [Portfolio](https://tech-with-prosper.vercel.app)
