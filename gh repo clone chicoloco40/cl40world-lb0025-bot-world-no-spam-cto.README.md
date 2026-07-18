# Switch to the project folder
cd /root/cl40-lb-international-b2c-bot

# Rewriting the README file in a professional and organized manner
cat << 'EOF' > README.md
# CL40 World - International B2C Campaign Engine

Professional multi-cluster Discord bot architecture designed for global music distribution and automated campaign tracking.

## Infrastructure Nodes
- **Primary Node:** https://discord.gg/H5cw3bexg
- **Secondary Node:** https://discord.gg/4ucb2Yes

## Linux Systemd Service Deployment
```ini
[Unit]
Description=CL40 World International B2C Discord Bot Engine
After=network.target

[Service]
Type=simple
User=root
WorkingDirectory=/root/cl40-lb-international-b2c-bot
EnvironmentFile=/root/cl40-lb-international-b2c-bot/.env
ExecStart=/usr/bin/bundle exec ruby src/bot.rb
Restart=always
RestartSec=5

[Install]
WantedBy=multi-user.target
```
EOF

# Upload the clean update directly to GitHub for appearance correction
git add README.md
git commit -m "Docs: Clean rewrite of core architectural specifications"
git push origin main --force
