# Monty - Automated GitHub Contributions

A simple GitHub Actions automation project that creates daily contributions to maintain an active GitHub profile.

## What This Project Does

This repository uses GitHub Actions to automatically create daily commits, helping to maintain a consistent contribution streak on your GitHub profile. The automation runs on a schedule and updates a contribution counter in the README.

## Build Schedule

The automation runs on the following schedule:
- **Frequency**: Every weekday (Sunday through Friday)
- **Time**: Midnight UTC (00:00)
- **Cron Expression**: `0 0 * * 0-5`

## How to Modify the Build Schedule

You can modify the build schedule by editing the `.github/workflows/daily-contribution.yml` file:

### Change the Schedule
Edit the `cron` expression in the workflow file:
```yaml
on:
  schedule:
    - cron: '0 0 * * 1-5'  # Current: Monday-Friday at midnight UTC
```

### Common Cron Patterns
- `0 0 * * *` - Daily at midnight UTC
- `0 0 * * 1-5` - Weekdays only (Monday-Friday)
- `0 12 * * *` - Daily at noon UTC
- `0 0 1 * *` - Monthly on the 1st
- `0 0 * * 0` - Weekly on Sundays

### Manual Trigger
You can also manually trigger the workflow:
1. Go to the "Actions" tab in your GitHub repository
2. Select "Daily Contributions" workflow
3. Click "Run workflow" button

## Project Structure

```
monty/
├── .github/
│   └── workflows/
│       └── daily-contribution.yml    # GitHub Actions workflow
├── README.md                        # This file
└── .gitignore                       # Git ignore rules
```

## Contribution Counter

Total contributions: 0

## 🫱 Contributing

Feel free to fork this repository and customize it for your own needs. The automation is designed to be easily modifiable and transparent.

---

*This project is for educational and personal use. Please ensure you comply with GitHub's terms of service when using automated contributions.*