# Flask CI/CD Pipeline

## Jenkins Pipeline

Stages:

- Checkout
- Build
- Test
- Deploy

Build is automatically triggered using GitHub Webhooks.

Email notifications are configured for success and failure.

## GitHub Actions

Workflow:

- Install Dependencies
- Run Tests
- Build
- Deploy to Staging (staging branch)
- Deploy to Production (release tag)

## Secrets

Repository Settings → Secrets

- DEPLOY_KEY
- API_TOKEN

## Run Locally

```bash
pip install -r requirements.txt

python app.py
```

Jenkis Installtion Steps
sudo apt update

sudo apt install openjdk-17-jdk -y

wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update

sudo apt install jenkins -y

sudo systemctl enable jenkins

sudo systemctl start jenkins

